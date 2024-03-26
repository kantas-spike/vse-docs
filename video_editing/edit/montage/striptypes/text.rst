.. _bpy.types.TextSequence:

Text ストリップ
,,,,,,,,,,

..
  The Text strip allows you to directly display text in a frame.
  It is meant to display titles or other short text fragments.
  So, its length is limited (511 characters) and 1 line of text (with wrapping).
  Most properties of the text (e.g. Location, Color, ...) can be animated but not the text content or its font.
  The :ref:`default <default-color>` color of the Text strip bar is: :text:`███`.
..

Text ストリップを使用すると、フレーム内にテキストを直接表示できます。
タイトルやその他の短いテキストを表示することを目的としています。
そのため、長さは 511 文字に制限されており、テキストは 1 行（折り返し付き）です。
テキストのほとんどのプロパティ (場所、色など) はアニメーション化できますが、テキストの内容やフォントはアニメーション化できません。
Text ストリップバーのデフォルトの色は :text:`███` です。

.. figure:: /images/vse_setup_project_striptypes_text.svg
   :alt: Example of text strip

   図1 Text ストリップの例

..
  As is obvious from figure 1, the Text strip is not meant to write essays.
  Even for credit rolls as in figure 1, things get complicated very quickly.
  For small texts however it is ideal. With the Location and Anchor fields,
  you could position the text in the Preview window.
..

図 1 から明らかなように、Text ストリップはエッセイを書くことを目的としたものではありません。
図 1 のようなクレジット ロールの場合でも、状況はすぐに複雑になります。
ただし、小さなテキストには理想的です。 [Location] フィールドと [Anchor] フィールドを使用すると、
Preview ウィンドウにテキストを配置できます。

Options
^^^^^^^

.. note::
   .. Panels documented elsewhere!
   パネルは他の場所で文書化されています。

   .. The following panels are identical to those from the Movie strip:
   次のパネルは、Movie ストリップのパネルと同じです。

   - :ref:`Compositing <compositing-panel>`
   - :ref:`Transform <transform-panel>`
   - :ref:`Crop <crop-panel>`
   - :ref:`Video <video-panel>`
   - :ref:`Color <color-panel>`
   - :ref:`Custom <custom-panel>`

   The Time panel has no Strip Offset or Hold Offset properties.
   because there is no content to offset. The strip is evenly colored.
   There is also no Source panel because the text is defined in the Effect panel.

.. An Effect panel is added to the Properties (see figure 2).

Effect パネルがプロパティに追加されます (図 2 を参照)。

Effect Strip
^^^^^^^^^^^^

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Effect Strip
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-effect-strip-text-.png
   :scale: 60%
   :alt: Effect Property of Text Strip
   :align: Right

   図 2: Effectストリップのプロパティ

Text
  ..
   The actual text that is displayed. This text can be 511 characters long.
   The text can be split over multiple lines with the Wrap feature (see below)
   but it is not easy to create the split at a predefined location.
  ..

  実際に表示されるテキスト。このテキストの長さは 511 文字です。
  折り返し機能 (下記参照) を使用してテキストを複数行に分割できますが、
  事前に定義した位置で分割を作成するのは簡単ではありません。

Wrap Width
  ..
   Wraps the text by a percentage of the frame width. Setting this to zero will disable word wrapping.
   A value of 1 will wrap the text at the right border of the Preview (there is a slight left and right margin)
   This option however works in combination with the Anchor and Location fields (see below).
   The previous effect occurs only with a Center anchor and an X Location of 0.5 (default setting).
   If a left-aligned anchor however is specified, then the X location should be at 0 to have a split at the borders.
  ..

  フレーム幅のパーセンテージでテキストを折り返します。これをゼロに設定すると、ワードラップが無効になります。
  1 を指定すると、Preview の右端でテキストが折り返されます (左右にわずかな余白が生じます)。
  ただし、このオプションは、[Anchor] フィールドと [Location] フィールドと組み合わせて機能します (以下を参照)。
  前述の効果は、中心アンカーと X 位置が 0.5 (デフォルト設定) の場合にのみ発生します。
  ただし、左揃えのアンカーが指定されている場合は、境界で分割するために X 位置を 0 にする必要があります。



Style
^^^^^

Font
  ..
   The default font is Blender's own BMonoFont.
   You could find it in the  ``datafiles/fonts`` folder of your Blender installation.
   Clicking on the Open button will show a File Browser window with probably the Fonts directory of *your* system selected.
   This directory is set in the Preferences > File Path > Data.
   Of course, you can navigate to another folder.
   There you can choose a new font for the selected Text strip.
  ..

  デフォルトのフォントは Blender 独自の BMonoFont です。
  これはdatafiles/fonts、Blender インストールのフォルダーにあります 。
  [Open] ボタンをクリックすると、ファイル ブラウザ ウィンドウが表示され、おそらくシステムの Fonts ディレクトリが選択されています。
  このディレクトリは、[Preferences] > [File Path] > [Data] で設定されます。
  もちろん、別のフォルダーに移動することもできます。そこで、選択したテキスト ストリップの新しいフォントを選択できます。

.. figure:: /images/video_editing_edit_montage_text-strip-fonts-preview.svg
   :alt: Font selection preview

   図3 フォント選択のプレビュー

   .. If you want to see a preview of the chosen font, click the Thumbnail button in the Header (see figure 3).
   選択したフォントのプレビューを表示したい場合は、ヘッダーの [Thumbnail] ボタンをクリックします (図3)。

   .. Next to the Font selector, you find the Bold and Italic toggle buttons.
   フォント セレクターの隣に、太字と斜体の切り替えボタンがあります。

Size
  ..
   Size of the text. The value can vary between 0 and 2000.
   This size is of course different from the point size of a font (e.g. Arial 12).
   The default size of 60 corresponds approximately with a point size of 30.
  ..
  テキストのサイズ。値は 0 ～ 2000 の間で変化します。
  もちろん、このサイズはフォント (Arial 12 など) のポイント サイズとは異なります。デフォルトのサイズ 60 は、ポイント サイズ 30 にほぼ対応します。


Color
  ..
   Clicking on the color button will display a standard
   :doc:`Color Picker </video_editing/edit/color-grading/terminology/terminology>`.
  ..

  カラー ボタンをクリックすると、標準の :doc:`Color Picker </video_editing/edit/color-grading/terminology/terminology>` が表示されます。

Shadow
  ..
   Creates a shadow of the specified color under the text.
   You can change the color and opacity of the shadow with a color selector next to it.
   This opens a standard :doc:`Color Picker </video_editing/edit/color-grading/terminology/terminology>`.
   You can not change the size nor the orientation of the shadow.
   In combination with a Box (see below), this gives a nice effect.
  ..

  テキストの下に指定した色の影を作成します。影の横にあるカラーセレクターを使用して、影の色と不透明度を変更できます。
  これにより、標準の :doc:`Color Picker </video_editing/edit/color-grading/terminology/terminology>` が開きます。
  影のサイズや向きは変更できません。ボックス (下記参照) と組み合わせると、素晴らしい効果が得られます。

Box
   .. Creates a background for the text to improve the readability and clarity of text in some situations.
   .. The color and opacity of the box can be adjusted using the color selector.
   テキストの背景を作成して、状況によってはテキストの読みやすさと明瞭さを向上させます。
   ボックスの色と不透明度は、カラーセレクターを使用して調整できます。

Box Margin
  ..
   The distance that the box boundaries extend from the boundaries of the font glyphs.
   The distance is measured as a factor of the image's width.
   It is however not obvious how the margin width relates to the width of the text.
   A value of zero creates of course no margin.
  ..
  ボックスの境界がフォント グリフの境界から延びる距離。距離は画像の幅の係数として測定されます。
  ただし、余白の幅がテキストの幅とどのように関係するかは明らかではありません。値がゼロの場合、当然マージンは作成されません。


Layout
^^^^^^

Location X, Y
  ..
   With the values *X* and *Y* you can position the text in the preview frame.
   The value (0,0) refers to the bottom left and (1,1) to the top right.
   A value of (0.5, 0.5) sets the anchor of the text in the middle of the frame.
   Therefore it is good practice to first set the Anchor alignment (see below).

   You can specify a location value > 1; effectively writing the text outside of the Preview frame.
   Because you can animate this Location value, this comes in very handy to create an effect of rolling in or out.
  ..
  値XとYを使用すると、プレビュー フレーム内にテキストを配置できます。値 (0,0) は左下を指し、(1,1) は右上を指します。
  値 (0.5, 0.5) は、テキストのアンカーをフレームの中央に設定します。したがって、最初にアンカーの配置を設定することをお勧めします (以下を参照)。

  Locationには 1より大きい値 を指定できます。Preview フレームの外側にテキストを効果的に書き込むことができます。
  この Location 値はアニメーション化できるため、ロールインまたはロールアウトのエフェクトを作成するのに非常に便利です。

Anchor X, Y
  ..
   Horizontal (Left, Center, Right) or vertical (Top, Center, Bottom) anchor point of the text.
   With this value, you can align the text horizontally or vertically.
   For example, Location X & Y = 0 and Anchor X = Left and Anchor Y = Bottom,
   will position the text at the bottom left corner.
  ..

  テキストの水平方向 (左、中央、右) または垂直方向 (上、中央、下) のアンカー ポイント。
  この値を使用すると、テキストを水平方向または垂直方向に配置できます。
  たとえば、位置 X & Y = 0、アンカー X = 左、アンカー Y = 下とすると、テキストは左下隅に配置されます。
