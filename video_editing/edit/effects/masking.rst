Masking
-------

.. Masking is a video editing technique to isolate a portion of a video image in order to apply some effect on the isolated area. The area of the strip that you want to isolate is specified by a mask. This is essentially a black-and-white image of the same size as the strip-image. The isolated area is painted in white; the area that can be ignored is painted in black.

マスキングは、ビデオ画像の一部を分離して、分離された領域に何らかの効果を適用するビデオ編集手法です。分離したいストリップの領域はマスクによって指定されます。これは本質的に、ストリップ画像と同じサイズの白黒画像です。孤立した領域は白でペイントされます。無視できる領域は黒で塗りつぶされます。

.. The masking then is done by changing the alpha channel of the source-strip. In addition to its RGB color values, each pixel has an additional value within the range 0-1. If alpha=0, then the pixel is transparent, and the RGB values of the pixel contribute nothing to the pixel’s appearance; for alpha=1, the pixel is fully opaque, and the color of the pixel is fully determined by its RGB values. You can remember these values by keeping the multiplication rule in mind: multiplying the RGB-values by 1 will keep the original RGB-values. Multiplying by zero will erase all RGB values.

次に、ソース ストリップのアルファ チャネルを変更することによってマスキングが行われます。 RGB カラー値に加えて、各ピクセルには 0 ～ 1 の範囲内の追加の値があります。 alpha=0 の場合、ピクセルは透明であり、ピクセルの RGB 値はピクセルの外観にまったく影響しません。 alpha=1 の場合、ピクセルは完全に不透明になり、ピクセルの色は RGB 値によって完全に決まります。乗算ルールを念頭に置くことで、これらの値を覚えておくことができます。つまり、RGB 値を 1 で乗算すると、元の RGB 値が保持されます。ゼロを乗算すると、すべての RGB 値が消去されます。

.. figure:: /images/video_editing_edit_effects_masking-alpha-channel.svg
   :alt: Mask alpha calculation

   図1 ソース ストリップに適用されたさまざまな領域のマスクによるアルファ値の計算

.. Masking multiplies the alpha value of a source-strip pixel with the smallest RGB-value of the corresponding mask pixel to get the result. So, if the mask is white (see fig 1), its RGB value is (1,1,1) and the alpha value of the corresponding result is set to 1 or fully opaque (1 x 1 = 1). If the mask is black RGB (0,0,0), the result is fully transparent because 1 x 0 = 0. The mid grey RGB(0.5,0.5,0.5) and yellow RGB(1,1,0) masks make the result partial transparent for the mid-grey because the smallest RGB value = 0.5 and fully transparent for the yellow mask because the smallest RGB value = 0. So, in figure 2, both the black and yellow regions of the mask will make the source strip transparent at that location.

マスキングでは、ソース ストリップ ピクセルのアルファ値と、対応するマスク ピクセルの最小の RGB 値を乗算して結果を取得します。したがって、マスクが白の場合 (図 1 を参照)、その RGB 値は (1,1,1) で、対応する結果のアルファ値は 1 または完全に不透明 (1 x 1 = 1) に設定されます。マスクが黒の RGB (0,0,0) の場合、1 x 0 = 0 であるため、結果は完全に透明になります。中間のグレーの RGB(0.5,0.5,0.5) と黄色の RGB(1,1,0) マスクにより、結果は、最小の RGB 値 = 0.5 であるため、中間グレーでは部分的に透明になり、最小の RGB 値 = 0 であるため、黄色のマスクでは完全に透明になります。 したがって、図 2 では、マスクの黒と黄色の両方の領域がソース ストリップになります。その場所では透明になります。

Strip masks
...........

.. Masking in the VSE is done with the help of the Mask modifier (see figure 2 and 3). Select the strip you want to mask and apply the Mask modifier.Select Strip as Mask Input Type and choose from the Mask drop-down your mask (in this case Mask-strip). Be sure to mark the mask strip as Muted (:kbd:`H`); you don't want to see this strip.
VSE でのマスキングは、Mask モディファイアを使用して行われます (図 2 および 3 を参照)。マスクするストリップを選択し、マスク モディファイアを適用します。マスク入力タイプとしてストリップを選択し、マスク ドロップダウンからマスク (この場合はマスク ストリップ) を選択します。必ずマスク ストリップをミュート (:kbd:`H`) としてマークしてください。このストリップは見たくないでしょう。

.. figure:: /images/video_editing_edit_effects_masking-strip-mask.svg
   :alt: Meta strip mask

   図2 ストリップ マスクを使用したMask modifier

.. Figure 2 uses a Color strip that is cropped to the size of the isolation area. The project is set to the resolution of the source strip (Sprite Fright - Blender Open Movie - 1280 x 536). So, the added Color strip has also a resolution of 1280 x 536. It is cropped to about 960 x 230 to isolate the area of the walking characters. The result of this Mask modifier is a cut-out of the isolated area on a transparent background.

図 2 では、分離領域のサイズに合わせてトリミングされたカラー ストリップを使用しています。プロジェクトはソース ストリップの解像度 (Sprite Fright - Blender Open Movie - 1280 x 536) に設定されます。したがって、追加されたカラー ストリップも 1280 x 536 の解像度を持ちます。歩行するキャラクターの領域を分離するために、約 960 x 230 にトリミングされます。このマスク モディファイアの結果は、透明な背景上の孤立した領域の切り抜きです。

.. Notice that the edges of the cut-out are sharp; from fully opaque to fully transparent in one pixel. This is because the Color strip also has sharp white to black/transparent borders.

切り抜きのエッジが鋭利であることに注意してください。 1 つのピクセルで完全に不透明から完全に透明になります。これは、カラー ストリップにも白から黒/透明のはっきりした境界線があるためです。

.. *Also* notice that the mask strip does not have to be of the same length as the source strip. The modifier takes care of applying the mask to the entire source strip. If you want the mask only for a specific time frame of the strip, you need cut the strip.

また、マスク ストリップはソース ストリップと同じ長さである必要はないことに注意してください。 modifier は、ソース ストリップ全体にマスクを適用します。ストリップの特定の時間枠のみマスクが必要な場合は、ストリップをカットする必要があります。

.. *Also*, the mask strip doesn't have to be at the same location of the source strip. For example, you can collect all of your mask strips at the end of the timeline. Most of the time, however, you will try to locate your mask strip nearby its source strip. A strip mask can be used multiple times within the same scene. Of course, then it is not possible to keep mask and source together at the same location.

また、マスク ストリップはソース ストリップと同じ位置にある必要はありません。たとえば、タイムラインの最後にすべてのマスク ストリップを収集できます。ただし、ほとんどの場合、マスク ストリップをソース ストリップの近くに配置しようとします。ストリップ マスクは、同じシーン内で複数回使用できます。もちろん、マスクとソースを同じ場所に保持することはできません。

.. figure:: /images/video_editing_edit_effects_masking-metastrip-mask.svg
   :alt: Meta strip mask
   :align: right
   :scale: 20%

   図3 矢印マスク

.. A mask strip can be a Meta strip. You can group several Color strips (with different shapes) into a Meta strip and use this strip as mask. Figure 3 shows how you can create a simple arrow-shape, out of 5 Color strips. A white background is used; so that the arrow can be used as a mask.

マスク ストリップはメタ ストリップにすることができます。複数のカラー ストリップ (形状が異なる) を 1 つのメタ ストリップにグループ化し、このストリップをマスクとして使用できます。図 3 は、5 つのカラー ストリップから単純な矢印の形を作成する方法を示しています。白い背景が使用されます。矢印をマスクとして使用できるようにします。

.. Masks don't need to be a black-and-white image. You can use whatever color, although in practice only grey-scale shades are used. To create a feather-effect, you need a gradient grey-scale border that goes from white to black. The more steps you have in the gradient, the smoother the feather. Behind the scenes, Blender takes smallest value of the RGB-triple and applies this value as a factor to the alpha channel of the source strip.

マスクは白​​黒画像である必要はありません。どのような色でも使用できますが、実際にはグレースケールの色合いのみが使用されます。フェザー効果を作成するには、白から黒へのグラデーションのグレースケール境界線が必要です。グラデーションのステップが多いほど、ぼかしが滑らかになります。 Blender はバックグラウンドで RGB トリプルの最小値を取得し、この値を係数としてソース ストリップのアルファ チャネルに適用します。

.. At last, the mask-image does not need to be static image. You can use whatever Movie strip as a mask.
最後に、マスク画像は静止画像である必要はありません。任意のムービー ストリップをマスクとして使用できます。


Data-block masks
................

.. Blender needs to know which area of a strip you want to isolate. You can specify this area by another strip (see above) or by creating a description of the mask in another editor. Masks can be created in the Image and Movie Clip editors, by changing the Editing Context to Mask in the header (see figure 4. This will add various tools and properties to the editor panels, while hiding others that are not needed for interacting with masks.

Blender は、ストリップのどの領域を分離したいかを知る必要があります。この領域は、別のストリップ (上記を参照) によって指定するか、別のエディタでマスクの定義を作成することによって指定できます。マスクは、Image Editor と Movie Clip Editorの ヘッダーの [Editing Context] を [Mask] に変更することで、で作成できます (図 4)。これにより、さまざまなツールとプロパティがエディター パネルに追加され、マスクの操作に必要のないその他のツールやプロパティは非表示になります。

.. figure:: /images/video_editing_edit_effects_masking-datablock-mask.svg
   :alt: Data-block mask

   図4 データ ブロック マスクを使用したマスク モディファイア

.. The Image Editor is a good choice for a static mask. In figure 4, the original File Browser window from the Video Editing workspace is replaced with the Image Editor. To have a reference image, you can first render the source strip (without mask) and use this Render Result in the Image Editor (click on the Browse Image to be linked button in the middle of the header to select the Render Result).

Image Editor は静的マスクに適しています。図 4 では、 Video Editing Workspace の元のファイル ブラウザ ウィンドウが Image Editor に置き換えられています。参照イメージを使用するには、まずソース ストリップを(マスクなしで)レンダリングし、このレンダリング結果をイメージ エディタで使用します(ヘッダーの中央にあるリンクするイメージを参照ボタンをクリックしてレンダリング結果を選択します)。

.. Use the menu Add or :kbd:`Shft - A` to add a Circle or Square mask. This small mask is added at the location of the 2D-cursor; usually at the bottom-left corner of the image (location 0.0). You can change the location of the 2D-cursor with the shortcut :kbd:`Shft - RMB` or with the sidebar > View > 2D Cursor. The top-right location is at (1.1). You can add custom masks by :kbd:`Ctrl - LMB` in the image. :kbd:`Ctrl - LMB` and drag will create a kind of Bezier handle to the curve.   To add a feather effect, use the shortcut :kbd:`Alt-S` and drag. Depending on the direction of the mask (menu Mask > Switch Direction) the feathering border (green line) is drawn inside or outside of the mask. The distance between the feathering border and the mask will control the smoothness of the transition between opaque and transparent.

[Add]メニュー または :kbd:`Shft-A` により、 [Circle] または [Square] マスクを追加できます。この小さなマスクは 2D カーソルの位置に追加されます。通常は画像の左下隅 (位置 0.0) にあります。 2D カーソルの位置は、 :kbd:`Shft-RMB` または、ショートカットまたは Sidebar > [View] > [2D Cursor] を使用して変更できます。
右上の場所は (1.1) です。:kbd:`Ctrl-LMB` で画像内でカスタムマスクを追加できます。 :kbd:`Ctrl-LMB` クリックし、ドラッグすると、曲線に対する一種のベジェ ハンドルが作成されます。フェザー効果を追加するには、ショートカット :kbd:`Alt-S` を使用してドラッグします。
マスクの方向 ( [Mask]メニュー > [Switch Direction]) に応じて、フェザリング境界線 (緑色の線) がマスクの内側または外側に描画されます。フェザリング境界線とマスクの間の距離は、不透明と透明の間の移行の滑らかさを制御します。

.. The mask can be named in the Browse Mask to be linked box (middle of header) and also appears as a data-block in the Outliner (Blend File display mode). You can use this mask multiple times within the same scene *but* also between scenes.

マスクは [Browse Mask to be linked] ボックス (ヘッダーの中央) で名前を付けることができ、アウトライナー (blendファイル表示モード) でデータ ブロックとしても表示されます。このマスクは、同じシーン内だけでなく、シーン間でも複数回使用できます。

.. Sometimes you need a mask that changes location or shape; e.g. when blurring a moving car license plate. Creating such a dynamic mask can best be done in the Movie Clip Editor. Change the workspace to the VFX > Masks workspace and  open the source clip. You cannot add a Scene strip or the render result of the VSE. In that case, you should render the scene first.  More information about creating and editing masks can be found in the `Motion Tracking & Masking <https://docs.blender.org/manual/en/latest/movie_clip/masking/index.html#>`_  section of the docs.

場合によっては、位置や形状を変更するマスクが必要になることがあります。たとえば、走行中の車のナンバープレートをぼかす場合などです。このようなダイナミック マスクの作成は、ムービー クリップ エディターで行うのが最適です。ワークスペースを [VFX] > [Masking] ワークスペースに変更し、ソース クリップを開きます。シーン ストリップや VSE のレンダリング結果を追加することはできません。その場合は、最初にシーンをレンダリングする必要があります。マスクの作成と編集の詳細については、 ドキュメントの `Motion Tracking & Masking <https://docs.blender.org/manual/en/latest/movie_clip/masking/index.html#>`_ セクションを参照してください。


.. todo::
   .. Add some more info to this section or refer to other docs
   このセクションにさらに情報を追加するか、他のドキュメントを参照してください。



.. Some examples
いくつかの例
.............

.. Masking is used in almost every video project, for example
マスキングはほぼすべてのビデオ プロジェクトで使用されます。たとえば、

..
  1. to cut out a part of a strip with some basic shapes as square, circle, arrow or more advanced such as letter masks.
  2. to blur a specific area of a strip,; e.g. faces or license plates.
  3. to color grade some area of a strip while leaving alone the rest, e.g. darken the sky.
  4. to create new images, for example in combination with green screens.
  5. to create a custom transition between strips; e.g. diagonal sweep.
..
1. 正方形、円、矢印などの基本的な形状、または文字マスクなどのより高度な形状でストリップの一部を切り取ります
2. ストリップの特定の領域をぼかすには、;顔やナンバープレートなど。
3. ストリップの一部の領域をカラー グレーディングし、残りの領域はそのままにしておきます (空を暗くするなど)。
4. たとえば、グリーン スクリーンと組み合わせて新しいイメージを作成します。
5. ストリップ間のカスタムトランジションを作成します。たとえば、斜めのスイープ。

.. figure:: /images/video_editing_edit_effects_masking_example-text-mask.png
   :alt: Cut out with letter mask

   図6 文字マスクで切り取る

.. For the letter mask of figure 6, you need to add a Text strip with white color. Select the movie clip, add a Mask modifier and choose the above text strip as mask. Don't forget to mute the mask strip.

図6 の文字マスクの場合、白色のテキスト ストリップを追加する必要があります。ムービークリップを選択し、[Mask modifier]を追加して、上記のテキストストリップをマスクとして選択します。マスクストリップをミュートにすることを忘れないでください。

.. figure:: /images/video_editing_edit_effects_masking_example-blur-mask.png
   :alt: Blur mask

   図7 ぼかしマスク

.. For the blur-effect, you need three strips and a mask. The first strip is the original movie, the second strip is a copy of the first, but with a cut-out mask applied. In the example of figure 7, the text of both boxes are masked out. An effects > Gaussian blur strip is added on top of this channel. The size of the blur should be adapted.

ぼかし効果を得るには、3 つのストリップとマスクが必要です。最初のストリップはオリジナルのムービーで、2 番目のストリップは最初のストリップのコピーですが、カットアウト マスクが適用されています。図 7 の例では、両方のボックスのテキストがマスクされています。[Effects] > [Gussian blur] ストリップがこのチャンネルの上に追加されます。ぼかしのサイズを調整する必要があります。


.. figure:: /images/video_editing_edit_effects_masking_example-colorgrade-mask.png
   :alt: Color grade mask

   図 8: カラーグレードマスク

.. In figure 8, a circular area is isolated in order to brighten it. You need a circular mask and the Brightness/Contrast modifier. Apply the modifier to the source strip and select the appropriate mask.

図8 では、明るくするために円形の領域が分離されています。円形マスクと [Brightness/Contrast modifier] が必要です。modifier をソース ストリップに適用し、適切なマスクを選択します。


.. figure:: /images/video_editing_edit_effects_masking_example-rotoscoping-mask.png
   :alt: Rotoscoping mask

   図 9: ロトスコーピング/グリーン スクリーン マスクカラー グレード マスク


.. To create this rotoscoping/green screen mask, you need two movies (one preferably shot before a green screen). Create a mask on the greenscreen movie; this will become the fore ground. In the example in figure 9, the character Spring has been masked out. Apply the mask and put the strip above the background movie (in the example Sprite Fright). Don't forget to change the blend mode of the greenscreen strip to Overdrop.

このロトスコープ/グリーン スクリーン マスクを作成するには、2 つのムービーが必要です (1 つはグリーン スクリーンの前に撮影することが望ましい)。グリーンスクリーン ムービーにマスクを作成します。これが前景になります。図 9 の例では、Spring という文字がマスクされています。マスクを適用し、背景ムービーの上にストリップを配置します (Sprite Fright の例)。グリーンスクリーン ストリップのブレンド モードをオーバードロップに変更することを忘れないでください。 [#f1]_

.. To create some nice transitions and VFX effects, you can follow the excellent `tutorial series <https://www.youtube.com/playlist?list=PLH3QvbpQe8WTbRFlKKWBwgJuTsZf58tXz>`_  by Blender Frenzy.

素晴らしいトランジションや VFX エフェクトを作成するには、Blender Frenzy による優れた `tutorial series <https://www.youtube.com/playlist?list=PLH3QvbpQe8WTbRFlKKWBwgJuTsZf58tXz>`_ に従うことができます 。

.. rubric:: 訳注

.. [#f1] 図9の内容と説明が違うように思います。
