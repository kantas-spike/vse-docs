.. Zoom
ズーム
....

.. In a video project it is important that you can zoom in on the section you're working on. On the other hand it's also important to have an overview of your timeline. Zooming in and out is thus a frequent occurring action.

動画編集プロジェクトでは、作業中のセクションを拡大できることが重要です。一方で、タイムラインの概要を把握することも重要です。したがって、ズームインとズームアウトは頻繁に行われるアクションです。

.. only:: not epub

  .. raw:: html

    <iframe width="560" height="315" src="https://www.youtube.com/embed/mgmaP45gKqA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    図1: すべてのズーム コマンドを使用した注釈付きビデオ

.. only:: epub

  .. image:: https://img.youtube.com/vi/mgmaP45gKqA/sddefault.jpg
    :alt: すべてのズーム コマンドを使用した注釈付きビデオ
    :target: https://www.youtube.com/embed/mgmaP45gKqA
  図1: すべてのズーム コマンドを使用した注釈付きビデオ

.. note::
   .. As with all commands in Blender, the interpretation of it depends on the position of the mouse cursor. Pressing :kbd:`Home` when the mouse cursor is over the preview window will only zoom the preview window. To zoom in or out of the Sequencer, your mouse cursor must be over that area.

   Blender のすべてのコマンドと同様に、その解釈はマウス カーソルの位置によって異なります。マウス カーソルが Preview ウィンドウ上にあるときに :kbd:`Home` を押すと、Preview ウィンドウのみがズームされます。Sequencer をズームインまたはズームアウトするには、マウス カーソルがその領域上にある必要があります。




.. figure:: /images/editors_vse_sequencer_timeline_menu-view.svg
   :alt: Menu View
   :align: right

   図2: View メニュー

.. |previous-button| image::
   /images/editors_vse_sequencer_timeline_previous-button.png
   :alt: Back to Previous button
   :scale: 60%

.. |restore-button| image::
   /images/editors_vse_sequencer_timeline_restore-button.png
   :alt: Restore button
   :scale: 40%


.. _sequencer_full_view:

Ctrl-Spacebar
   .. The :kbd:`Ctrl-Spacebar` key will switch the window under the mouse cursor into semi-full view. The header and menus are still visible. The video in figure 1 is created with this view. You can tell because at the very top, there is a button "Back to Previous" |previous-button|. This full-screen view will help you to keep an overview; especially in the vertical dimension (channels). Pressing :kbd:`Ctrl-Spacebar` again or the Back to Previous button will restore the window. You can invoke this command from the menu: View > Area > Toggle Maximize Area.

   :kbd:`Ctrl-Spacebar` キーを押すと、マウス カーソルの下にあるウィンドウがセミフルビューに切り替わります。ヘッダーとメニューは引き続き表示されます。図 1 のビデオはこのビューで作成されています。
   一番上に [Back to Previous] ボタン  |previous-button| があるのでわかります。この全画面表示は概要を把握するのに役立ちます。特に垂直方向の次元（チャネル）において。もう一度 :kbd:`Ctrl-Spacebar` 押すか、[Back to Previous] ボタンを押すと、ウィンドウが復元されます。このコマンドはメニューから呼び出すことができます: [View] > [Area] > [Toggle Maximize Area]

Alt-Ctrl-Spacebar
   .. The :kbd:`Alt-Ctrl-Spacebar` key will switch the window under the mouse cursor into full view. All the available screen space is reserved for the Timeline. To restore the window, you need to press :kbd:`Alt-Ctrl-Spacebar` again. *No other key will do!* Or you can hover your mouse over the top right corner of the window until the restore button |restore-button| pops up. *It's very easy to miss!* You can invoke this command from the menu: View > Area > Toggle FullScreen  Area.

   :kbd:`Alt-Ctrl-Spacebar` キーを押すと、マウスカーソルの下にあるウィンドウが全体表示に切り替わります。利用可能な画面スペースはすべてタイムライン用に予約されています。ウィンドウを元に戻すには、もう一度 :kbd:`Alt-Ctrl-Spacebar` 押す必要があります。 *他のキーは役に立ちません* 。または、復元ボタン  |restore-button|  が表示されるまで、ウィンドウの右上隅にマウスを置きます。*とても見逃しやすいです！* このコマンドはメニューから呼び出すことができます: [View] > [Area] > [Toggle FullScreen  Area]

Home
   .. Pressing the :kbd:`Home` key zooms in on the total project; from Start to End and from channel 0 to channel 7. If some strips are beyond these borders, the range is extended to cover these strips (see section on :doc:`Moving the Timeline window <move>`. Whenever you get lost in your timeline, press the :kbd:`Home` key to get back at the complete picture. Many Zoom commands can also be issued from the menu (see figure 2). The menu equivalent for :kbd:`Home` is: View > Frame All.

   :kbd:`Home` キーを押すと、プロジェクト全体が拡大表示されます。開始から終了まで、およびチャンネル 1 からチャンネル 7 まで。一部のストリップがこれらの境界を越えている場合、範囲はこれらのストリップをカバーするように拡張されます (:doc:`Moving the Timeline window <move>` セクションを参照してください)。タイムラインで迷った場合は、 :kbd:`Home` キーを押して、全体像に戻ります。多くのズーム コマンドはメニューから実行することもできます (図 2)。:kbd:`Home` と同等のメニューは [View] > [Frame All] です。

NumpadPeriod
   .. Pressing the :kbd:`NumpadPeriod` key zooms the Visible Range to fit only the selected strips. Please note that this key is the period key on the numpad, not the period key on the alphanumeric keypad. The menu equivalent is: View > Frame Selected (see figure 2).

   :kbd:`NumpadPeriod` キーを押すと、選択したストリップのみに合わせて表示範囲がズームされます。このキーはテンキーのピリオド キーであり、英数字キーパッドのピリオド キーではないことに注意してください。同等のメニューは、[View] > [Frame Selected] です (図2)。

   .. Warning::
      .. If you don't have a numpad, the `Emulate Numpad <https://docs.blender.org/manual/en/dev/editors/preferences/input.html>`_ option in the User Preferences will not help you out. You cannot use the regular period key from the alphanumeric keypad.
      テンキーをお持ちでない場合、ユーザー設定の `Emulate Numpad <https://docs.blender.org/manual/en/dev/editors/preferences/input.html>`_ オプションは役に立ちません。英数字キーパッドから通常のピリオド キーを使用することはできません。


      .. _keymaps:

      .. You can however change these shortcuts or make some of your own. Blender Frenzy has a nice video about creating these `Custom Keymaps <https://www.youtube.com/watch?v=2RtlvZfv8TI>`_.

      ただし、これらのショートカットを変更したり、独自のショートカットを作成したりできます。Blender Frenzy には、これらの `Custom Keymaps <https://www.youtube.com/watch?v=2RtlvZfv8TI>`_ に関する素晴らしいビデオがあります。

Numpad +/-
   .. Pressing the :kbd:`Numpad +` or :kbd:`Numpad -` key will zoom in or out in small incremental steps (+/- 5 frames, +/- 10 frames, +/- 15 frames, ...), starting from the current Visible Range. You can continue pressing the key until you have reached the desired zoom level.

   :kbd:`Numpad +` または :kbd:`Numpad -` キーを押すと、現在の表示範囲から開始して、小さな増分ステップ (+/- 5 フレーム、+/- 10 フレーム、+/- 15 フレーム、…) でズームインまたはズームアウトします。希望のズーム レベルに達するまでキーを押し続けることができます。

Shift-B
   .. After pressing the :kbd:`Shift-B` key (from Box Select), a crosshair cursor appears and you can click and drag to draw a rectangle in the Sequencer window. Upon releasing the mouse button, the Visible Range is zoomed to this rectangle. The menu equivalent of pressing :kbd:`Shift-B` is: View > Zoom (see figure 2).

   :kbd:`Shift-B` キーを押すと、十字カーソルが表示され、クリックしてドラッグしてSequencerウィンドウに矩形で範囲選択できます。マウスボタンを放すと、表示範囲がこの矩形にズームされます。 :kbd:`Shift-B` を押すのと同等のメニューは、[View] > [Zoom]  です (図2)。

MMB + Wheel Roll
   .. Scrolling the middle mouse wheel will zoom in horizontally around the playhead. Scrolling towards yourself will zoom out. Scrolling towards the screen will zoom in.

   マウスの中ホイールをスクロールすると、Playheadの周囲を水平方向にズームインします。自分の方にスクロールするとズームアウトします。画面に向かってスクロールするとズームインします。

   .. Using the MMB wheel roll in combination with Ctrl or Shift will change the behavior from zoom to move (see :doc:`Moving the Timeline window <move>`).

   Ctrl または Shift と組み合わせて MMB ホイール ロールを使用すると、動作がズームから移動に変わります(:doc:`Moving the Timeline window <move>`を参照)。

Ctrl-MMB + drag
   .. Pressing :kbd:`Ctrl-MMB` and dragging left will zoom out or dragging right will zoom in. Dragging up will zoom in vertically and dragging down will zoom out vertically.
    :kbd:`Ctrl-MMB`を押して左にドラッグするとズームアウトし、右にドラッグするとズームインします。上にドラッグすると垂直にズームインし、下にドラッグすると垂直にズームアウトします。

   .. It's important to press the :kbd:`Ctrl-MMB` first and then drag.
   最初に:kbd:`Ctrl-MMB` を押してからドラッグすることが重要です。

Scrollbar circles
   .. At the bottom and far right of the sequencer area, there are scrollbars. The length or the height of the scrollbar gives you an indication how much percentage of the Strip Range is visible. Pressing the :kbd:`Home` key for example will make the scrollbars at full length and height because the Visible Range will then be equal to the Strip Range.

   Sequencer領域の最下部と右端には、スクロールバーがあります。スクロールバーの長さまたは高さは、Strip Range のどのくらいの割合が表示されているかを示します。例えば :kbd:`Home` キーを押すと、表示範囲が Strip Range と等しくなるため、スクロールバーが最大の長さと高さになります。

   .. Each scrollbar has a circle at the beginning and end (see figure 3). Dragging these circles will shrink or expand the scrollbar length or height and therefore also the Visible Range. For example, in figure 3, dragging the left zoom circle to the left, will expand the Visible Range from frame 200 to frame 1 (which is the start of the project). The right zoom circle can be dragged to frame 1000 (End of the project). At that moment the scrollbar is full length (you see the complete project Duration). The visible range will then be larger than the Strip Range and will ultimately show you the largest visible Range possible in Blender, which is -500 000 to + 500 000 frames.

   各スクロールバーの最初と最後には円があります (図3)。これらの円をドラッグすると、スクロールバーの長さまたは高さが縮小または拡大され、これに従い 表示範囲も縮小または拡大されます。たとえば、図3 では、左側のズームサークルを左にドラッグすると、表示範囲がフレーム 200 からフレーム 1 (プロジェクトの開始点) まで拡大されます。右のズームサークルをフレーム 1000 (プロジェクトの終わり) にドラッグできます。この時点で、スクロールバーは全長になります (完全なプロジェクトの範囲が表示されます)。表示範囲はStrip Rangeより大きく、最終的には Blender で可能な最大の表示範囲 (-500,000 ～ + 500,000 フレーム) が表示できます。

.. figure:: /images/editors_vse_sequencer_timeline_scrollbar-circles.svg
   :alt: Scrollbars
   :align: right

   図3: ズームサークルと垂直・水平スクロールバー

.. Most commands from above will zoom in or out on both dimensions simultaneously. For example, the :kbd:`Home` will zoom until all strips are visible, both on the horizontal and vertical dimension. With the scrollbar circles, you can zoom in or out in one dimension only and choose in which direction you want to zoom.

上記のほとんどのコマンドは、両方の次元を同時に拡大または縮小します。たとえば、:kbd:`Home` は水平方向と垂直方向の両方ですべてのストリップが表示されるまでズームします。スクロールバーの円を使用すると、1 次元でのみズームインまたはズームアウトし、ズームする方向を選択できます。
