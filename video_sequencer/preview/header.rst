Header
------
.. figure:: /images/editors_vse_preview_header.svg
   :alt: Header of Preview


   図1: PreviewウィンドウのHeader

.. The Type Selector buttons are identical to those of the Sequencer header. The menu bar is limited to a stripped-down View menu. The Show Overlay button gets the company of the Display buttons (far right) and the Pivot Point in the middle. For more general info about the Type Selectors, see :doc:`Sequencer header <../sequencer/header>`

Type Selectorボタンは、SequencerのHeaderのボタンと同じです。メニューバーは、必要最低限の機能を備えた [View] メニューに限定されています。
[Show Overlay] ボタンは、表示系ボタングループの右端にあり、中央に[Pivot Point]ボタンがある。Type Selectorに関する一般的な情報については、:doc:`Sequencer header <../sequencer/header>` を参照してください。

.. View Menu
Viewメニュー
.........

.. figure:: /images/editors_vse_preview_view-menu.png
   :alt: View menu of Preview


   図2: PreviewウィンドウのViewメニュー

Sidebar - Toolbar
   .. See :doc:`Sequencer header <../sequencer/header>` for more info.
   詳細は :doc:`Sequencer header <../sequencer/header>` を参照

Preview During Transform
   .. With this option disabled, dragging the left or right strip handle will extend or reduce the strip length but the current frame in the preview does not change. In other words, the image in the preview does not change during dragging. With the option enabled however, dragging the strip handles will show the frame the strip handle is pointing to in the Preview window. The current frame is temporarily disabled. This will allow very precise trimming.
   このオプションを無効にすると、左または右のストリップ ハンドルをドラッグするとストリップの長さが延長または短縮されますが、Preview 内の現在のフレームは変更されません。つまり、ドラッグ中にPreviewの画像は変化しません。ただし、このオプションを有効にすると、ストリップ ハンドルをドラッグすると、ストリップ ハンドルが指しているフレームがPreviewウィンドウに表示されます。現在のフレームは一時的に無効になります。これにより、非常に正確なトリミングが可能になります。
Fit Preview in Window :kbd:`Home`
   .. Resize the Preview window so that the Project Dimensions area it fits in. Depending on the specific rendered image, the height or the width or both are set equal to the project height or width.
   プロジェクトのサイズに収まるようにPreviewウィンドウのサイズを変更します。特定のレンダリングイメージに応じて、高さまたは幅、またはその両方がプロジェクトの高さまたは幅と等しく設定されます。
Zoom :kbd:`Shift-B`
   .. Click and drag to draw a rectangle and zoom to this rectangle. The selected area is centered in the window and the Preview is zoomed with a factor size preview window/ size selected rectangle. This is normally a zoom in, but you can also drag a rectangle selection that is larger than the Preview window (by starting outside the window; resulting in a zoom out.
   クリックとドラッグして矩形選択し、この矩形の範囲にズームします。選択した領域がウィンドウの中央に配置され、プレビューは `Previewウィンドウ / 選択された矩形サイズ の倍率` でズームされます。通常、これはズームインですが、Previewウィンドウより大きい四角形の選択範囲をドラッグすることもできます (ウィンドウの外側から開始すると、ズームアウトになります)。
Fractional Zoom
   .. Resize the preview (project area) in steps from 1:8 to 8:1 (see figure 1). Suppose that the Project Dimensions are: 640 x 640. A fractional zoom of 1:1 (:kbd:`Numpad - 1`) will resize the project area (see :ref:`Figure 1: Preview Areas <preview-areas>` so that it will cover exactly 640 x 640 pixels in the preview window. If the Preview window is very small, the image will extend beyond the borders. A fractional zoom of 1:2 (1 divided by 2) indicates that the original 640 x 640 will be reduced to half or 320 x 320 pixels. A fractional zoom of 2:1 will double the Project area.
   Preview (プロジェクト領域) のサイズを 1:8 から 8:1 までの段階で変更します (図 1 を参照)。
   プロジェクトのサイズが 640 x 640 であるとします。 1:1 の分数ズーム (:kbd:`Numpad-1` ) により、プロジェクト領域のサイズが変更されます (:ref:`図1: Preview領域 <preview-areas>`)。そして、Previewウィンドウで正確に 640 x 640 ピクセルをカバーするようにします。
   Previewウィンドウが非常に小さい場合、画像は境界線を越えて広がります。 1:2 (1 を 2 で割った) の分数ズームは、元の 640 x 640 が半分の 320 x 320 ピクセルに縮小されることを示します。 2:1 の分数ズームでは、プロジェクト領域が 2 倍になります。
Zoom to Fit
   .. The command Zoom to Fit adjusts the largest side of the Preview so that its fits perfectly within the Preview window; e.g. has the same length as the largest side of the Preview window.
   [Zoom to Fit]コマンドは、Previewウィンドウ内に完全に収まるようにプレビューの最大の辺を調整します。たとえば、プレビューの最大の編は、Previewウィンドウの最大の辺と同じ長さになります。

Ctrl-Spacebar
   .. The :kbd:`Ctrl-Spacebar` key will switch the window under the mouse cursor; eg. the Preview, into semi-full view. The header and menus are still visible. At the very top, there is a button "Back to Previous". Pressing :kbd:`Ctrl-Spacebar` again or the Back to Previous button will restore the window. You can invoke this command from the menu: View > Area > Toggle Maximize Area.
   :kbd:`Ctrl-Spacebar` キーを押すと、マウスカーソルの下のウィンドウが切り替わります。例えば。プレビューをセミフル表示にします。Headerとメニューは引き続き表示されます。一番上に [Back to Previous]ボタンがあります。もう一度 :kbd:`Ctrl-Spacebar` を押すか、「Back to Previous」ボタンを押すと、ウィンドウが復元されます。このコマンドはメニューから呼び出すことができます: [View ] > [Area] > [Toggle Maximize Area]

Alt-Ctrl-Spacebar
   .. The :kbd:`Alt-Ctrl-Spacebar` key will switch the window under the mouse cursor into full view. All the available screen space is reserved for the Preview. To restore the window, you need to press :kbd:`Alt-Ctrl-Spacebar` again. *No other key or menu will do! There even isn't the small pop-up in the left top corner as in other maximized windows* You can invoke this command from the menu: View > Area > Toggle FullScreen Area.
   :kbd:`Alt-Ctrl-Spacebar` キーを押すと、マウス カーソルの下にあるウィンドウが全体表示に切り替わります。利用可能な画面スペースはすべてPreview用に確保されます。ウィンドウを元に戻すには、もう一度 :kbd:`Alt-Ctrl-Spacebar` 押す必要があります。他のキーやメニューは機能しません。他の最大化されたウィンドウのように、左上隅に小さなポップアップさえありません。メニューからこのコマンドを呼び出すことができます: [View] > [Area] > [Toogle FullScreen Area]。

   .. This command can also be useful if you run a dual monitor setup, but you'll first have to add a shortcut to ctrl+alt+space ex. shift+ctrl+alt+space, then you select Window > New Window, move it to the 2. monitor and then hit shift+ctrl+alt+space(windowless) & ctrl+alt+space(headerless fullscreen).
   このコマンドは、デュアル モニター セットアップを実行する場合にも役立ちますが、
   最初にOSのウィンドウ最大表示化のショートカット(例: shift+ctrl+alt+space [#f1]_)を追加しておくと、[Window] > [New Window] を実行し、作成したウィンドウをセカンドモニターに移動した後に、 shift+ctrl+alt+space キーでOSのウィンドウ最大表示、および ctrl+alt+spaceキーでBlenderのヘッダーなしの全画面表示を行えます。

Show Cache, Sequence Render Image, Sequence Render Animation, Export Subtitles
   .. * Rendering is described in section Video Editing > Render.
   .. * Subtitles are described in Video Editing > Edit > Sound.
   * レンダリングについては、:doc:`Video Editing > Render </video_editing/render/index>` セクションを参照
   * 字幕については :doc:`Video Editing > Rendering > Postprocessing </video_editing/render/postprocessing/subtitles/subtitles>` を参照

.. todo::
   .. Add links to those sections
   それらのセクションへのリンクを追加する (subtitlesの記載がない)

Toggle Sequencer/Preview :kbd:`Ctrl-Tab`
   .. Switch the editor display type between Sequencer and Preview.
   エディターの表示タイプを Sequencer と Preview の間で切り替えます。

Pivot Point
...........

.. figure:: /images/editors_vse_preview_header_pivot-point.png
   :alt: Pivot Point options
   :scale: 40%
   :align: right


   図3: Pivot Pointオプション


.. The Pivot Point is primarily used in operations such as Rotate and Scale. It defines the point around which the strip image will be rotated or scaled. Using this selector in the header of the Preview, you can change the location of the pivot point.

Pivot Point は主に、回転やスケールなどの操作で使用されます。これは、ストリップイメージを回転または拡大縮小する基準となる点を定義します。
PreviewのHeaderでこのセレクターを使用すると、Pivot Pointの位置を変更できます。

.. The Pivot Point is also extensively used in the 3D Viewport; see `Editors > 3D Viewport <https://docs.blender.org/manual/en/dev/editors/3dview/controls/pivot_point>`_.
Pivot Pintは 3D Viewport でも広く使用されています。参照 `Editors > 3D Viewport <https://docs.blender.org/manual/en/dev/editors/3dview/controls/pivot_point>`_

Bounding Box center
   .. The bounding box is a rectangular box that is wrapped as tightly as possible around the selection.
   Bounding Boxは、選択範囲をできるだけしっかりと囲む長方形のボックスです。
Median Point
   .. The Median Point is the points that is closest to *all* the origins of the selected strips. You can think of it as the midpoint of the area that is covered with the selected strips.
   Median Pointは、選択したストリップのすべての原点に最も近い点です。これは、選択したストリップでカバーされる領域の中点と考えることができます。

2D cursor
   .. Sometimes you want to rotate a strip around a specific point in the Preview. Therefore, you can set the 2D Cursor (with the Toolbar) and change the Pivot Point accordingly.
   プレビュー内の特定の点を中心にストリップを回転させたい場合があります。その場合、(ツールバーを使用して) 2D Cursor を設定し、それに応じてピボット ポイントを変更できます。
Individual origins
   .. If multiple strips are selected, you may want to rotate or scale these strips around there own origins instead of for example the Median Point of all selected strips. For example, if you have three portrait strip^s of faces, you probably want each face to be rotated around its individual origin.
   複数のストリップが選択されている場合、選択したすべてのストリップの中点などの代わりに、ストリップ自身の原点を中心に、回転または拡大縮小することができます。たとえば、顔のポートレート ストリップが 3 つある場合、おそらく各顔をそれぞれの原点を中心に回転させる必要があるでしょう。

Display Mode
............

.. With the Display Mode button, you can choose between a (default) Image Preview or a Luma Waveform, a Chroma Vectorscope or a Histogram view of the rendered image at the current frame.

[Display Mode] ボタンを使用すると、現在のフレームでレンダリングされたイメージを、Image Preview(default)、Luma Waveform、Chroma Vectorscope、または Histgram ビューのどちらで表示するかを選択できます。

Image Preview
   .. The Image Preview mode shows you what the resulting video will look like when rendered. This is the default working mode.
   Image Preview モードでは、レンダリングされた動画がどのように見えるかを確認できます。これはデフォルトの動作モードです。
Luma Waveform
  .. The Luma Waveform is the graphical representation of the luminosity or brightness of an image or video. For more detailed information about how to use this tool, see section on Color Grading. The examples below are very stylized to explain the basic principles and are not representative for real-world images.

 Luma Waveformは、画像または動画の輝度(luminosity)または明るさ(brightness)をグラフで表現したものです。このツールの使用方法の詳細については、カラー グレーディングのセクションを参照してください。以下の例は、基本原理を説明するために非常に様式化されており、現実世界の画像を表すものではありません。

 .. figure:: /images/editors_vse_preview_luma-waveform.svg
   :alt: Luma Waveform

   図4: Luma Waveform と Image preview

   .. Figure 4 shows two Preview windows: the left one with Display Mode Luma Waveform, the right one with the default display Mode Image Preview. The image is composed of 4 columns with several areas of grey-scale. The last column also contains the white text "50%".

   図 4 は 2 つの Preview ウィンドウを示しています。左側は表示モード Luma Waveform、右側はデフォルトの表示モードである Image Preview です。この画像はいくつかのグレースケール領域を含む 4 つの列で構成されています。最後の列にも白い文字「50%」が含まれています。

   .. The X-axis of the Luma Waveform represents the X-axis of the image. If the image is 400 pixels wide, so is the Luma Waveform. Although you cannot recognize individual shapes  of the image  (e.g. faces, ...) in the Luma Waveform, the 4 columns are discernible in this example because they vary widely in luminosity. The Y-axis of the Luma Waveform represents luminosity, ranging from zero (black) at the bottom to 1 (white) at the top. There are a few preset values (the red lines) at 0.1, 0.7 and 0.9.

   Luma Waveform の X 軸は画像の X 軸を表します。画像の幅が 400 ピクセルの場合、Luma Waveform も幅 400 ピクセルになります。Luma Waveform では画像の個々の形状 (顔など) を認識することはできませんが、この例では 4 つの列は明度が大きく異なるため、識別できます。Luma Waveformの Y 軸は、下部の 0 (黒) から上部の 1 (白) までの範囲の明るさを表します。0.1、0.7、0.9 にプリセット値 (赤線) があります。


   .. The first column in the image has a RGB-value (0.3, 0.3, 0.3), which is a 70% grey. This is shown by the small white line at (a). For a given position X at the horizontal axis, all the pixels in the vertical axis have the same luminosity value of 0.3. This is the interpretation of the single, small white line for the first 100 X-pixels in the Luma Waveform.

   画像の最初の列の RGB 値 (0.3、0.3、0.3) は 70% グレーです。これは (a) の小さな白い線で示されています。水平軸の特定の位置 X について、垂直軸のすべてのピクセルは同じ輝度値 0.3 を持ちます。これが、Luma Waveformの 最初の水平方向の100ピクセルの1本の小さな白い線の意味です。


   .. The second column contains three small white lines at level 0.2 (d), 0.6 (b) and 0.8 (c). For a given position X (ranging from pixel 100 - 199), there are only three luminosity values, corresponding to the three squares in the image.

   2 番目の列には、レベル 0.2 (d)、0.6 (b)、および 0.8 (c) の 3 本の小さな白い線が含まれています。特定の位置 X (ピクセル 100 ～ 199 の範囲) については、画像内の 3 つの正方形に対応する 3 つの明度値のみが存在します。

   .. The third column in the image is a gradient, ranging from black to white. So, for every position X in the range 300-399, there are multiple luminosity values, ranging from black (0) to white (1) and resulting in multiple white lines.   ,  The luminance values for respectively (c), (d) and (e) are 0.8, 0.6 and 0.2. Because the second column contains only those 3 luminance values, the Luma Waveform shows only three small (white) lines at the values 0.8, 0.6 and 0.2.

   画像の 3 列目は黒から白までのグラデーションです。したがって、300 ～ 399 の範囲内のすべての位置 X には、黒 (0) から白 (1) までの範囲の複数の明度値があり、結果として複数の白い線が生じます。

   .. The fourth column has a background of 50% grey, resulting in a single white line at level 0.5. The "point-cloud" above the 0.5 luminosity is caused by the anti-aliased white text (50%). Some X positions (right in the middle of the column) have multiple luminosity values: 0.5 from the background and several from the white, anti-aliased text. These values are all above 0.5 because the text is white and is merged with the 50% grey background.

   4 番目の列の背景は 50% グレーで、レベル 0.5 で 1 本の白い線が表示されます。明度 0.5 を超える「点の集まり」は、アンチエイリアス処理された白いテキスト (50%) によって発生します。一部の X 位置 (列の真中) には複数の明度値があります。背景からの 0.5 と、白いアンチエイリアス処理されたテキストからの値です。テキストが白で 50% の灰色の背景とマージされているため、これらの値はすべて 0.5 を超えています。

   .. With the sample tool you can determine the Luminosity value and other color values of every pixel in the image. Select the Sample tool and :kbd:`LMB-Click` on the image will show this info in the status bar. In figure 4, I've clicked on area (d). In the status bar, you can read the L-value: 0.2.

   サンプル ツールを使用すると、画像内のすべてのピクセルの輝度値とその他の色の値を確認できます。サンプル ツールを選択すると、画像上のステータス バーにこの情報が表示されます。図4 では、領域 (d) をクリックしました。ステータス バーで、L 値: 0.2 を読み取ることができます。

Chroma Vectorscope
  .. The Chroma Vectorscope is a graphical representation of the Hue and Saturation x Brightness values of an image. The three primary colors (red, green, blue) and the three secondary colors (yellow, cyan, magenta) and the in-betweens are visualized as a hexagon with the aforementioned colors at the vertices.  The center of the hexagon (the red dot) has a saturation x Brightness value of zero (because one or both  are zero, the Hue equals Black). The values at the border have a Saturation x Brightness value of 1. Every dot within the hexagon represent a pixel or a group of pixels with the same hue and saturation x Brightness value. A very dim or desaturated image for example will appear as group of dots near the center. An image with a very saturated (blue) sky, will show show as a bunch of dots near the blue border.

  Chroma Vectorscopeは、画像の色相(Hue)および彩度(Saturation) x 明るさ(Brightness)の値をグラフィカルに表現したものです。3 つのプライマ色 (赤、緑、青) と 3 つのセカンダリ色 (イエロー、シアン、マゼンタ)、およびそれらの間の色は、頂点に前述の色を持つ六角形として視覚化されます。六角形の中心 (赤い点) の彩度 x 明度の値は 0 です (一方または両方が 0 であるため、色相は黒と等しくなります)。境界線の値の彩度 x 明るさの値は 1 です。六角形内の各ドットは、同じ色相と彩度 x 明るさの値を持つピクセルまたはピクセルのグループを表します。たとえば、非常に薄暗い画像や彩度の低い画像は、中心近くの点のグループとして表示されます。非常に飽和した (青い) 空を持つ画像は、青い境界線の近くに点の束として表示されます。

  .. figure:: /images/editors_vse_preview_vectorscope.svg
    :alt: Display Mode Histogram

    図4: Chroma Vectorscope と Image Preview

  .. Figure 4 contains 14 different hue and Saturation x Brighness values. Each of them is represented by a small dot. The number of pixels with that particular value does not matter. For example, the small rectangles (e) and (f)  are equally represented by one (small) dot as the larger rectangles (a), ...
  図 4 には、14 の異なる色相と彩度 x 明度の値が含まれています。それぞれは小さな点で表されます。その特定の値を持つピクセルの数は重要ではありません。たとえば、小さな長方形 (e) と (f) は、大きな長方形 (a) と同様に 1 つの (小さな) ドットで表されます。

  .. Because the rectangles (a), (b), (c), and (d) have all the same (blue-ish) Hue, but a different Saturation x Brightness value, they lie at a line pointing to that Hue at the hexagon border.
  長方形 (a)、(b)、(c)、および (d) はすべて同じ (青っぽい) 色相を持ちますが、彩度 x 明るさの値が異なるため、六角形のその色相(blue)を指す線上に位置します。

Histogram
 .. The histogram is a graph that visualizes the intensity of the Red, Green and Blue component of a image.
   The X-axis of the histogram ranges from 0 to 1, which are the acceptable intensity values in a display color space. The Y-axis is a quantity measure: how many pixels have this specific Red, Green or Blue intensity.
 ヒストグラムは、画像の赤、緑、青の成分の強度を視覚化するグラフです。ヒストグラムの X 軸の範囲は 0 から 1 で、これは表示色空間で許容される強度値です。Y 軸は量の尺度であり、この特定の赤、緑、または青の強度を持つピクセルがいくつあるかを表します。

 .. figure:: /images/editors_vse_preview_histogram.svg
   :alt: Display Mode Histogram


 図5: Histogram と Image preview

 .. In figure 4, the rendered image is made up of three rectangles.
 図 4 では、レンダリングされたイメージは 3 つの長方形で構成されています。

 .. * (a) green RGB(0.2, 0.5, 0.4): 1/8 of the image size
 .. * (b) purple RGB (0.7, 0.6, 0.9): a quarter of the image size
 .. * (c) red RGB (0.8, 0.2, 0.3): half of the image size
 - (a\) 緑 RGB(0.2, 0.5, 0.4)：画像サイズの1/8
 - (b\) 紫 RGB(0.7, 0.6, 0.9)：画像サイズの1/4
 - (c\) 赤 RGB(0.8, 0.2, 0.3): 画像サイズの半分

 .. So, there are 9 RGB components, but only 8 of them are different (the value 0.2 occurs two times). Because rectangle (c) contains half of all pixels in the image, the histogram bars are about 0.5 high and they are drawn at X-location 0.2, 0.3 and 0.8. Rectangle (b) is half the size of (c), and so are the histogram bars. They are drawn at location 0.6, 0.7 and 0.9. Rectangle (a) has one RGB component value in common with rectangle (c). The Red component of (a) is drawn on top of the Green component (c), which results in a yellow bar at postion 0.2.

 つまり、RGB コンポーネントは 9 つありますが、そのうち 8 つだけが異なります (値 0.2 が 2 回出現します)。長方形 (c) にはイメージ内のすべてのピクセルの半分が含まれているため、ヒストグラム バーの高さは約 0.5 で、X 位置 0.2、0.3、および 0.8 に描画されます。長方形 (b) は (c) の半分のサイズであり、ヒストグラム バーも同様です。これらは位置 0.6、0.7、0.9 に描画されます。長方形 (a) には、長方形 (c) と共通の 1 つの RGB コンポーネント値があります。(a) の赤コンポーネントが緑コンポーネント (c) の上に描画され、位置 0.2 に黄色のバーが表示されます。

 .. Finally, there is the transparent area (1/8 of the image size). This is represented by a black color RGB (0,0,0), resulting in a white bar (red on top of green on top of blue) at location 0.

 最後に、透明領域 (画像サイズの 1/8) があります。これは黒色の RGB (0,0,0) で表され、位置 0 に白いバー (緑の上に赤、青の上に赤) が表示されます。

 .. You can always check the RGB value by selecting the Sample tool (default) and :kbd:`LMB-Click`/ In figure 5, you can verify that the RBB value of the red rectangle is indeed (0.8, 0.2, 0.3).
 サンプル ツール (デフォルト) を選択すると、いつでも RGB 値を確認できます。図 5 では、:kbd:`LMB-Click`で、赤い四角形の RBB 値が実際に (0.8, 0.2, 0.3) であることを確認できます。

Display Channels
................

.. You can choose between:
次の中から選択できます。

Color and Alpha
   .. Display preview image with transparency over checkerboard pattern.
   市松模様パターンの上に透明度のあるプレビュー イメージを表示します。
Color
   .. Ignore transparency of preview image (fully transparent areas will be black).
   プレビュー画像の透明度を無視します(完全に透明な領域は黒になります)。

Show Gizmo
..........
.. figure:: /images/editors_vse_header_preview-gizmo.png
   :alt: Show Gizmo
   :scale: 40%
   :align: right

   図6: Gizmoの表示

.. With Show Gizmo, you can display the Zoom and Move gizmos of the Preview window (the Hand and Magnifying glass; see :doc:`Gizmos <gizmos>` for more info. You can also enable the display of the Active Tools. These are the gizmos that appear around the selected strips when activating a specific tool (e.g. Move, Scale, Rotate).

[Show Gizmo] を使用すると、Previewウィンドウのズームと移動のギズモ [#f2]_ (手と虫眼鏡。詳細については :doc:`Gizmos <gizmos>` を参照) を表示できます。
また、アクティブツールの表示を有効にすることもできます。特定のツール（移動、拡大縮小、回転など）をアクティブ化時に、これらは選択したストリップの周囲に表示されるギズモです。


.. This setting is global for all scenes.
この設定はすべてのシーンにグローバルです。

Show Overlay
............

.. Overlays consist of additional information that is displayed on top of the preview region. With the Show Overlay button, you can switch off or on all overlays for the preview region. With the Overlays button (down pointing arrow) you can chose the type of Overlay: Frame Overlay, Safe Areas, Metadata or annotations. The following Overlays are available.

オーバーレイは、プレビュー領域の上に表示される追加情報で構成されます。[Show Overlay] ボタンを使用すると、Preview領域のすべてのオーバーレイをオフまたはオンに切り替えることができます。
[Overlays] ボタン (下向き矢印) を使用して、オーバーレイのタイプ (Frame Overlay, Safe Areas, Metadata および annotations) を選択できます。以下のオーバーレイが利用可能です。

.. More info about the available options are described in :doc:`Section Frame Overlay </video_sequencer/preview/sidebar>`.
利用可能なオプションの詳細については、 :doc:`Section Frame Overlay </video_sequencer/preview/sidebar>` を参照してください。

.. rubric:: 脚注

.. [#f1] (訳注) 意味を理解できなかったので勝手に解釈しました。誤訳の可能性があります。セカンドモニター用にOSのウィンドウ最大表示のショートカット(例: shift+ctrl+alt+space)を導入する意味と解釈しました。ただ、このショートカットの導入が便利かどうか、よくわかりません。

.. [#f2] (訳注) Gizmo は小道具、ガジェットといった意味のようです。Blenderでは、Toolbarのツールではなく、画面に常に表示できるボタンや情報をギズモと呼ぶようです。
