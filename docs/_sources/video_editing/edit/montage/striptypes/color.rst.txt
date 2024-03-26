.. _bpy.types.ColorSequence:

***********
Color ストリップ
***********

..
  The Color strip is a sequence of 25 frames with a solid color.
  It fills the complete preview area with the selected color.
  The resolution is derived from the Project Settings.
  Its Duration is set by the same mechanism as the Image strip (see :ref:`Movie strip - Time panel <time-panel>`.
  The :ref:`default <default-color>` color of the Color strip bar is: :color:`███`.
  However, the selected color will also be shown in the lower half of the strip bar (see figure 1).
..

カラー ストリップは、単色の 25 フレームのシーケンスです。Preview 領域全体が選択した色で塗りつぶされます。
解像度はプロジェクト設定から取得されます。
その Duration は、Image ストリップと同じメカニズムによって設定されます (参照 :ref:`Movie strip - Time panel <time-panel>`)。
カラー ストリップ バーのデフォルトの色は :color:`███` です。
ただし、選択した色はストリップの下半分にも表示されます)バー (図 1)。

.. The Color strip is used to create some custom transitions and in combination
.. with the Crop and/or Transform property to create some horizontal or vertical colored bars (see figure 1).

Color ストリップは、カスタム トランジション や
水平または垂直の色付きバー([Crop] および/または [Transform] プロパティと組み合わせて) を作成するために使用されます (図 1 を参照)。

.. figure:: /images/vse_setup_project_striptypes_color.svg
   :alt: Use of the Color strip

   図1 Color ストリップの使用例

..
  Note that the original color strips have a dimension of 1920 x 1080.
  Cropping Left and Right will produce the vertical bars.
  You can do some simple math to position the bars exactly.
  Because the height is 1080, the middle bar should be at 1080/2.
  If you want a width of 10 pixels for this bar, you need to subtract additional 5 pixels from top and bottom crop.
  Please, note also that these Color strips should have a blend mode of Overdrop or Alpha Over.
..

オリジナルの Color ストリップの寸法は 1920 x 1080 であることに注意してください。左右をトリミングすると、垂直バーが生成されます。
簡単な計算を行ってバーを正確に配置することができます。
高さは 1080 なので、中央のバーは 1080/2 になるはずです。
このバーの幅を 10 ピクセルにしたい場合は、上部と下部のトリミングからさらに 5 ピクセルを減算する必要があります。
これらの Color ストリップには、Overdrop または Alpha Over のブレンド モードが必要であることにも注意してください。



Options
=======

.. note::

   .. Panels documented elsewhere!
   パネルは他の場所で文書化されています。


   .. The following panels are identical to those from the Movie strip:
   次のパネルは Movie ストリップのパネルと同じです

   - :ref:`Compositing <compositing-panel>`
   - :ref:`Transform <transform-panel>`
   - :ref:`Crop <crop-panel>`
   - :ref:`Video <video-panel>`
   - :ref:`Color <color-panel>`,
   - :ref:`Time <time-panel>`
   - :ref:`Custom <custom-panel>`.

   .. The Time panel has no Strip Offset or Hold Offset properties because there is no content to offset.
   .. The strip is evenly colored.

   オフセットするコンテンツがないため、[Time] パネルには [Strip Offset] または [Hold Offset] プロパティがありません。
   ストリップは均一に色付けされています。

.. An Effect panel is added to the Properties.
エフェクトパネルがプロパティに追加されます。

Effect Strip
------------

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Effect Strip
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-effect-strip-color.png
   :scale: 50%
   :alt: Effect Strip Property
   :align: right

   図2 Color ストリップのEffectプロパティ

Effect Strip
  ..
   With the vertical slider, you can set the brightness of the color.
   Clicking on the horizontal slider will display a standard Color Picker.
   More info about the :doc:`Color Picker </video_editing/edit/color-grading/terminology/terminology>` in the Color grading section.
   This Color Picker has some additional settings, i.e. opacity.

   The existing Color panel has some overlap with the Effect Strip panel, for example, the Saturation field.
  ..
  垂直スライダーを使用して、色の明るさを設定できます。
  水平スライダーをクリックすると、標準のカラー ピッカーが表示されます。
  Color grading セクションの :doc:`Color Picker </video_editing/edit/color-grading/terminology/terminology>` を参照してください。
  このカラーピッカーには、不透明度などの追加設定があります。

  既存のカラーパネルには、Saturation フィールドなど、Effect ストリップ パネルと重複する部分があります。

