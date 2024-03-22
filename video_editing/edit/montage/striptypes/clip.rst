.. _bpy.types.MovieClipSequence:

**********
Clip ストリップ
**********

..
  A clip strip is created from the output of the `Movie Clip Editor <https://docs.blender.org/manual/en/dev/editors/clip/introduction.html>`_.
  There is nothing in the Clip menu of the VSE unless you've opened media (video or images) in the Movie Clip Editor.
  At all other times it's just a blank menu. Together with ``Scene`` and ``Mask``,
  the Clip strip forms a group where the source of the strip must be generated within Blender.
  The :ref:`default <default-color>` color of the Clip strip bar is: :clip:`███`

  The Movie Clip Editor is used for advanced editing such as motion tracking and advanced masking.
..

クリップ ストリップは、 `Movie Clip Editor <https://docs.blender.org/manual/en/dev/editors/clip/introduction.html>`_ の出力から作成されます。
Movie Clip Editor でメディア (ビデオまたは画像) を開いていない限り、VSE の [Clip] メニューには何も表示されません。
それ以外の場合は、単なる空白のメニューです。
SceneおよびMaskとともに、Clip ストリップは、ストリップのソースが Blender 内で生成される必要があるグループを形成します。
クリップ ストリップ バーのデフォルトの色は :clip:`███` です。

Movie Clip Editor は、モーション トラッキングや高度なマスキングなどの高度な編集に使用されます。



Options
=======

.. note::
   .. Panels documented elsewhere!
   パネルは他の場所で文書化されています。

   ..
    The following panels are identical to those from the Movie strip:
    :ref:`Compositing <compositing-panel>`, :ref:`Transform <transform-panel>`,
    :ref:`Crop <crop-panel>`, :ref:`Color <color-panel>`, :ref:`Time <time-panel>` and :ref:`Custom <custom-panel>`.
   ..
   次のパネルはムービー ストリップのものと同じです:

   - :ref:`Compositing <compositing-panel>`
   - :ref:`Transform <transform-panel>`
   - :ref:`Crop <crop-panel>`
   - :ref:`Color <color-panel>`
   - :ref:`Time <time-panel>`
   - :ref:`Custom <custom-panel>`

..
  There isn't any Source panel because the Clip strip is created from an in-memory data block,
  that on his turn is created in the Movie Clip Editor.
  There can be multiple data blocks and they are stored within the Blend-file upon saving.

  Two extra properties are added to the Video panel.
  The *Strobe* and *Reverse Frames* properties are the same as in the :ref:`Movie Strip <video-panel>`.
..

Clip ストリップは、Movie Clip Editor 上で作成されたデータを メモリ内のデータブロック経由で作成します。
そのため、ソース パネルはありません。
複数のデータ ブロックが存在する可能性があり、それらは保存時に blend ファイル内に保存されます。

2 つの追加プロパティがビデオ パネルに追加されます。
ストロボ プロパティとリバースフレームプロパティは、 :ref:`Movie Strip <video-panel>` のプロパティと同じです。

Video
-----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Video
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-video-strip-clip.png
   :scale: 50%
   :alt: Video Property of Clip Strip
   :align: Right

   図 1: Clip ストリップのビデオ プロパティ

.. Tracker: Stabilize 2D clip
Tracker: 2D クリップを安定化
   .. The purpose of Tracking in the Movie Clip Editor is mostly to stabilize the video.
   .. With this checkbox, you can use the stabilized version of the clip.
   Movie Clip Editor でのトラッキングの目的は、主にビデオを安定させることです。
   このチェックボックスをオンにすると、安定化されたバージョンのクリップを使用できます。

.. Distortion: Undistort clip
Distortion: クリップの歪みを解除
   .. Stabilizing a video is done by moving and rotating the video around the stable anchor point.
   .. With this option, you can remove the distortion of the clip which is the result of stabilizing it.
  ビデオを安定させるには、安定したアンカー ポイントを中心にビデオを移動および回転します。
  このオプションを使用すると、クリップを安定化した結果生じるクリップの歪みを除去できます。
