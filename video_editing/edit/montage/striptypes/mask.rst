.. _bpy.types.MaskSequence:

**********
Mask ストリップ
**********

..
  In general, any strip could be a masking strip.
  The VSE Mask strip however is rather restricted to the masks, created in the Movie Clip Editor.
  There will be nothing in the Mask menu unless you have created a mask in the Movie Clip Editor.
  At all other times, it's just a blank menu. If there are multiple masks in the Movie Clip Editor,
  you can choose the appropriate mask from the drop-down menu. These masks could also be used as a modifier.
..

一般に、どのようなストリップもマスキング ストリップとして使用できます。
ただし、VSEの Mask ストリップは、Movie Clip Editor で作成されたマスクに限定されています。
Movie Clip Editor でマスクを作成しない限り、[Mask]メニューには何も表示されません。
それ以外の場合は、単なる空白のメニューです。Movie Clip Editorに複数のマスクがある場合は、
ドロップダウン メニューから適切なマスクを選択できます。これらのマスクは Modifire としても使用できます。


.. figure:: /images/vse_setup_project_striptypes_mask.svg
   :alt: Masking

   図2 Movie Clip Editor と Mask ストリップを使用したマスキング

..
  A mask is a grey-scale image. The Movie Clip Editor generates this image
  as you create a mask but also a common Image strip can be used.
  It is stored in a data-block and saved within the Blend-file.
  You place this mask image on top of a background image and apply the ``Multiply`` blend mode.
  Therefore, you need a Mask strip or a Mask modifier. Because the color White is coded as RGB(1,1,1),
  multiplying a color from the background (underlying strip) with 1 will return the same color as the background.
  The white area of the mask is thus fully transparent, the background image 'shines' through.
  A black color is coded as RGB (0,0,0).
  So, multiplying this color with the background color will result in 0 or black. The mask is opaque.

  In the Movie Clip Editor, you can do also tracking. The mask should indeed follow the movement of the dog.
..

マスクはグレースケール画像です。
Movie Clip Editorはマスクの作成時にこのイメージを生成しますが、一般的な Image ストリップを使用することもできます。

これはデータブロックに保存され、blend ファイル内に保存されます。
このマスク イメージを背景イメージの上に配置し、 ``Multiply`` ブレンド モードを適用します。
したがって、Mask ストリップまたは Mask Modifire が必要です。

白の色は RGB(1,1,1) としてコード化されているため、背景 (下にあるストリップ) の色に 1 を乗算すると、背景と同じ色が返されます。
したがって、マスクの白い領域は完全に透明になり、背景画像が「透けて」見えます。
黒は RGB (0,0,0) としてコード化されます。したがって、この色と背景色を乗算すると、結果は 0 または黒になります。マスクは不透明です。

Movie Clip Editorでは、トラッキングも行うことができます。マスクは確かに犬の動きに追従する必要があります。



Options
=======

.. note::

  .. Panels documented elsewhere!
  パネルは他の場所で文書化されています。

   .. The following panels are identical to those from the Movie strip:
   次のパネルは Movie ストリップのパネルと同じです。

   - :ref:`Compositing <compositing-panel>`
   - :ref:`Transform <transform-panel>`
   - :ref:`Crop <crop-panel>`
   - :ref:`Video <video-panel>`
   - :ref:`Color <color-panel>`
   - :ref:`Time <time-panel>`
   - :ref:`Custom <custom-panel>`.

.. A Mask panel is added to the Properties (see figure 2)

[Mask]パネルがプロパティに追加されます (図 2)

Mask
----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Mask
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-mask.png
   :scale: 50%
   :alt: Mask Property of Mask Strip
   :align: Right

   図 2: Mask ストリップの[Mask]プロパティ

Mask selector
  ..
   With the drop-down, you can select the appropriate mask. If a mask is selected,
   this mask will be stored with the Blend file. If a mask is nowhere selected,
   it will be garbage-collected upon closing Blender and no more available the next time.
   With the Fake User button, you can prevent the loss of the mask, even if it is nowhere selected.
  ..

  ドロップダウンを使用して、適切なマスクを選択できます。
  マスクが選択されている場合、このマスクは blend ファイルとともに保存されます。
  マスクがどこにも選択されていない場合、そのマスクは Blender を閉じるときにガベージ コレクションされ、次回からは使用できなくなります。
  [Fake User] ボタンを使用すると、マスクがどこにも選択されていない場合でも、マスクの紛失を防ぐことができます。


Original Frame Range
   .. In the Movie Clip Editor, you have to set the Frame Range that the mask that will be applied.
   ..  By default, this range is set to frame 1 -100.
   Movie Clip Editor では、マスクが適用されるフレーム範囲を設定する必要があります。
   デフォルトでは、この範囲はフレーム 1 ～ 100 に設定されています。
