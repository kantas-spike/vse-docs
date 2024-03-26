Python
******

.. The following scripts could best be tested in an adapted workspace.
次のスクリプトは、調整されたワークスペースでテストするのが最適です。

..
  (1) From an existing video editing project, switch to the Scripting Workspace (eventually, click on the Add Workspace button in the menu bar)
  (2) Replace the 3D Editor window (top left) with the Video Sequencer.
  (3) Select an appropriate object (e.g. movie strip) in the sequencer ( See figure 1). Working within this workspace is explained in :doc:`python-scripting-workspace`.
..

(1) 既存のビデオ編集プロジェクトから、[Scripting Workspace] に切り替えます (最終的には、メニュー バーの [Add Workspace] ボタンをクリックします)
(2) 3D エディタ ウィンドウ (左上) をビデオ シーケンサに置き換えます。
(3) シーケンサーで適切なオブジェクト (ムービー ストリップなど) を選択します (図1)。このワークスペース内での作業については、 [Scripting Workspace] で説明しています。

.. figure:: img/adapted-workspace.svg
   :alt: Adapted scripting workspace
   :align: Right

   図1 VSE スクリプト用に調整されたスクリプト ワークスペース

.. Adding still_offset fields
still_offset フィールドの追加 [#f1]_
==========================

/video_editing/edit/montage/striptypes

.. Blender exposes 9 time codes in the UI (see :doc:`Movie strip  </video_editing/edit/montage/striptypes/movie>`). There are more available through the Python API. Table 1 shows all the available time codes. The second column is the name from the sidebar (UI) and the third column is the name from the Python API.

Blender は UI で 9 つのタイム コードを公開します (参照 :doc:`Movie strip  </video_editing/edit/montage/striptypes/movie>` )。
Python API を通じて利用できるものは他にもあります。表 1 に、使用可能なすべてのタイム コードを示します。2 列目はサイドバー (UI) からの名前で、3 列目は Python API からの名前です。

.. csv-table:: Table 1: Time code fields in UI and from Python API
   :header: "#", "UI field", "Python API (1)"
   :widths: 5, 50,50

   0 , Channel (2)           , channel
   1 , Start                 , frame_start
   2 , *Visible in strip (3)* , frame_final_start
   3 , Duration              , frame_final_duration
   4 ,                       , frame_duration
   5 , End                   , frame_final_end
   6 , Strip Offset Start    , frame_offset_start
   7 , Strip Offset End      , frame_offset_end
   8 , Hold Offset Start     , animation_offset_start
   9 , Hold Offset End       , animation_offset_end
   10, Current Frame         , *calculated (4)*
   11,                       , frame_still_start
   12,                       , frame_still_end


.. If you want to see those values in the side panel, you'll have to extend the existing code; It's rather easy. Select a movie strip and right-click on a timecode field, e.g. Hold Offset Start and choose "Edit Source". The "space_sequencer.py" code will become visible (op open with the Browse Text to be linked button at the top middle). Search in this code (Ctrl + F) for the string "Hold Offset Start". It is about line 1607 (Blender 3.1). Add the following code after the Hold Offset section (about line 1877).

これらの値をサイド パネルに表示したい場合は、既存のコードを拡張する必要があります。それはかなり簡単です。ムービー ストリップを選択し、タイムコード フィールドを右クリックします。たとえば、[Offset Start] を押したままにして、[Edit Source] を選択します。「space_sequencer.py」コードが表示されます（上部中央のリンクするテキストの参照ボタンで開きます）。このコード内で (Ctrl + F) 文字列「Hold Offset Start」を検索します。1607行目(Blender 3.1)についてです。Hold Offset セクション (1877 行目あたり) の後に次のコードを追加します。

.. code-block:: Python

   split = sub.split(factor=0.5 + max_factor, align=True)
   split.alignment = 'RIGHT'
   split.label(text="Still Offset Start")
   split.prop(strip, "frame_still_start", text=smpte_from_frame(strip.frame_still_start))

   split = sub.split(factor=0.5 + max_factor, align=True)
   split.alignment = 'RIGHT'
   split.label(text="End")
   split.prop(strip, "frame_still_end", text=smpte_from_frame(strip.frame_still_end))

.. Run the code Alt + P). The sidebar will be changed. See figure 2. Note that this code will not run automatically when you open the file again. If you want the changes to be persistent, you should convert the space_sequencer.py code into an add-on.

:kbd:`Alt+P` で コード を実行します。Sidebar が変更されます。
図 2 を参照してください。ファイルを再度開いたときに、このコードは自動的に実行されないことに注意してください。変更を永続的にしたい場合は、space_sequencer.py コードをアドオンに変換する必要があります。

.. figure:: img/script-adding-still-fields.svg
   :alt: Script
   :align: Right

   図2 上記のスクリプトを実行した結果

.. rubric:: 脚注

.. [#f1] still_offset は Blender4.0 は廃止されています。
