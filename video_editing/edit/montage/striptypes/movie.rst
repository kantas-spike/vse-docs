.. _bpy.types.MovieSequence:

***********
ムービーストリップ
***********

.. The input source of a movie strip is a video file with extension
.. (see `Video formats <https://docs.blender.org/manual/en/dev/files/media/video_formats.html>`_).

ムービー ストリップの入力ソースは、拡張子が以下のビデオファイルです。(参照 `Video formats <https://docs.blender.org/manual/en/dev/files/media/video_formats.html>`_)

``.mp4``, ``.mpg``, ``.mpeg``, ``.dvd``, ``.vob``,  ``.avi``, ``.mov``, ``.dv``, ``.ogg``, ``.ogv``, ``.mkv``, ``.flv``, ``.webm``

..
  Blender uses the ffmpeg library to process the video files.
  Which codecs are available depends on the operating system and ffmpeg version.
  The :ref:`default <default-color>` color of the movie strip bar is: :movie:`███`
..

Blender は ffmpeg ライブラリを使用してビデオ ファイルを処理します。
どのコーデックが利用できるかは、オペレーティング システムと ffmpeg のバージョンによって異なります。
ムービー ストリップ バーのデフォルトの色は次のとおりです: :movie:`███`

..
  Each video file contains a sequence of image frames (the actual movie)
  and some meta-information such as resolution.
  The resolution and framerate (fps or frame per seconds) info is exposed in the source-panel_.
..

各ビデオ ファイルには、一連の画像フレーム (実際のムービー) と解像度などのメタ情報が含まれています。
解像度とフレームレート (fps または 1 秒あたりのフレーム数) の情報は、source-panel_ で公開されます。

.. warning::
  ..
   The Project Settings parameters should preferably be the same as the strip parameters.
   For example, if the project is set to a frame rate of 30 fps, and your clip is only 24 fps,
   then the clip will appear accelerated.
   Thirty frames mean 1 second, according to the Project Settings; according to the project settings.
   But, these 30 frames cover 1.2 s in the original footage (30 x 24 fps = 1.2 s).
   Compressing 1.2s in 1s during playback will induce acceleration.

   Also, if your clip has variable framerate; e.g. footage from some smartphones,
   then you'll get an audio sync problem because Blender uses a constant frame rate.
   To solve this, you have to convert your clip to a constant frame rate with programs as
   `ffmpeg <https://ffmpeg.org/>`_ or `Handbrake <https://handbrake.fr/>`_
  ..

  プロジェクト設定パラメータは、ストリップパラメータと同じであることが望ましいです。
  たとえば、プロジェクトのフレーム レートが 30 fps に設定されているのに、
  クリップが 24 fps しかない場合、クリップは速い再生速度で表示されます。
  プロジェクト設定によれば、30 フレームは 1 秒を意味します。
  ただし、これらの 30 フレームは、元の映像の 1.2 秒をカバーします (30 / 24 fps = 1.2 秒)。
  再生中に 1.2 秒を 1 秒に圧縮すると再生速度を速めます。

  また、クリップが可変フレームレートの場合も同様です。
  たとえば、一部のスマートフォンからの映像の場合、
  Blender は一定のフレーム レートを使用するため、
  オーディオ同期の問題が発生します。
  これを解決するには、 `ffmpeg <https://ffmpeg.org/>`_ や `Handbrake <https://handbrake.fr/>`_ などのプログラムを使用して
  クリップを一定のフレーム レートに変換する必要があります。



Options
=======

..
  The movie strip is a much-used strip type and has lots of properties.
  They are organized in panels in the `sidebar <https://docs.blender.org/manual/en/dev/interface/window_system/regions.html>`_.
..

ムービー ストリップはよく使用されるストリップ タイプであり、多くのプロパティがあります。これらは `sidebar <https://docs.blender.org/manual/en/dev/interface/window_system/regions.html>`_ のパネルに整理されています。



.. _compositing-panel:

Compositing
-----------

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Compositing
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-compositing.png
   :scale: 50 %
   :alt: Compositing property
   :align: Right

   図 1: Compositing パネル

.. In the Compositing panel you can set the properties `Blend` and `Opacity` (see figure 1).
[Compositing] パネルでは、 `Blend` と `Opacity` のプロパティを設定できます(図 1)。

Blend
   .. When two strips are placed on top of each other, the strip of the higher channel completely covers the strip below, even if it is much smaller. In the Preview Window you will only see the strip from the higher channel; for example, you can safely delete the strip below without noticing anything.

   2 つのストリップを重ねて配置すると、たとえそれがはるかに小さかったとしても、高いチャンネルのストリップが下のストリップを完全に覆います。
   Preview ウィンドウには、上位チャンネルのストリップのみが表示されます。たとえば、下にあるストリップは何も気付かずに安全に削除できます。

   .. This is because the Blend Mode of the higher channel strip is set to ``Cross``. This is the default value for all strips; except the Text strip which has a default value of ``Alpha Over``.

   これは、上位チャンネル ストリップのブレンド モードが ``Cross`` に設定されているためです。
   これはすべてのストリップのデフォルト値です。ただし、デフォルト値が ``Alpha Over`` のテキスト ストリップは除きます。

   .. The Blend mode of a strip specifies how the strip immediately below should combine or blend with it. There are 27 blend modes, such as ``Color Dodge`` or ``Alpha Over``. They all have unique and sometimes subtle effects. For example, the ``Cross`` and ``Replace`` blend mode seems on first sight exactly the same. The higher channel strip replaces completely the lower channel strip. However, in combination with an Opacity value of zero (see below), both Blend modes have completely different results.

   ストリップのブレンド モードは、すぐ下のストリップがどのように結合またはブレンドされるかを指定します。
   ``Color Dodge`` や ``Alpha Over`` など、27 のブレンド モードがあります。
   それらはすべてユニークで、時には微妙な効果を持っています。
   たとえば、 ``Cross`` と ``Replace`` ブレンド モードは一見するとまったく同じように見えます。
   高い方のチャンネルストリップは、低い方のチャンネルストリップを完全に置き換えます。
   ただし、不透明度値 0 (以下を参照) と組み合わせると、両方のブレンド モードでまったく異なる結果が得られます。

   .. - Blend mode = Replace + Opacity = 0 --> completely transparent Preview Window
   .. - Blend mode = Cross  + Opacity = 0 --> Preview Window filled with lower strip.
   - Blend mode = Replace + Opacity = 0 --> 完全に透明な Preview ウィンドウ
   - Blend mode = Cross  + Opacity = 0 --> Preview Window に下のストリップを表示

   .. todo::
      .. A detailed description of all blend modes will be available soon in chapter Edit > Color Grading.
      すべてのブレンド モードの詳細な説明は、「編集 > カラー グレーディング」の章で間もなく公開されます。

Opacity
   .. An opaque object is completely impervious to light. You cannot see through it. Opacity is the opposite of transparency. Each pixel in an image can have - besides the Red, Green and Blue values - also an Alpha value, a number between 0 and 1. An  Alpha = 0 indicates a completely transparent image. A completely opaque image has an Alpha = 1.

   不透明な物体は光をまったく通しません。それを通して見ることはできません。
   不透明度は透明度の反対です。画像内の各ピクセルは、赤、緑、青の値のほかに、0 から 1 までの数値であるアルファ値を持つことができます。
   アルファ = 0 は、完全に透明な画像を示します。完全に不透明なイメージのアルファ = 1 になります。

   .. hint::
      .. A simple mnemonic to remember these values: 0 is like a peeping hole = see through = transparent.
      これらの値を覚えておくための簡単なニーモニック: 0 はのぞき穴のような = シースルー = 透明です。

   .. The Alpha value of each pixel in the image is multiplied with the Opacity value of this field. A value of 1 does not affect the opacity of the strip. For example, if the strip is semi-transparent (e.g. alpha = 0.6), then it remains semi-transparent (0.6 x 1 = 0.6).
   .. A value of zero will make the strip fully transparent because multiplying with zero will always result in zero.
   .. See :doc:`Mask strips <mask>` for more details on transparency/opacity.

   画像内の各ピクセルのアルファ値は、このフィールドの不透明度値と乗算されます。
   値 1 はストリップの不透明度に影響しません。
   たとえば、ストリップが半透明（たとえば、アルファ = 0.6）の場合、半透明のままになります（0.6 x 1 = 0.6）。
   ゼロを乗算すると常にゼロになるため、値をゼロにするとストリップが完全に透明になります。
   透明度/不透明度の詳細については、 :doc:`Mask strips <mask>` を参照してください。


.. _transform-panel:

Transform
---------

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Transform
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-transform.png
   :scale: 50%
   :alt: Transform Property
   :align: Right

   図2: Transform パネル

.. The Transform panel contains the Position, Scale, and Rotation properties and the -perhaps less- important Mirror property.
Transform パネルには、Position、Scale、Rotation プロパティと、おそらくそれほど重要ではない Mirror プロパティが含まれています。

.. todo::
  .. Add a link to the Image Transform menu (Scale to Fit, Scale to Fill, ...).
  Image Transformメニューへのリンクを追加する


Position X, Y
  ..
   The dimensions of the view area of the sequencer output are set by the project dimensions;
   e.g. 1920 x 1080 by default (see :doc:`/video_editing/setup/directory-structure`).
   A movie is centered (and scaled) within this view area. So, position (0,0) wil refer to the midpoint of the image. With the X, Y values, you can move the frame along the horizontal and vertical axis. The values are expressed in pixels.
  ..
  シーケンサー出力の表示領域のサイズは、プロジェクトのサイズによって設定されます。
  たとえば、デフォルトでは 1920 x 1080 ( :doc:`/video_editing/setup/project-settings` を参照)。ムービーは、この表示領域内で中央に配置 (および拡大縮小) されます。
  したがって、位置 (0,0) は画像の中点を指します。X、Y の値を使用して、水平軸と垂直軸に沿ってフレームを移動できます。値はピクセル単位です。


Scale X, Y
  ..
   With this value, you can scale the image on the X (=horizontal) and Y (=vertical) axis. It is a number between 0 and infinity.
   A scale of 0.5 on the X axis for example will halve the width of the frame. A scale of 2 will double it.
   To scale the frame proportionally, you have to use the same value for X and Y.

   Scaling an image will by no means change the resolution of the image!
  ..
  この値を使用すると、X (= 水平) 軸と Y (= 垂直) 軸で画像を拡大縮小できます。
  0 から無限大までの数値です。たとえば、X 軸のスケールを 0.5 にすると、
  フレームの幅が半分になります。スケールを 2 にすると 2 倍になります。
  フレームを比例的に拡大縮小するには、X と Y に同じ値を使用する必要があります。

  画像を拡大縮小しても、画像の解像度は決して変わりません。

Rotation
  ..
   Rotates the frame along the Z axis; expressed in degrees.
   A negative value will rotate counter clockwise. This value can be > 360°, e.g. in animations,
   you can rotate a frame 3 times around its Z axis by entering the value 1080° = 3 x 360°.
  ..
  フレームを Z 軸に沿って回転します。度で表されます。
  負の値を指定すると反時計回りに回転します。この値は 360° を超えることができます。
  たとえば、アニメーションでは、値 1080° = 3 x 360° を入力すると、Z 軸を中心にフレームを 3 回回転できます。

Mirror
   .. Mirrors the image along the X axis (left to right) or the Y axis (top to bottom).
   X 軸 (左から右) または Y 軸 (上から下) に沿ってイメージをミラーリングします。

..
  Figure 3 shows an example of a Picture-in-Picture (PIP) setup. You need the Position, Scale, and Blend mode property to accomplish this. Figure 3 has three channels.
  Channel 1 contains the audio. Channels 2 forms the background.
  Channel 3 contains the foreground picture. This picture is scaled (0.3) and repositioned (717,300) to create a PIP.
..
図 3 は、ピクチャ イン ピクチャ (PIP) セットアップの例を示しています。
これを実現するには、Position、Scale、および Blend モードのプロパティが必要です。
図 3 には 3 つのチャネルがあります。チャンネル 1 にはオーディオが含まれます。
チャンネル 2 が背景を形成します。
チャンネル 3 には前景画像が含まれます。この画像は拡大縮小 (0.3) され、位置変更 (717,300) されて PIP が作成されます。

.. figure:: /images/vse_setup_project_striptypes_PIP-example.svg
   :alt: PIP example

   図 3: ピクチャー・イン・ピクチャーの例

..
  The "Spring" open-movie in figure 3 has non-default dimensions: 2048 x 858.
  To download this movie, see :doc:`creating test-files - section E) </video_editing/setup/creating-test-files>`.
  If you add this movie to the default FHD timeline (1920 x 1080), it will be scaled.
  The longest dimension (2048) will be scaled to 1920 with a factor of 0.9375 (0.9375 x 2048 = 1920).
  The vertical dimension too will be scaled with the same parameter,
  given a height of 858 * 0.9375 = 804, leaving two transparent bands above and below the video.
  In figure 3 we changed the project dimensions to equal
  the strip dimensions so that the viewport is fully taken by the video.
..
図 3 の「Spring」オープン ムービーのサイズはデフォルトではありません: 2048 x 858。このムービーをダウンロードするには、 `creating test-files - section E) </video_editing/setup/creating-test-files>`_ を参照してください。
このムービーをデフォルトの FHD タイムライン (1920 x 1080) に追加すると、スケーリングされます。
最長の寸法 (2048) は 0.9375 の係数で 1920 にスケーリングされます (0.9375 x 2048 = 1920)。
垂直方向の寸法も同じパラメータで拡大縮小され、高さ 858 * 0.9375 = 804 が指定され、
ビデオの上下に 2 つの透明なバンドが残ります。
図 3 では、ビューポートがビデオに完全に表示されるように、プロジェクトの dimensions をストリップの dimensions と等しくなるように変更しました。

..
  The foreground picture (from the same open-movie "Spring") is scaled with a factor of 0.3. This leads to the following pixel sizes: 2048 x 0.3 = 614 and 858 x 0.3 = 257.
  If you want to position this strip into the top-right corner, you have to change the X and Y position.
  But how much? The center of each picture is position (0,0).
  So, the background picture runs from bottom-left (-1024,-429) to top-right (1024, 429).
  To tuck the small picture in the top-right corner,
  you have to move it on the X-axis to position: 1024 - (614/2) = 717.
  And on the Y-axis to position 429 - (257/2) = 300.
..

前景の画像 (同じ公開映画「Spring」から) は 0.3 倍に拡大縮小されます。
これにより、ピクセル サイズは 2048 x 0.3 = 614 および 858 x 0.3 = 257 になります。
このストリップを右上隅に配置したい場合は、X と Y の位置を変更する必要があります。
しかし、いくらですか？各ピクチャの中心は位置 (0,0) です。したがって、背景画像は左下 (-1024、-429) から右上 (1024、429) まで続きます。
小さな画像を右上隅に押し込むには、X 軸上で 1024 - (614/2) = 717 の位置に移動する必要があります。
また、Y 軸上で 429 - (257/2) = 300 の位置に移動する必要があります。

.. _crop-panel:

Crop
----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Crop
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-crop.png
   :scale: 50%
   :alt: Crop Property
   :align: Right

   図 4: Crop パネル

.. Cropping is the removal of unwanted outer areas from an image.
Cropping とは、画像から不要な外側の領域を除去することです。

Left, Right, Top, Bottom
   .. The specified number of pixels are removed from the *Left*, *Right*, *Top* and/or *Bottom* of the image.
   And as such making this image smaller. Although you can specify a negative number, this does not affect the image.
   指定された数のピクセルが画像のLeft、Right、Topおよび/またはBottomから削除されます。
   したがって、この画像は小さくなります。負の数値を指定することもできますが、画像には影響しません。

..
  Crop and Scale are two very much different operations.
  Take a look at figure 5. Both small pictures have the same size.
  The left one is obtained by scaling to 0.3 of the original 2048 x 858 image,
  resulting in a picture of 614 x 257 pixels (see also figure 3).
  The picture on the right is obtained by cropping.
..

CropとScaleは、まったく異なる 2 つの操作です。
図 5 をご覧ください。両方の小さな画像は同じサイズです。
左側の画像は、元の 2048 x 858 イメージを 0.3 にスケールして、614 x 257 ピクセルの画像になります (図 3 も参照)。
右の写真はCropしたものです。

..
  The combined crop Left and Right should be equal to 2048 - 614 = 1434.
  By cropping 1434 pixels from the left and right (670 + 764), you'll get a resulting picture that is exactly 614 pixels wide.
  The combined crop Top and Bottom should be: 858 - 257 = 601 or 572 + 29. Of course,
  the exact ratio between Left/Right and Top/Bottom depends on the detail you want to have in focus.
  To center on the dog, we need the following crop sizes: Left (670), Right (734), Top (572), and Bottom (29).
  This will result in the exact same size but zoomed in.
..

LeftとRightのCropを組み合わせた値は、2048 - 614 = 1434 になるはずです。
左右から 1434 ピクセル (670 + 764) をCropすると、正確に 614 ピクセル幅の画像が得られます。
Cropの Top と Bottom を組み合わせた値は、858 - 257 = 601 または 572 + 29 である必要があります。
もちろん、Left/Right と Top/Bottom の正確な比率は、焦点を当てたいディテールによって異なります。
犬を中心にするには、次のトリミング サイズが必要です: Left (670)、Right (734)、Top (572)、Bottom (29)。
これにより、まったく同じサイズになりますが、拡大されます。


.. figure:: /images/vse_setup_project_striptypes_crop-vs-scale.svg
   :alt: Crop vs Scale

   図 5: Crop と Scale の例


.. _video-panel:

Video
-----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Video
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-video-strip-movie.png
   :scale: 50%
   :alt: Video Property
   :align: Right

   図6: Videoパネル

Strobe
  ..
    The Strobe value indicates that only each nth frame will be displayed. By default it's set to 1.
    For example, if you set this to 10, the preview will only display frame 1 for the range 1-10 frames,
    frame 11 for the range 11-20, frame 21 for ...
  ..
  Strobe 値は、各 n 番目のフレームのみが表示されることを示します。
  デフォルトでは 1 に設定されています。たとえば、これを 10 に設定すると、
  プレビューには 1 ～ 10 フレームの範囲ではフレーム 1 のみが表示され、11 ～ 20 の範囲ではフレーム 11 が表示され、...

  ..
    It is not really a strobe-effect because the frames 2-9,
    11-19, ... aren't blacked out.  You can easily check this out with the timecode overlay test file
    (see :doc:`Creating test files - section C </video_editing/setup/creating-test-files>`).
  ..
  フレーム 2 ～ 9、11 ～ 19 などは黒く塗りつぶされていないため、実際にはストロボ効果ではありません。
  これは、タイムコード オーバーレイ テスト ファイルを使用して簡単に確認できます (参照 :doc:`Creating test files - section C </video_editing/setup/creating-test-files>`)。

Reverse Frames
  ..
   The strip is played backwards starting from the last frame in the sequence to the first frame.
   This will also work with split strips. However, just pay attention to use the "Hold Split" (Shift + K) cut (see /edit/montage/splitting).
  ..
  ストリップは、シーケンスの最後のフレームから最初のフレームまで逆方向に再生されます。
  これは分割ストリップでも機能します。ただし、"Hold Split" (Shift + K) カットを使用することに注意してください (/edit/montage/splitting を参照)。

.. _color-panel:

Color
-----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Color
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-color.png
   :scale: 50%
   :alt: Color Property
   :align: Right

   図 7: Colorパネル

..
  The properties in this panel seem to be an easy shortcut for some effects or modifiers.
  The Saturation could be changed (for each color independent) with the Color Hue modifier.
  The Multiply property could be achieved with the Multiply effect and a color strip.
..
このパネルのプロパティは、一部のエフェクトやモディファイアの簡単なショートカットのようです。
[Saturation]は、Color Hue モディファイアを使用して (色ごとに独立して) 変更できます。 [Multiply] プロパティは、Multiply エフェクトとカラー ストリップを使用して実現できます。

Saturation
  ..
   Increases or decreases the color saturation or the vividness of an image.
   A saturation value of zero will turn the color image into a grey-scale image.
  ..
  画像の彩度や鮮やかさを増減します。彩度値を 0 にすると、カラー イメージがグレースケール イメージに変わります。

Multiply
  ..
   Multiplies the colors by this value. This will increases the brightness for values > 1.
   Using a value < 1 will reduce the brightness. A value of zero will produce a uniformly black image;
   the color code of black is RGB (0,0,0).
  ..
  色にこの値を乗算します。これにより、値が 1 より大きい場合は明るさが増加します。
  値が 1 より小さい場合は明るさが減少します。値をゼロにすると、均一な黒のイメージが生成されます。黒のカラーコードは RGB (0,0,0) です。

Convert to Float
   .. Converts the multiply value to a float data type.
   乗算値を float データ型に変換します。

.. todo::

   .. The Convert to Float does not seem to do anything.
   .. But see Stackexchange: https://blender.stackexchange.com/questions/57528/
   Convert to Float は何も行わないようです。
   ただし、Stackexchange: https://blender.stackexchange.com/questions/57528/ を参照してください


.. _time-panel:

Time
----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Time
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-time.png
   :scale: 50%
   :alt: Time Property
   :align: Right

   図8: Time パネル

..
  Most - but not all - of the available time codes can be updated in this panel.
  A general introduction of the Timeline and time codes can be found in :doc:`Timeline basics </video_sequencer/sequencer/timeline>`.
  A clear understanding of these time codes is essential in trimming and freezing clips.
..
すべてではありませんが、使用可能なタイム コードのほとんどをこのパネルで更新できます。
タイムラインとタイムコードの概要については、 :doc:`Timeline basics </video_sequencer/sequencer/timeline>` を参照してください。
クリップのトリミングやフリーズを行うには、これらのタイムコードを明確に理解することが不可欠です。

..
  A movie strip is a sequence of frames that is represented by a blue bar in the sequencer.
  To draw this movie strip you need a few properties: the Channel,
  the Start position in the timeline and some time codes of the movie strip.
..
ムービー ストリップは、シーケンサー内の青いバーで表される一連のフレームです。
このムービー ストリップを描画するには、チャンネル、タイムラインの開始位置、
ムービー ストリップのタイム コードなど、いくつかのプロパティが必要です。

.. |notequal| unicode:: 0x2260

Channel
  ..
   Strips are placed in channels; rows stacked upon each other (see for example figure 1 with 3 channels).
   Upon adding a movie clip, Blender searches for the next free channel at the position of the playhead to place the movie strip.
   With this property, you can change the channel number, e.g. the row number of the strip.
   If the channel is already taken by another strip, the strip will be positioned at the next higher available channel.
   The first channel 0 is unusable as a place to put strips.
   This is because it is used by the Sequencer Display to show a composite of all strips above channel 0.
   The maximum number of channels is 32.
  ..
  ストリップはチャンネルに配置されます。行が互いに積み重ねられています (たとえば、3 つのチャネルがある図3 を参照)。
  ムービークリップを追加すると、Blender は再生ヘッドの位置で次の空きチャンネルを検索し、ムービー ストリップを配置します。このプロパティを使用すると、チャネル番号を変更できます。チャンネルがすでに別のストリップによって使用されている場合、ストリップは次に高い利用可能なチャンネルに配置されます。
  最初のチャンネル 0 はストリップを配置する場所としては使用できません。
  これは、チャンネル 0 より上のすべてのストリップの合成を表示するためにシーケンサー ディスプレイによって使用されるためです。チャンネルの最大数は 32 です [#f1]_ 。

..
  To ease the understanding of these timecodes, you can imagine 4 markers on a movie strip.
  See figure 9 for some clarification.
..

これらのタイムコードを理解しやすくするために、ムービー ストリップ上の 4 つのマーカーを想像してください。説明については、図 9 を参照してください。

..
  - First accessible frame (FA): the first frame in the sequence that *could* be displayed;
    usually also the very first frame of the video.
  - First Visible (FV) frame: the first frame that is actually displayed in the preview.
    It marks also the beginning of the strip bar.
  - Last Visible (LV) frame: the last frame of the sequence that is displayed. The end of the blue bar.
  - Last Accessible (LA) frame: the last frame of the sequence that *could* be displayed.
..

- First accessible frame (FA): *表示できる* シーケンス内の最初のフレーム。通常はビデオの最初のフレームでもあります。
- First Visible (FV) frame: Preview に実際に表示される最初のフレーム。これはストリップ バーの始まりでもあります。
- Last Visible (LV) frame: 表示されるシーケンスの最後のフレーム。青いバーの端。
- Last Accessible (LA) frame: *表示できる* シーケンスの最後のフレーム。

Start
  ..
   This field specifies where the FA frame of the movie strip should be placed on the timeline.
   Upon adding a movie strip to the sequencer, the Start field is set to the value of the playhead.
   You can change it manually by entering a different frame number
   or by moving the strip to another position in the timeline.

   Right after adding FV= FA and LV = LA. Because of this, the movie seems to start at the Start position.
   This is however not always the case.
  ..
  このフィールドは、ムービー ストリップの FA フレームをタイムライン上のどこに配置するかを指定します。
  ムービー ストリップを Sequencer に追加すると、Start フィールドが再生ヘッドの値に設定されます。
  別のフレーム番号を入力するか、ストリップをタイムライン内の別の位置に移動することで、手動で変更できます。

  ストリップを追加した直後は、FV=FA、LV=LA になります。
  このため、ムービーは Start 位置から始まるように見えます。ただし、常にそうとは限りません。

Duration
  ..
   This field represents the actual duration; the length of the blue bar; or LV minus FV (see figure 9).
   You can change the Duration by entering a different value.
   A smaller value will shorten the strip (LV will be positioned earlier; see figure 9);
   a larger value will lengthen the strip by repeating the last frame. LV should become larger than LA?
   So, the Preview window has to display frames that aren't there?
   This problem is solved via two unexposed fields:
   *frame_still_start* and *frame_still_end* fields, accessible through the Python API (see further).
  ..

  このフィールドは実際の期間を表します。
  青いバーの長さ。または LV から FV を引いた値 (図 9 を参照)。
  別の値を入力すると、期間を変更できます。値が小さいほどストリップが短くなります (LV が前に配置されます。図 9 を参照)。
  値を大きくすると、最後のフレームが連動し、ストリップが長くなります。
  LVはLAより大きくなるはず？ そして、Previewウィンドウには存在しないフレームも表示する必要があるのでしょうか?
  この問題は、Python API を通じてアクセスできる2つの非公開フィールド、 *frame_still_start* フィールドと *frame_still_end* フィールドによって解決されます (詳細は Python APIを参照) [#f2]_ 。

End
  ..
   Specifies the actual ending or the Last Visible frame (LV) of the strip.
   This value cannot be edited and is the result of the calculation: Start + Duration - 1.
  ..
  ストリップの実際の終了または最後に表示されるフレーム (LV) を指定します。この値は編集できません。Start + Duration - 1 という計算の結果です。

Strip Offset Start
  ..
   With this value, you reposition the FV marker. It can be a positive or negative value.
   If positive, the actual start (FV) of the strip will be further in time.
   A few frames are skipped and the movie strip starts later (see figure 9).
   If negative, the FV frame should come before the FA frame (assuming FV = FA initially), which is impossible.
   As a result, the FA frame will be repeated (see the section on Hold Offset for an explanation).
  ..

  この値を使用して、FV マーカーの位置を変更します。正の値または負の値を指定できます。正の場合、ストリップの実際の開始 (FV) はさらに後になります。いくつかのフレームがスキップされ、ムービー ストリップが後で開始されます (図 9 を参照)。負の場合、FV フレームは FA フレームの前に来る必要があります (最初に FV = FA と仮定します)。これは不可能です。
  そのため、FA フレームが繰り返されます (説明については、ホールド オフセットのセクションを参照してください)。


Strip Offset End
   .. This field repositions the LV frame. If positive, the strip will be shortened.
   .. If negative, the strip is lengthened, thereby repeating (freezing) the LA frame.

   このフィールドは LV フレームの位置を変更します。
   正の場合、ストリップは短くなります。
   負の場合、ストリップは長くなり、それによって LA フレームが繰り返されます (フリーズします)。

.. figure:: /images/vse_setup_project_striptypes_offset-strip.svg
   :alt: Strip Offset fields

   図 9: ストリップ オフセット フィールドの視覚化

..
  Both Strip Offset fields can be changed by entering a value or by dragging the left or right strip handles.
  If Show Overlay is enabled a small bar appears at the bottom or top of the strip bar to indicate the Offsets.
..
両方の Strip Offset フィールドは、値を入力するか、左右のストリップ ハンドルをドラッグすることによって変更できます。
[Show Overlay] が有効になっている場合、オフセットを示す小さなバーがストリップ バーの下部または上部に表示されます。

Hold Offset Start
  ..
   This field will reposition the FA frame.
   It can't be negative because there are no frames available before the FA frame.
   A positive value does something seemingly contra-intuitive: the Duration of the strip is shortened.
   However, the Start field (where the FA is positioned at the timeline)
   remains the same and there are fewer frames available to display.
   So, the strip is shortened but the FA frame will be different.
  ..
  このフィールドは FA フレームの位置を変更します。
  FA フレームの前に利用可能なフレームがないため、負の値にすることはできません。
  正の値を指定すると、一見矛盾しているように見えますが、ストリップの Duration が短くなります。
  ただし、Start フィールド (FA がタイムラインに配置される場所) は同じままで、表示できるフレームが少なくなります。つまり、ストリップは短くなりますが、FA フレームはそのままです。

Hold Offset End
  ..
   This field will reposition the LA frame. A positive number will reduce the LA value.
   The effect is also a shortening of the strip.
  ..
  このフィールドは LA フレームの位置を変更します。正の数を指定すると、LA 値が減少します。
  この効果はストリップを短くすることにもなります。


.. figure:: /images/vse_setup_project_striptypes_offset-hold.svg
   :alt: Hold Offset fields

   図 10: Hold Offset フィールドの視覚化

..
  Of course, you can combine both types of offset. In figure 11, there is a combined offset of 8 frames.
  So, the original duration of 10 frames is reduced to two frames.
..
もちろん、両方のタイプのオフセットを組み合わせることもできます。
図 11 には、合せて8フレームのオフセットが設定されています。そのため、元の10フレームの長さは 2 フレームに短縮されます。

.. figure:: /images/vse_setup_project_striptypes_offset-both.svg
   :alt: Both Offset fields

   図 11: ストリップ フィールドとホールド オフセット フィールドの両方の視覚化

..
  In the previous text, we mentioned a few times the "freezing" effect or the repeating of the first or last frame.
  This can be done by for example extending the LV frame beyond the LA frame
  (entering a larger number in the Duration field).
  Or by dragging the left or right handle beyond the FA or LA frame.
  In figure 12 there are two repeating first frame and two repeating last frames.
  The Still Offset fields are added to the Time panel via a Python script.
  For an in-depth explanation of how to do this,
  see :doc:`section 5 Extra-tools </extra-tools/python-useful-scripts>`.
..

前の文章では、*freezing* 効果、つまり最初または最後のフレームの繰り返しについて何度か言及しました。
これは、たとえば、LV フレームを LA フレームを超えて拡張する ([Duration] フィールドに大きな数値を入力する) ことで実行できます。
または、左または右のハンドルを FA または LA フレームを超えてドラッグします。

図 12 には、最初のフレームが 2 つ繰り返され、最後のフレームが 2 つ繰り返されます。Still Offset フィールド  [#f3]_ は、Python スクリプトを介して Time パネルに追加されます。これを行う方法の詳細な説明については、 :doc:`section 5 Extra-tools </extra-tools/python-useful-scripts>` を参照してください。


.. figure:: /images/vse_setup_project_striptypes_offset-still.svg
   :alt: Still Offset fields

   図 12: Still Offset フィールドの視覚化

Current Frame
  ..
   Position of the Playhead relative to the FA frame of the active strip.
   So, if the strip starts at frame 10 and the Playhead is positioned at (timeline) frame 15,
   the Current Frame will be 5.
  ..
  アクティブなストリップの FA フレーム [#f4]_ に対するPlayheadの位置。
  したがって、ストリップがフレーム 10 で始まり、Playheadが (タイムライン) フレーム 15 に配置されている場合、現在のフレームは 5 になります。




.. _source-panel:

Source
------

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Source
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-source-movie-strip.png
   :scale: 50%
   :alt: Source Property
   :align: Right

   図13: Sourceパネル

File
  ..
   The directory and filename that contains the source file.
   When a file has moved this field can be updated instead of re-creating the strip.
  ..
  ソースファイルが含まれるディレクトリとファイル名。ファイルが移動された場合、ストリップを再作成する代わりに、このフィールドを更新できます。

Color Space
  ..
   To specify the color space of the source file of this strip.
   The color space for the Sequencer is globally set in the Color Management panel
   of the Render Properties but you can deviate from it here.
   Most of the imported clips however have a sRGB color space.
   For :doc:`Scene strip <./scene>` it can be beneficial to set the color space to Filmic.
  ..
  このストリップのソース ファイルのカラー スペースを指定します。
  Sequencer のカラー スペースは、[Render]Properties の [Color Management]パネルでグローバルに設定されますが、ここで独自設定することができます。
  ただし、インポートされたクリップのほとんどは sRGB カラー スペースを持っています。 :doc:`Scene strip <./scene>` の場合、カラースペースをフィルミックに設定すると効果的です。

MPEG Preseek
  ..
   Preseek is used to decide for the fastest way to decode a specific frame.
   It should match the Group of Pictures (GOP) size of the video;
   see `Bryan Samis blog <https://aws.amazon.com/blogs/media/part-1-back-to-basics-gops-explained/>`_
   for an in-depth explanation of GOP.
   Finding the GOP-size of a video however, is not a trivial thing (see the above link for a manual approach).
   Setting preseek to a high value like 200 could negatively impact seek performance.
   Therefore it is limited to max = 50 where it makes little to no difference.
   So, in practice, you will not use this option very often.
  ..

  プリシークは、特定のフレームをデコードする最速の方法を決定するために使用されます。
  ビデオのグループ オブ ピクチャ (GOP) サイズと一致する必要があります。 GOP の詳細な説明については、 `Bryan Samis blog <https://aws.amazon.com/blogs/media/part-1-back-to-basics-gops-explained/>`_ を参照してください。
  ただし、ビデオの GOP サイズを見つけるのは簡単なことではありません (手動の方法については、上記のリンクを参照してください)。
  プリシークを 200 などの高い値に設定すると、シークのパフォーマンスに悪影響を及ぼす可能性があります。
  したがって、違いがほとんどない最大 = 50 に制限されます。したがって、実際には、このオプションはあまり使用されません。


Stream Index
    ..
     Some video files can contain multiple video and audio streams; for example, two surveillance camera outputs.
     However, most video players cannot simultaneously preview both streams next to each other.
     With this property, you can select the stream to preview (but again not both at the same time).
     Of course, you can add the same movie strip twice, set the stream index appropriately,
     and use the Picture-in-Picture approach from above. For the inverse:
     see :doc:`section Extra tools > ffmpeg </extra-tools/ffmpeg>`
     to merge two video channels into one container.
    ..
    一部のビデオ ファイルには、複数のビデオ ストリームとオーディオ ストリームを含めることができます。
    たとえば、2 つの監視カメラ出力。ただし、ほとんどのビデオ プレーヤーでは、両方のストリームを並べて同時にプレビューすることはできません。
    このプロパティを使用すると、プレビューするストリームを選択できます (ただし、同時に両方を選択することはできません)。
    もちろん、同じムービー ストリップを 2 回追加し、ストリーム インデックスを適切に設定し、
    上記のピクチャ イン ピクチャ アプローチを使用することもできます。
    逆の場合: :doc:`section Extra tools > ffmpeg </extra-tools/ffmpeg>` を参照して 、2 つのビデオ チャネルを 1 つのコンテナにマージします。

Deinterlace
  ..
   Most (old) TV broadcasts use interlaced scan technology.
   A HD (1920 x 1080) image is split in half (two fields)
   and the odd and even lines are transmitted separately, one after the other.
   So, there is a very small time delay between the two fields.
   Most modern TVs and computer screens work with Progressive technology
   where the full image is transmitted at once; line per line.
   Viewing an interlaced image/movie on a computer monitor
   shows interlacing artifacts such as saw teeth or combing.

   Figure 10 shows an interlaced (left) and deinterlaced (right) still from a movie.
   Perhaps you have to zoom in to see the artifacts. In the movie, the blue square is moving.
   Interlacing artifacts are more noticeable with movement
   because the scanned fields are not taken at the same time (one after the other!).
   And with movement, this becomes more apparent.
  ..
  ほとんどの (古い) テレビ放送ではインターレース スキャン テクノロジが使用されています。
  HD (1920 x 1080) 画像は半分 (2 フィールド) に分割され、奇数ラインと偶数ラインが別々に順番に送信されます。
  したがって、2 つのフィールド間には非常に小さな時間遅延が生じます。
  最新のテレビやコンピュータ画面のほとんどはプログレッシブ技術で動作し、行ごとに完全な画像が一度に送信されます。
  コンピューターのモニターでインターレース画像/ムービーを表示すると、鋸歯やコーミングなどのインターレースアーティファクトが表示されます。

  図 14 は、ムービーのインターレース静止画 (左) とインターレース解除静止画 (右) を示しています。
  おそらく、アーティファクトを確認するにはズームインする必要があります。
  動画では青い四角が動いています。スキャンされたフィールドは同時に (次々に) 取得されないため、
  動きがあるとインターレース アーティファクトがより目立ちます。そして、動くと、それがより顕著になります。

.. figure:: /images/vse_setup_project_striptypes_deinterlace.svg
   :alt: Interlace vs deinterlace
   :align: Right

   図 14: インターレースおよびデインターレース スキャン



.. You can download the test file from figure 10 from the
.. `Grass Valley Developers <http://www.gvgdevelopers.com/concrete/products/summit/test_clips/>`_ website.
図 14 のテスト ファイルは、 `Grass Valley Developers <http://www.gvgdevelopers.com/concrete/products/summit/test_clips/>`_  Web サイトからダウンロードできます。

.. _resolution:

Resolution & fps
  ..
   Dimension (width x height in pixels) of the active strip image output.
   Frames per second (fps) of the active strip.

   These properties are not not editable and should preferably match the settings of the project (see :doc:`see Organize > Import section </video_editing/edit/montage/add>` ).

   Note that scaling the strip will change the visual dimension of the frame but of course not its resolution.
  ..

  アクティブなストリップ画像出力の dimentions (ピクセル単位の幅 x 高さ)。アクティブなストリップの 1 秒あたりのフレーム数 (fps)。

  これらのプロパティは編集できません。できればプロジェクトの設定と一致させるとよいです。 ( :doc:`see Organize > Import section </video_editing/edit/montage/add>` を参照)。

  ストリップをスケーリングすると、フレームの視覚的な dimension が変わりますが、解像度は変わりません。


.. _custom-panel:

Custom Properties
-----------------

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Custom
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-custom.png
   :scale: 50%
   :alt: Custom Property
   :align: Right

   図15: Custom パネル

..
  Custom properties are a way to store your own metadata in a strip.
  For example, you could use it to store some copyright
  information of a strip or instructions for further post-processing.
  More information can be found in the `data-blocks section <https://docs.blender.org/manual/en/dev/files/data_blocks.html#files-data-blocks-custom-properties>`_.
..

カスタム プロパティは、独自のメタデータをストリップに保存する方法です。たとえば、これを使用して、ストリップの著作権情報や、さらなる後処理のための指示を保存できます。詳細については、 `data-blocks section <https://docs.blender.org/manual/en/dev/files/data_blocks.html#files-data-blocks-custom-properties>`_ を参照してください。

.. rubric:: 脚注

.. [#f1] Blender4.0 では 利用できるChannelの範囲は1〜128です。
.. [#f2] Blender3.2で *frame_still_start* と *frame_still_end* は削除されたようです。 (https://developer.blender.org/docs/release_notes/3.2/python_api/#breaking-changes)
.. [#f3] Blender3.2以降では、 *frame_still_start* と *frame_still_end* ではなく、 *frame_offset_start* と *frame_offset_end* の負値で表現します。
.. [#f4] Blender4.0 では、 `Strip Offset Start`(負の場合あり) に対する Playheadの位置 のようです。
