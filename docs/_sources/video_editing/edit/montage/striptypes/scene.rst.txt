.. _bpy.types.SceneSequence:

***********
Scene ストリップ
***********

.. Blender is first and foremost a `3D and 2D modeling <https://docs.blender.org/manual/en/dev/index.html>`_ environment. You can create, animate, and render beautiful realistic or stylized 2D and 3D scenes with it. But, instead of rendering out that scene to a video, and then inserting the video file in the sequence editor, you can insert the scene directly. Scene strips are a way to insert the render output of another scene into your sequence. A typical use case is the creation of a 3D logo or an animated intro of your video.

Blender は何よりもまず `3D および 2D modeling <https://docs.blender.org/manual/en/dev/index.html>`_ 環境です。
これを使用して、美しいリアルまたは様式化された 2D および 3D シーンを作成、アニメーション化、レンダリングできます。
ただし、そのシーンをビデオにレンダリングしてから Video Sequence Editor にビデオ ファイルを挿入する代わりに、シーンを直接挿入することができます。
Scene ストリップは、別のシーンのレンダリング出力をシーケンスに挿入する方法です。
典型的な使用例は、ビデオの 3D ロゴやアニメーション イントロの作成です。


.. The :ref:`default <default-color>` color of the scene strip bar is :scene:`███`.
.. The strip length is determined by the Start & End frame of the imported scene (see  `work with scenes <https://docs.blender.org/manual/en/dev/scene_layout/scene/introduction.html#controls>`_ ).

Scene ストリップ バーのデフォルトの色は :scene:`███` です。
ストリップの長さは、インポートされたシーンの開始フレームと終了フレームによって決まります。 (参照 `work with scenes <https://docs.blender.org/manual/en/dev/scene_layout/scene/introduction.html#controls>`_)。

.. important::
   .. Each scene has its *own* Video Sequencer. Scene strips can *not* be used to insert the sequence's own scene. If you have a 3D animation in *scene-1*, you can insert it as a scene strip in *scene-2* but not in *scene-1*.

   各シーンには *自身* の ビデオ シーケンサーがあります。Sceneストリップを使用して、シーケンス自身のシーンを挿入することはできません。 *scene-1* に 3D アニメーションがある場合、それを *scene-2* にScene ストリップとして挿入できますが、 *scene-1* には挿入できません。

Options
=======

.. note::
   .. Panels documented elsewhere!

   パネルは他の場所で文書化されています。

   ..
    The following panels are identical to those from the Movie strip:  :ref:`Compositing <compositing-panel>`, :ref:`Transform <transform-panel>`, :ref:`Crop <crop-panel>`, :ref:`Video <video-panel>`, :ref:`Color <color-panel>`, :ref:`Time <time-panel>` and :ref:`Custom <custom-panel>`.
   ..
   次のパネルは Movieストリップのパネルと同じです。

   - :ref:`Compositing <compositing-panel>`
   - :ref:`Transform <transform-panel>`
   - :ref:`Crop <crop-panel>`
   - :ref:`Video <video-panel>`
   - :ref:`Color <color-panel>`
   - :ref:`Time <time-panel>`
   - :ref:`Custom <custom-panel>`


.. A new property is added to the Time panel: ``Original Frame Range``. As the name indicates, this new property shows the number of frames of the source scene. This field is updated when the source scene changes in length. However, the strip bar length is *not* updated in the sequencer.

新しいプロパティ ``Original Frame Range`` が [Time] パネルに追加されます。名前が示すように、この新しいプロパティはソース シーンのフレーム数を示します。このフィールドは、ソース シーンの長さが変更されると更新されます。ただし、ストリップバーの長さは Sequencer では更新されません。


.. todo::
   .. How can the scene strip length be updated to reflect the actual length of the source scene (same problem as with metastrips).
   ソース シーンの実際の長さを反映するようにシーン ストリップの長さを更新するにはどうすればよいですか (メタストリップと同じ問題)。

.. An entirely new Scene panel is also added.
まったく新しいシーンパネルも追加されます。

Scene
-----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Scene
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-scene.png
   :scale: 50%
   :alt: Scene Property of Scene Strip
   :align: Right

   図1 Sceneのプロパティ

Scene
   .. Clicking the icon lets you pick the source scene; e.g. Scene1 from a drop-down. With the link/unlink button (X), you can remove the chosen source scene. The stripbar becomes red as a visual indication.

   アイコンをクリックすると、ソース シーンを選択できます。たとえば、ドロップダウンから Scene1 を選択します。[link/unlink] ボタン (X) を使用すると、選択したソース シーンを削除できます。視覚的に示すために、ストリップバーが赤になります。

Input
   .. You can choose between Camera or Sequencer. The original source Scene - where the content of this scene strip came from - could also have a Video Sequencer with content in it. Therefore, the output of that scene could be generated from that Video Sequencer or from the camera/compositor of that scene.

   Camera または Sequencer のいずれかを選択できます。この Sceneストリップのコンテンツの元となるソース シーンには、コンテンツを含む Viedeo Sequencerが含まれる場合もあります。したがって、そのシーンの出力は、そのビデオ シーケンサーまたはそのシーンの Camera/Compositor から生成される可能性があります。

   ..
    In the source scene, you choose the `Post Processing panel <https://docs.blender.org/manual/en/dev/render/output/properties/post_processing.html?highlight=post%20processing%20panel>`_ of the Output Properties.
    But, of course, it is not a good habit to change that setting from within another scene.
    So, with this input choice, you can choose between the two possibilities.
   ..
   ソース シーンで、 `Post Processing パネル <https://docs.blender.org/manual/en/dev/render/output/properties/post_processing.html?highlight=post%20processing%20panel>`_ の [Output]プロパティを選択します。
   ただし、その設定を別のシーン内から変更するのは良い習慣ではありません。したがって、この入力を選択すると、2 つの可能性から選択できます。

  ..
   A nice example is illustrated in figure 2. Suppose that you are responsible for the quarterly reporting.
   So, each month, you made a nice video and you used a separate scene for that.
   At the end of the quarter, you want to combine them into an overview video.
   Figure 2 shows your project file. It contains 5 scenes (see figure 2 at the top).
   The sequencer of Scene Overview contains four Scene strips; the three months and an intro.
   From the color, you can deduce that this intro is a text strip.
   You can see this also in the Preview. Scene Month-2 contains one Movie/Sound strip (blue and green color).
   Scene Month-3 contains a Text strip (purple) and a color strip (orange).
   All four scenes have selected the Sequencer as input.
  ..

   良い例を図 2 に示します。あなたが四半期報告書の責任者であると仮定します。毎月、素敵なビデオを作成し、そのビデオに別のシーンを使用しました。
   四半期の終わりに、それらを組み合わせて概要ビデオを作成したいと考えています。図 2 にプロジェクト ファイルを示します。
   これには 5 つのシーンが含まれています (上部の図 2 を参照)。シーン概要の Sequencer には 4 つの Sceneストリップが含まれています。 3か月とイントロ。色から、 このイントロはTextストリップであると推測できます。
   これは Preview でも確認できます。シーン Month-2 には、1 つの Movie/Sound ストリップ (青と緑の色) が含まれています。シーン Month-3 には、Text ストリップ  (紫) と Color ストリップ (オレンジ) が含まれています。 4 つのシーンはすべて入力として Sequencer を選択しています。


   .. figure:: /images/vse_setup_project_striptypes_scene.svg
      :alt: Scene containing scene strips

      図2 4 つのシーン ストリップを含むシーンの概要

  ..
   Although scene strips are a unique feature of Blender against other video editors,
   there are some major annoyances. First, Blender does not store the editor/workspace you're working in.
   For the scene Overview, you are obviously working with the Video Editor.
   For the other scenes, you probably have selected the Modeling Workspace and you're working in the 3D Viewport.
   If you switch from scene Overview to scene Intro,
   you stay in the Video Sequencer and you have to switch manually to the other editor.
   Second, you have no clue where the current frame (you are previewing) is situated in the original scene.
  ..

   Scene ストリップは他のビデオ エディターに比べて Blender 独自の機能ですが、大きな迷惑な点がいくつかあります。
   まず、Blender は作業中のエディタ/ワークスペースを保存しません。
   シーンの概要については、明らかにビデオ エディタで作業しています。
   他のシーンでは、おそらくモデリング ワークスペースを選択し、3D ビューポートで作業していると思います。
   シーンの概要からシーンのイントロに切り替えると、Video Sequencer に留まり、手動で他のエディタに切り替える必要があります。
   第 2 に、(Prevewしている) 現在のフレームが元のシーンのどこにあるのかわかりません。

   ..
    Third, there is also a `Scene Strip Display <https://docs.blender.org/manual/en/dev/video_editing/preview/sidebar.html>`_ panel in the sidebar of the Preview window.
    These settings can influence the display of your scene strip.
    For example, if you want to get the compositor output into the scene strip,
    you have to enable these *four* settings (see also below):
   ..

   3 番目に、プレビュー ウィンドウのサイドバーには `Scene Strip Display <https://docs.blender.org/manual/en/dev/video_editing/preview/sidebar.html>`_ パネもあります。これらの設定は、Scene ストリップの表示に影響を与える可能性があります。
   たとえば、コンポジター出力を Scene ストリップに取得したい場合は、次の4 つの設定を有効にする必要があります

   - Properties > Post Processing > Compositor
   - Compositor > Use Nodes > Checked (両方のオリジナルシーン)
   - View > Scene Strip Display > Rendered
   - Scene Strip > Input > Camera (最後の2つの対象シーン)

   .. Last but not least, the speed of a (complex) scene strip is far from optimal.
   最後に重要なことですが、(複雑な) シーン ストリップの速度は最適とは程遠いです。

Camera
  ..
   The same reasoning holds for multiple cameras. The active camera is set in the original scene.
   But the receiving scene can choose to use another camera.
   If the original scene has multiple cameras, you can choose here which camera to use.
   This is very useful in Multicam-editing.

   Following options ``Show Grease Pencil`` and ``Transparent`` only appear if Camera (see above) has been selected.
  ..
  同じ理由が複数のカメラにも当てはまります。アクティブなカメラは元のシーンに設定されます。
  ただし、受信シーンでは別のカメラの使用を選択できます。元のシーンに複数のカメラがある場合、ここでどのカメラを使用するかを選択できます。これはマルチカム編集に非常に役立ちます。

  以下の ``Show Grease Pencil`` および ``Transparent`` オプションは、Camera(上記を参照) が選択されている場合にのみ表示されます。

   Show Grease Pencil
      .. Shows Grease Pencil in non render preview i.e. Solid mode.
      非レンダリング プレビュー、つまりソリッド モードでグリース ペンシルを表示します。

   Transparent
      .. Creates a transparent background.
      .. This is useful for doing overlays like rendering out Grease Pencil films via the Sequencer.
      透明な背景を作成します。これは、シーケンサーを介してグリース ペンシル フィルムをレンダリングするなどのオーバーレイを行う場合に便利です。

   .. todo::
      .. These two options don't seem to do much.
      これら 2 つのオプションはあまり効果がないようです。

Volume
   .. The volume of the original audio can be increased (> 1) or reduced (< 1) with this setting.
   .. See :doc:`Volume level </video_editing/edit/sound/measuring/volume>` for an interpretation of this volume level.
   この設定では、元のオーディオの音量を上げたり (> 1) 下げたり (< 1) したりできます。
   この音量レベルの解釈については、 :doc:`Volume level </video_editing/edit/sound/measuring/volume>` を参照してください。
