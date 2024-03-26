Toolbar
-------
.. The Toolbar can be toggled on or off with :menuselection:`View --> Toolbar` or the shortcut :kbd:`T`. It contains 12 tools; spread over 8 icons (see figure 1, left side).

Toolbar は、[View] > [Toolbar] またはショートカット :kbd:`T` でオンまたはオフを切り替えることができます。12 個のツールが含まれており、8 つのアイコンにまたがります (図1 の左側を参照)。

.. figure:: /images/editors_vse_preview_toolbar_select.svg
   :alt: Sample Tool

   図1: Sequencer & Preview の Toolbar

.. Figure 1 shows the Sequencer & Preview View of the Sequence Editor. This means that the Toolbar (at the left) and the Sidebar (at the right) contain entries that apply both to the Sequencer and Preview View. For example, the Blade tool (left bottom) is normally only visible in the Sequencer view. The Sidebar also contains panels from both views.

図 1 は Video Sequence Editor の Sequencer と Preview ビューを示しています。これは、Toolbar (左側) と Sidebar (右側) に、Sequencer と Preview ビューの両方に適用されるエントリが含まれていることを意味します。たとえば、Bladeツール (左下) は通常、Sequencer ビューでのみ表示されます。Sidebarには、両方のビューのパネルも含まれています。


Select tool :kbd:`W`
   .. figure:: /images/editors_vse_preview_toolbar_select.png
      :alt: Select Tool
      :align: right
      :scale: 50%

      図2: Selectツール と そのサブツール

   .. The Select tool contains two sub-tools; indicated by the small triangle at the bottom-right corner. The last selected sub-tool is displayed on the icon when collapsed. Selecting a strip in the Preview will also select the strip in the Sequencer and vice versa.

   選択ツールには 2 つのサブツールが含まれています。右下隅の小さな三角形で示されます。最後に選択したサブツールは、折りたたまれたときにアイコン上に表示されます。Preview でストリップを選択すると、Sequencer でもそのストリップが選択され、その逆も同様です。

   .. The Tweak sub-tool is the regular select tool. With :kbd:`Shift` pressed, you can select multiple strips. The strip with the white border is the Active object; those with an orange border are selected (but not active). The tools from the Toolbar will act on all selected strips. The Properties from the Sidebar will only affect the Active object. For example; strip 1 and 3 are selected (with strip 3 the active one). Both will be rotated, if done with the Rotate tool. But, only strip 3 will be rotated if done with the Rotate field in the Side bar. However, pressing :kbd:`Alt Enter` after entering a value in the Rotate field will also affect both strips.

   Tweak サブツールは通常の選択ツールです。:kbd:`Shift` 押すと、複数のストリップを選択できます。白い枠線の帯はアクティブ オブジェクトです。オレンジ色の枠線が付いているものは選択されています (ただしアクティブではありません)。Toolbar のツールは、選択したすべてのストリップに作用します。Sidebar のプロパティは、アクティブなオブジェクトにのみ影響します。例えば; ストリップ 1 と 3 が選択されています (ストリップ 3 がアクティブです)。回転ツールを使用すると、両方が回転します。ただし、Sidebar の回転フィールドを使用すると、ストリップ 3 のみが回転します。ただし、「回転」フィールドに値を入力した後に :kbd:`Alt Enter` を押すと、両方のストリップにも影響します。

   .. In the Sequencer view all strips are stacked at the same position in different channels. Strips at a higher channel lay on top in the Preview window. Therefore, strip 1 is overlapped by strip two; which is overlapped at its turn by strip 3.

   Sequencer ビューでは、すべてのストリップが異なるチャンネルの同じ位置にスタックされます。高いチャンネルのストリップが Preview ウィンドウの一番上に表示されます。したがって、ストリップ 1 はストリップ 2 とオーバーラップされます。これは、今度はストリップ 3 によってオーバーラップされます。

   .. Warning::
      .. Strips can be on top of other strips (e.g. strip 6 in figure 1). Clicking within the area of strip 6 (with the Tweak sub-tool selected) will however select the blue color strip beneath it. Clicking a second time will select strip 6. In other words, when clicking on a shared pixel of overlapping strips, the strip from the lowest channel in the Sequencer view will be selected first and then upon further clicking the channels above.

      ストリップは他のストリップの上に置くことができます (たとえば、図 1 のストリップ 6)。ただし、(Tweak サブツールを選択した状態で) ストリップ 6 の領域内をクリックすると、その下の青色のカラー ストリップが選択されます。もう一度クリックすると、ストリップ 6 が選択されます。つまり、重なっているストリップの共有ピクセルをクリックすると、シーケンサー ビューの最下位チャンネルのストリップが最初に選択され、次に上のチャンネルをクリックするとさらに選択されます。 [#f1]_

   .. The shortcut for the Select tool is :kbd:`W`. The mouse cursor must be above the Preview window. Pressing :kbd:`W` consecutively will toggle between Tweak and Box Select mode.

   選択ツールのショートカットは :kbd:`W` です。マウスカーソルはPreviewウィンドウの上にある必要があります。連続して :kbd:`W` 押すと、Tweak モードと Box Select モードが切り替わります。

   .. If the Select Box sub-tool is selected, you can drag a dashed line rectangle in the Preview window. Every strip that has at least one pixel within this rectangle will be selected. Note however that the active strip is not changed.

   [Select Box] サブツールが選択されている場合は、Preview ウィンドウで破線の矩形をドラッグできます。この矩形内に少なくとも 1 つのピクセルがあるすべてのストリップが選択されます。ただし、アクティブなストリップは変更されないことに注意してください。

   .. warning::
      .. You can also just click without dragging with this sub-tool. You will select then a single strip. The active strip however is changed.
      このサブツールを使用すると、ドラッグせずにクリックするだけで済みます。次に単一のストリップを選択します。ただし、アクティブなストリップは変更されます。

Cursor tool
   .. The white-red circle with a crosshair is called the 2D cursor. You can place this cursor at any location within the preview window (including the area outside the Render region). This cursor in itself doesn't do anything but is used in conjunction with the Pivot Point (to the right of the View menu in the Header).

   十字線が付いた白赤の円は 2Dカーソルと呼ばれます。このカーソルは、Preview ウィンドウ内の任意の場所 (レンダリング領域の外側の領域を含む) に配置できます。このカーソル自体は何も行いませんが、[Pivot Point] (Headerの [View] メニューの右側) と組み合わせて使用​​されます。

   .. Setting the Pivot point to *2D Cursor* will scale and rotate all strips in relation to this point. For example, strip 2 will be rotated in a kind of circle path with the 2D cursor at its center.

   Pivot Point を2Dカーソルに設定すると、このポイントを基準にしてすべてのストリップが拡大縮小および回転されます。たとえば、ストリップ 2 は、2Dカーソルを中心にして一種の円パス内で回転します。

   .. You can only switch the display of this 2D cursor off by disabling all Overlays (rightmost button in the Header).

   この 2D カーソルの表示をオフに切り替えるには、すべての[Overlay](Headerの右端のボタン) を無効にする必要があります。

Move tool
   .. The shortcut for the Move tool is :kbd:`G` (Grab). You can also click on the Move icon in the toolbar and start dragging the strip. A message appears beneath the menu: `Dx:0.0000 Dy: 0.0000 (0.0000)`; indicating the distance in pixels that the strip has been moved in the X and the Y direction. The number between parenthesis is the Euclidean distance that has been moved.

   移動ツールのショートカットは :kbd:`G`(Grab) です。ツールバーのMoveアイコンをクリックして、ストリップのドラッグを開始することもできます。メニューの下に次のメッセージが表示されます。Dx:0.0000 Dy: 0.0000 (0.0000) これは、ストリップが X 方向と Y 方向に移動した距離をピクセル単位で示します。括弧内の数値は、移動されたユークリッド距離です。

   .. You can constrain the movement in different ways: along the X or Y axis, in smaller or larger increments or by specific number of pixels; see :doc:`Montage > Move </video_editing/edit/montage/move>` for a more detailled description.

   さまざまな方法で動きを制限できます。X 軸または Y 軸に沿って、より小さな増分またはより大きな増分で、あるいは特定のピクセル数で。詳細については、:doc:`Montage > Move </video_editing/edit/montage/move>` を参照してください。


   .. If the Active Tools option is enabled in Show Gizmo (see figure 1); you can also move the strip by dragging the gizmo.
   [Show Gizmo] で [Active Tools] オプションが有効になっている場合 (図 1 を参照)。ギズモをドラッグしてストリップを移動することもできます。

   .. The result of the Move operation is also visible in the Position X and Y fields of the strip Properties. Of course, you can also update these fields directly.
   移動操作の結果は、ストリップのプロパティの [位置 X] フィールドと [位置 Y] フィールドにも表示されます。もちろん、これらのフィールドを直接更新することもできます。

Rotate tool
   .. The shortcut for the Rotate-tool is :kbd:`R` (Grab). You can also click on the Rotate icon in the toolbar and start dragging (in a circle) the strip. A message appears beneath the menu: `Rotation: 0.0`; indicating the angle in degrees that the strip has been rotated. A positive number is a clockwise rotation; a negative number is counter-clockwise rotation. You can rotate more than 360° and also more than one strip at the same time. By default, the rotation is around the Median Point of the selected strips. You can change however the Pivot point (see figure 1).

   回転ツールのショートカットは :kbd:`R` (Grab) です。ツールバーの回転アイコンをクリックして、ストリップを (円を描くように) ドラッグし始めることもできます。メニューの下に次のメッセージが表示されます: Rotation: 0.0 これは、ストリップが回転された角度を度単位で示します。正の数は時計回りの回転です。負の数は反時計回りの回転です。360° 以上回転でき、同時に複数のストリップを回転することもできます。デフォルトでは、回転は選択したストリップの中点を中心に行われます。ただし、ピボット ポイントは変更できます (図 1 を参照)。

   .. The further away the mouse cursor is from the Pivot point, the slower the rotation movement is. So, to accomplish a very fast rotation (but difficult to fine-grain), place the mouse cursor very near the pivot point.

   マウス カーソルがピボット ポイントから離れるほど、回転の動きは遅くなります。したがって、非常に高速な回転を実現するには (ただし、細かい調整は困難です)、マウス カーソルをピボット ポイントのすぐ近くに置きます。

   .. As with the Move tool, you can constrain the rotation. Pressing :kbd:`Shift` while rotating will reduce the rotation increment; so that you can fine-tune the result (the result is also visible in the Rotation field of the strip Properties). To specify a specific rotation angle, enter a number after the :kbd:`R`. For example, `R-90` will rotate the strip 90° counter-clockwise. You can also use the Arrow-keys to move the Rotation handle horizontally or vertically.

   移動ツールと同様に、回転を制限できます。回転中に :kbd:`Shift` を押すと回転の増分が減少します。これにより、結果を微調整できます (結果はストリップのプロパティの [Rotation] フィールドにも表示されます)。特定の回転角度を指定するには、 :kbd:`R` の後に数値を入力します。たとえば、`R-90` はストリップを反時計回りに 90° 回転させます。矢印キーを使用して、回転ハンドルを水平または垂直に移動することもできます。

   .. If the Active Tools option is enabled in Show Gizmo (see figure 1); you can also rotate the strips by dragging the gizmo.
   [Show Gizmo] で [Active Tools] オプションが有効になっている場合 (図 1 を参照)。ギズモをドラッグしてストリップを回転することもできます。

Scale tool
   .. The shortcut for the Scale-tool is :kbd:`S` (Grab). You can also click on the Scale icon in the toolbar and start dragging along the X and/or (both is also possible) axis. The further away the mouse cursor is from the Pivot point, the smaller the scaling unit is and the more precise you can work. A message appears beneath the menu: `Scale X: 1.0000 Y:1.0000`. This means that the Scale tool uses the Local view. For example, you have scaled a strip already to 0.8. The second Scale operation will again start as size 1.0. So scaling the second time to 0.5, will scale the strip in absolute (global) terms to 0.4 or 40% of the original size. A number > 1 will scale the strip up; a number smaller than 1 will scale it down.

   スケールツールのショートカットは  :kbd:`S` (Grab) です。ツールバーの「スケール」アイコンをクリックして、X 軸および/または (両方も可能) 他の軸に沿ってドラッグを開始することもできます。マウス カーソルがピボット ポイントから離れるほど、スケーリング単位が小さくなり、より正確に作業できるようになります。メニューの下に「Scale X: 1.0000 Y:1.0000」というメッセージが表示されます。これは、スケール ツールがローカル ビューを使用することを意味します。たとえば、ストリップはすでに 0.8 にスケールされています。2 番目のスケール操作は再びサイズ 1.0 として開始されます。したがって、2 回目に 0.5 にスケーリングすると、ストリップは絶対 (グローバル) 単位で元のサイズの 0.4 または 40% にスケーリングされます。1より大きい数値を指定すると、ストリップが拡大されます。1 より小さい数値を指定するとスケールダウンされます。

   .. The scaling occurs with the Pivot point as reference. So, for example, if the Pivot point is set to 2D Cursor, scaling down a strip will also move the strip in the direction of the 2D cursor. s

   スケーリングはピボット ポイントを基準にして行われます。したがって、たとえば、Pivot Point が 2D カーソルに設定されている場合、ストリップを縮小すると、ストリップも 2D カーソルの方向に移動します。

   .. Pressing :kbd:`Shift` while scaling will reduce the scaling unit; so that you can fine-tune the result You can also use the Arrow-keys to move the Scale handle horizontally or vertically.

   スケーリング中に :kbd:`Shift` を押すと、スケーリング単位が減少します。これにより、結果を微調整できます。また、矢印キーを使用してスケール ハンドルを水平または垂直に移動することもできます。

   .. If the Active Tools option is enabled in Show Gizmo (see figure 1); you can also scale the strips by dragging the gizmo.

   [Show Gizmo] で [Active Tools] オプションが有効になっている場合 (図 1 を参照)。ギズモをドラッグしてストリップを拡大縮小することもできます。

Transform
   .. The Transform tool supports any combination of Grab, Rotate and Scale at the same time. In figure 2, the Transform tool is enabled and strip 3 selected.

   変形ツールは、グラブ、回転、スケールの任意の組み合わせを同時にサポートします。図3 では、変形ツールが有効になっており、ストリップ 3 が選択されています。

   .. figure:: /images/editors_vse_preview_toolbar_transform.png
      :alt: Transform Tool

      図3: 変形ツール

   .. With the four squares at the corners of the strip, you can scale the strip. The circle on top is for rotating and the crosshair in the middle is for moving the strip.

   ストリップの角にある 4 つの四角形を使用して、ストリップを拡大縮小できます。上部の円は回転用で、中央の十字はストリップの移動用です。

Sample
 .. The Sample tool (with the little eyedropper icon) can be used to sample a pixel's color. Be sure that the Sample Tool is selected (which is by default) and :kbd:`LMB - Click` anywhere in the Project Preview area. Information about the pixel under the mouse cursor appears in the status bar.

 Sampleツール (小さなスポイト アイコン付き) を使用して、ピクセルの色をサンプリングできます。Sampleツールを選択し (デフォルトで選択されている)、Preview 領域の任意の場所で :kbd:`LMB-Click` しましょう。マウスカーソルの下のピクセルに関する情報がステータス バーに表示されます。

 .. figure:: /images/editors_vse_preview_sample-tool.svg
  :alt: Sample Tool

  図4: Sample Tool in action

  .. The Preview window of figure 1 contains a simple Color strip with RGB values (0.8, 0.7, 0.4) or the equivalent HSV values (0.142, 0.5, 0.8). These values are set with the Color Picker. They are also shown in figure 1. :kbd:`LMB - Click` on the bottom-right corner of the Preview (position X = 1870 and Y = 79; see figure 2) will show a status bar, containing the following info:

  図4 のPreviewウィンドウには、RGB 値 (0.8, 0.7, 0.4) または同等の HSV 値 (0.142, 0.5, 0.8) を含む単純なカラーストリップが含まれています。これらの値はカラーピッカーで設定されます。これらは図4 にも示されています。プレビューの右下隅 (X = 1870 および Y = 79 の位置、図 2 を参照) には、次の情報を含むステータス バーが表示されます。

  .. * The X and Y coordinates of the clicked pixel. Remember that the left bottom corner is location (0,0) and that the project resolution is set to 1920 x 1080.
  .. * The values for the Red, Green, and Blue component as from the Color Picker.
  .. * The Alpha value of the pixel.
  .. * The Color Managed values of the Red, Green and Blue component or the color as you see in the Preview.
  .. * The Hue, Saturation, Value and Luminance equivalent values of the Color Managed values.
  * クリックされたピクセルの X 座標と Y 座標。左下隅が位置 (0,0) であり、プロジェクトの解像度が 1920 x 1080 に設定されていることを思い出してください
  * カラーピッカーからの赤、緑、青コンポーネントの値
  * ピクセルのアルファ値
  * Color Managed Values: 赤、緑、青、またはプレビューに表示される色
  * Color Managed Values に相当する 色相、彩度、明度、輝度

 .. The Color Managed values are the result of applying the View Transform function from the `Color Management panel <https://docs.blender.org/manual/en/latest/render/color_management.html>`_. For the Video Editing Workspace, this is by default the Standard View Transform. This Transform function does not change the display device color values.

 Color Managed Values は、`Color Management panel <https://docs.blender.org/manual/en/latest/render/color_management.html>`_ からビュー変換機能を適用した結果です。Video Editing Workspace の場合、これはデフォルトで標準ビュー変換です。この変換関数は、表示デバイスの色の値を変更しません。

 .. note::
   .. If your colors look a bit "washed" out, then better check the `View Transform function <https://docs.blender.org/manual/en/latest/render/color_management.html>`_. If you started your project from another workspace than the Video Editing Workspace, this function is set by default to Filmic. This Transform function does change your colors (makes them "washed out"). Luckily, the VSE resets the Transform function to Standard, but only if the first added strip is a movie or image. If you add, for example a Scene strip as the first strip, the Transform function will not be changed.

   色が少し「色あせて」見える場合は、
   `View Transform function <https://docs.blender.org/manual/en/latest/render/color_management.html>`_  を確認してください。Video Editing Workspace 以外のワークスペースからプロジェクトを開始した場合、この機能はデフォルトで Filmic に設定されます。この変換機能は色を変更します (色を「色褪せ」させます)。幸いなことに、VSE は変換機能を標準にリセットしますが、これは最初に追加されたストリップがムービーまたは画像の場合に限ります。たとえばシーン ストリップを最初のストリップとして追加した場合、トランスフォーム機能は変更されません。


 .. todo::
   .. Reference to the color management section or short explanation about RGB --> HSV conversion and/or transform function.
   カラー管理セクションへの参照、または RGB -> HSV 変換および/または変換関数に関する簡単な説明。



:ref:`Annotate <tool-annotate>`
   .. With the Annotate tool, you can draw free-hand annotations onto the Preview window (thus, also outside the Project Preview area). This is a handy tool to give some instructions if you are working in team on a project (or to your later self). These annotations are saved with the Blend-file.

   Annotate ツールを使用すると、Previewウィンドウ (つまり、プロジェクト Preview領域の外にも) にフリーハンドの注釈を描画できます。これは、チームでプロジェクトに取り組んでいる場合に (または後の自分に) 指示を与えるのに便利なツールです。これらの注釈は Blend ファイルとともに保存されます。

   .. The Annotations and its Settings are stored in the :ref:`Annotations panel <annotations>` in the Side bar. To remove all annotations, just click on the Unlink button.

   注釈とその設定は、サイドバーの :ref:`Annotations panel <annotations>` に保存されます。すべての注釈を削除するには、[Unlink]ボタンをクリックするだけです。

   .. More information about the Annotate tool can be found in the :ref:`User Interface section <tool-annotate>` of the docs.

   Annotateツールの詳細については、ドキュメントの :ref:`User Interface section <tool-annotate>` セクションを参照してください。



.. rubric:: 脚注

.. [#f1] (訳注) Blender4.0では、最上位チャンネルのストリップが最初に選択され、次に下のチャンネルが選択されるようです。
