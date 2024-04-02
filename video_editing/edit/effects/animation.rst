.. Animation in VSE
VSE でのアニメーション
----------------

.. Blender is a 2D modeling and animation program. So, animation appears in many different places; for example, rigging, 2D animation (grease pencil), physics simulation  & particle systems and, of course, in the Video Sequence Editor.

Blender は 2D モデリングおよびアニメーション プログラムです。このように、アニメーションはさまざまな場所で登場します。たとえば、リギング、2D アニメーション (グリース ペンシル)、物理シミュレーションとパーティクル システム、そしてもちろんビデオ シーケンス エディターです。

.. Animation in the VSE is exclusively achieved with the use of keyframes. Creating and editing keyframes is fully described in the docs; section `animation & rigging <https://docs.blender.org/manual/en/latest/animation/keyframes/introduction.html>`_.

VSE のアニメーションは、キーフレームを使用してのみ実現されます。キーフレームの作成と編集についてはドキュメントで詳しく説明されています。 参照 `animation & rigging <https://docs.blender.org/manual/en/latest/animation/keyframes/introduction.html>`_。

.. Figure 2 shows the result of a simple Fade In and Out animation (menu Add > Fade > Fade In and Out). The default VSE workspace is adapted so that it is a little easier to work with animations. The default General > Animation workspace is preconfigured for working in 3D view, not for animations within the VSE. In figure 2, the File Browser window of the default VSE workspace (top left) is replaced with the Graph Editor. The Timeline editor (bottom) is somewhat increased in height and also replaced with the Dope Sheet Editor.

図2 は、単純なフェードインおよびフェードアウト アニメーション ( [Add]メニュー > [Fade] > [Fade In and Out]) の結果を示しています。
デフォルトの VSE ワークスペースは、アニメーションの操作が少し簡単になるように調整されています。デフォルトの [General] > [Animation] ワークスペースは、VSE 内のアニメーション用ではなく、3D ビューで作業するように事前構成されています。図 2 では、デフォルトの VSE ワークスペースのファイル ブラウザ ウィンドウ (左上) がグラフ エディタに置き換えられています。タイムライン エディタ (下) の高さが若干増加し、ドープ シート エディタに置き換えられました。

.. figure:: /images/video_editing_edit_effects_animation.svg
   :alt: Animation

   図 1: アニメーションを操作するように調整された VSE ワークスペース

.. As you can see in the Preview window, the strip with the Blender logo is animated. At frame 0, the logo is invisible (opacity = 0). It becomes gradually more visible until it is completely opaque at frame 13 - 14. Then the Fade Out sets in until the logo disappears at frame 26. This is the result of the standard Fade In and Out effect.

プレビュー ウィンドウでわかるように、Blender ロゴの付いたストリップがアニメーション化されています。フレーム 0 では、ロゴは非表示になります (不透明度 = 0)。フレーム 13 ～ 14 で完全に不透明になるまで、徐々に見えやすくなります。その後、フレーム 26 でロゴが消えるまでフェードアウトが開始されます。これは、標準のフェードインおよびフェードアウト効果の結果です。

.. With the setting Show Overlays > F-curves, you can see this Opacity change in the strip background. For more exact numbers, you have to look at the sidebar for the Opacity property. At frame 20 (but also at frame 7) the Opacity is exact 0.500.  You can tell that there is a keyframe at the Opacity attribute because it is colored (see `keyframes <https://docs.blender.org/manual/en/latest/animation/keyframes/introduction.html>`_ for a description of the meaning of the different colors).

[Show Overlays] > [F-curves] を設定すると、ストリップの背景でこの不透明度の変化を確認できます。より正確な数値については、サイドバーの Opacity プロパティを参照する必要があります。フレーム 20 (フレーム 7 でも) では、不透明度は正確に 0.500 です。不透明度アトリビュートに色が付けられているため、キーフレームがあることがわかります(さまざまな色の意味の説明については、 `keyframes <https://docs.blender.org/manual/en/latest/animation/keyframes/introduction.html>`_ を参照してください)。

.. In total, the animation has 4 keyframes: at frame 0 (opacity = 0), 13 (opacity = 1), 14 (opacity = 1) and 26 (opacity = 0). These keyframes are represented by an orange color in the Properties and with small circles in the Dope Sheet (bottom) and Graph Editor (top left). The Dope Sheet is primarily used for basic operations on keyframes: inserting new keyframes (of the same attribute), deleting, moving, scaling, duplicating (copy/paste) keyframes. More information on the Dope Sheet can be found in Editors > `Dope Sheet <https://docs.blender.org/manual/en/latest/editors/dope_sheet/introduction.html>`_ of the docs.

アニメーションには合計 4 つのキーフレームがあります: フレーム 0 (不透明度 = 0)、13 (不透明度 = 1)、14 (不透明度 = 1)、および 26 (不透明度 = 0)。これらのキーフレームは、プロパティではオレンジ色で表され、ドープ シート (下) とグラフ エディター (左上) では小さな円で表されます。ドープ シートは主に、(同じ属性の) 新しいキーフレームの挿入、削除、移動、スケーリング、キーフレームの複製 (コピー/ペースト) など、キーフレームの基本操作に使用されます。 ドープシート の詳細については、ドキュメントの [Editors] > [`Dope Sheet <https://docs.blender.org/manual/en/latest/editors/dope_sheet/introduction.html>`_] を参照してください。

.. The Graph Editor is mostly used to change the timing of the animation. Each keyframe in the Graph Editor has Bezier-like handles from which you can change the appearance of the F-curve. As you can see in the graph the Opacity (of Blender-logo.png) changes in a smooth way from 0 to 1 and back to 0. Dragging the keyframe handles changes the slope of the curve.  More information on the Graph Editor can be found in Editors > `Graph Editor <https://docs.blender.org/manual/en/latest/editors/graph_editor/index.html>`_ of the docs.

グラフ エディタは主にアニメーションのタイミングを変更するために使用されます。グラフ エディターの各キーフレームには、F カーブの外観を変更できるベジェのようなハンドルがあります。グラフでわかるように、(Blender-logo.png の) 不透明度は 0 から 1 に滑らかに変化し、0 に戻ります。キーフレーム ハンドルをドラッグすると、カーブの傾きが変わります。グラフ エディターの詳細については、ドキュメントの [Editors] > [`Graph Editor <https://docs.blender.org/manual/en/latest/editors/graph_editor/index.html>`_]を参照してください。

.. Suppose you want the increase the time of the plateau (opacity = 1) of the F-curve. With the default Fade In and Out effect, the animation only stays two frames at maximum opacity. You can select the third keyframe (in Dope Sheet or Graph Editor) but then the F-curve becomes asymmetrical (long increase, short decrease). You can also select keyframes 3 an 4, and drag them to the right.

F カーブの丘 (不透明度 = 1) の時間を長くしたいとします。デフォルトのフェードインおよびフェードアウト効果では、アニメーションは最大の不透明度で 2 フレームだけ留まります。 (ドープ シートまたはグラフ エディタで) 3 番目のキーフレームを選択できますが、F カーブは非対称になります (長く増加し、短く減少します)。キーフレーム 3 と 4 を選択して、右にドラッグすることもできます。

.. To create the animation manually, follow the next steps.
アニメーションを手動で作成するには、次の手順に従います。

..
  1. Select the strip you want to apply the effect on. You cannot add keyframes to multiple strips in one action.
  2. Set the playhead at the very start of the strip; e.g. frame 0.
  3. Set the opacity to 0 in the sidebar Properties.
  4. Hover the mouse cursor over opacity attribute and press I to insert a keyframe. The background of the attribute becomes green.
  5. Move the playhead to the frame 13.
  6. Set the opacity to 1 and set a new keyframe (repeat step 4).
  7. Move the playhead to frame 14 and repeat step 4 (set keyframe on opacity).
  8. Move playhead to the last frame (e.g. frame 26). Change the opacity to 0 and set a keyframe (repeat step 4).
  9.  Repeat step 4-5 for each attribute.
..
1. エフェクトを適用したいストリップを選択します。 1 回のアクションで複数のストリップにキーフレームを追加することはできません。
2. Playhead をストリップの先頭に設定します。たとえばフレーム 0。
3. Sidebarのプロパティで不透明度を 0 に設定します。
4. 不透明度属性の上にマウス カーソルを置き、I キーを押してキーフレームを挿入します。属性の背景が緑色になります。
5. Playheadをフレーム 13 に移動します。
6. 不透明度を 1 に設定し、新しいキーフレームを設定します (手順 4 を繰り返します)。
7. Playheadをフレーム 14 に移動し、ステップ 4 (不透明度にキーフレームを設定) を繰り返します。
8. Playheadを最後のフレーム (フレーム 26 など) に移動します。不透明度を 0 に変更し、キーフレームを設定します (手順 4 を繰り返します)。
9. 属性ごとにステップ 4 ～ 5 を繰り返します。


.. It is possible that the slope of your F-curve is different due to different Preferences. To change these preferences: menu Edit > Preferences > Animation > Default Interpolation. You can also change the Interpolation of this particular F-curve by selecting all keyframes, pressing :kbd:`T` and selecting Bezier.

環境設定の違いにより、F カーブの傾きが異なる可能性があります。これらの環境設定を変更するには、[Edit]メニュー > [Preferences] > [Animation] > [Default Interpolation] を選択します。すべてのキーフレームを選択し、 :kbd:`T` を押してベジェを選択することで、この特定の F カーブの補間を変更することもできます。



.. **Another example**
**もう1つの例**


.. Here's how to create a `Ken Burns effect <https://en.wikipedia.org/wiki/Ken_Burns_effect>`_; to simulate motion from still images.
`Ken Burns effect <https://en.wikipedia.org/wiki/Ken_Burns_effect>`_ を作成する方法は次のとおりです。静止画像から動きをシミュレートします。

.. figure:: /images/video_editing_edit_effects_animation_ken-burns.svg
   :alt: Ken Burns effect


   図 2. Ken Burns 効果の例

..
   1. Select the strip you want to apply the effect on. You cannot add keyframes to multiple strips in one action.
   2. Set the playhead at the very start of the strip.
   3. Zoom in on the image for a wide-angle view.
   4. Hover the mouse cursor over the transform > Scale X attribute in the side bar.
   5. Press I to insert a keyframe. Repeat step 4-5 for the Scale Y attribute; eventually also for the Position X and Y attributes. This action will remember the original zoom-state of the image; eg. the green outline in figure 1.
   6. Move the playhead to the last frame of the still image strip.
   7. Zoom in on the image; eventually reposition the image a bit. This is represented by the red rectangle in figure 1.
   8. Repeat step 4-5 for each attribute.
..

1. エフェクトを適用したいストリップを選択します。 1 回のアクションで複数のストリップにキーフレームを追加することはできません。
2. Playheadをストリップの先頭に設定します。
3. 広角ビューを表示するには、画像をズームインします。
4. マウス カーソルを Sidebar の [Strip]タブ > [Transform]パネル > [Scale X] アトリビュートの上に置きます。
5. I を押してキーフレームを挿入します。 [Scale Y] アトリビュートに対して手順 4 ～ 5 を繰り返します。最終的には位置 X および Y 属性にも適用されます。このアクションは、画像の元のズーム状態を記憶します。例えば。図 1 の緑色の枠線。
6. Playheadを静止画像ストリップの最後のフレームに移動します。
7. 画像を拡大してください。最終的には画像の位置を少し変更します。これは、図2 の赤い四角形で表されます。
8. 属性ごとに手順 4 ～ 5 を繰り返します。

