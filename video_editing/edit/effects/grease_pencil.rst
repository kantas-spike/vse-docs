.. Annotation with Grease Pencil
グリースペンシルによる注釈
-----------------------------
.. To create a Grease Pencil annotation over your footage in the Video Sequence Editor, you need two scenes; one for the Grease Pencil annotation and one for the Video Sequencer. You cannot create the Grease Pencil annotation within the same same scene that contains the video footage. Let's call them GP-scene and VSE-scene. You probably have already the VSE-scene you're working on. The GP-scene can be a Copy Settings of the VSE-scene. This will make the framerate and resolution of both scenes the same; not a requirement though. A camera however is not copied and should be added manually to the GP-scene. Then, add the GP-scene as a scene strip in the VSE-scene (menu Add > Scene) on top of the already existing footage. Of course, because the annotation hasn't been created yet, nothing will appear in the preview.

ビデオ シーケンス エディターで映像にグリース ペンシルの注釈を作成するには、2 つのシーンが必要です。
1 つはグリース ペンシルの注釈用で、もう 1 つはビデオ シーケンサー用です。ビデオ映像が含まれる同じシーン内にグリース ペンシル アノテーションを作成することはできません。
それらを GP シーンと VSE シーンと呼びましょう。おそらく、作業中の VSE シーンがすでにあるでしょう。 GP シーンは、VSE シーンの設定をコピーできます。これにより、両方のシーンのフレームレートと解像度が同じになります。必須ではありませんが。
ただし、カメラはコピーされないため、GP シーンに手動で追加する必要があります。
次に、GP シーンをシーン ストリップとして VSE シーン ([Add]メニュー > [Scen]) の既存のフッテージの上に追加します。もちろん、注釈はまだ作成されていないため、プレビューには何も表示されません。

.. Switch to the GP-scene and open the 2D Animation workspace (see figure 1). Add a new camera. You can add the the to-be-annotated movie as a background of the camera. Select the camera in the Properties panel and search for the panel Background images. Another option is to add the movie as a texture on a plane. This can be easily done with the add-on Images as planes.
GP シーンに切り替えて、2D アニメーション ワークスペースを開きます (図 1 を参照)。新しいカメラを追加します。注釈を付けるムービーをカメラの背景として追加できます。 カメラを選択し[Properties] パネルで、[Background Images] Panelを探しします。
もう 1 つのオプションは、ムービーをプレーン上のテクスチャとして追加することです。これは、アドオンの画像を平面として使用すると簡単に実行できます。

.. You also have to make the canvas background transparent. Otherwise, the background of the GP-scene will completely cover the VSE-scene strip. Switch to the Render Properties in the Properties panel and set the Film property of the GP-scene to Transparent. Put the Current Frame indicator or playhead at frame 1 and add a Grease Pencil object (menu Add > Grease Pencil > Blank). Switch to the Draw mode in Grease Pencil and draw something on the canvas.

キャンバスの背景も透明にする必要があります。そうしないと、GP シーンの背景が VSE シーン ストリップを完全に覆ってしまいます。 [Properties] エディターで [Render]タブ に切り替え、GP シーンの [Film] プロパティを [Transparent] に設定します。現在のフレーム インジケーターまたはPlayheadをフレーム 1 に配置し、グリース ペンシル オブジェクトを追加します (メニューの [Add] > [Grease Pencil] > [Blank])。グリースペンシルの描画モードに切り替えて、キャンバス上に何かを描きます。


.. Figure 1 shows the 2D Animation workspace in Draw Mode.  A yellow box and arrow is drawn on the canvas. Note that the yellow box is keyframed at frame 1 and the arrow at frame 20. Both are visible in the 2D Animation workspace because the current frame is at location 20.

図 1 は、描画モードの 2D アニメーション ワークスペースを示しています。キャンバス上に黄色のボックスと矢印が描画されます。黄色のボックスはフレーム 1 でキーフレームされ、矢印はフレーム 20 でキーフレームされていることに注意してください。現在のフレームが位置 20 にあるため、両方とも 2D アニメーション ワークスペースに表示されます。

.. figure:: /images/video_editing_edit_effects_grease-pencil-1.png
   :alt: 2D Animation workspace

   図1 グリース ペンシル オブジェクトと背景画像を含む 2D アニメーション ワークスペース

.. Switch back to the VSE-scene and to the Video Editing workspace and look for the result. Make sure that Rendered Shading in the View panel of the Properties of the Preview is switched on. You will see the GP drawing on top of the underlying movie.

VSE シーンとビデオ編集ワークスペースに戻り、結果を確認します。プレビューのプロパティのビューパネルでレンダリングシェーディングがオンになっていることを確認してください。下にあるムービーの上に GP 描画が表示されます。

.. Although the Video Editing workspace contains a camera by default, it is not necessary to have one. The Video Sequencer creates its own output based on the added strips.

ビデオ編集ワークスペースにはデフォルトでカメラが含まれていますが、必ずしもカメラを持つ必要はありません。ビデオ シーケンサーは、追加されたストリップに基づいて独自の出力を作成します。

.. figure:: /images/video_editing_edit_effects_grease-pencil-2.png
   :alt: Video Editing workspace

   図 2: (カットされた) シーン ストリップが追加されたビデオ編集ワークスペース

.. As you can see in the Sequencer, the GP-scene is added at about frame 50. The current frame for the scene strip however is frame 17. So, only the yellow box is displayed. From frame 20 on, the arrow will appear.

シーケンサーでわかるように、GP シーンは約フレーム 50 に追加されます。ただし、シーン ストリップの現在のフレームはフレーム 17 です。したがって、黄色のボックスのみが表示されます。フレーム 20 以降に矢印が表示されます。


.. The technique from above only works if you haven't haven't edited the original clip. But, if you have, for example, applied a transformation (e.g. rotation, scale) on the original footage, this technique won't work. Then you need to render out first the edited strip and insert this output into the GP-scene.

上記のテクニックは、元のクリップを編集していない場合にのみ機能します。ただし、たとえば、元の映像に変換 (回転、スケールなど) を適用した場合、このテクニックは機能しません。次に、最初に編集したストリップをレンダリングし、この出力を GP シーンに挿入する必要があります。


.. Multiple annotations
複数の注釈

.. Most of the time, you need more than one annotation in your video project. The workflow becomes then of course a little more complex. You can choose between a few alternatives.

ほとんどの場合、ビデオ プロジェクトには複数の注釈が必要です。もちろん、ワークフローはもう少し複雑になります。いくつかの選択肢の中から選択できます。

.. * You can create one scene for each animation that you need and each animation is then repesented by one scene strip.
* 必要なアニメーションごとに 1 つのシーンを作成でき、各アニメーションは 1 つのシーン ストリップで表されます。
.. * It is also possible to encapsulate several animations within one scene. If the animation is however rather complex, a separate scene is adviseable.
* 1 つのシーン内に複数のアニメーションをカプセル化することもできます。ただし、アニメーションがかなり複雑な場合は、別のシーンを作成することをお勧めします。

   .. * Separate each animation based on a time frame, for example the first animation starts at frame 1, the second at frame 500, the third at frame 1000, .... The scene strip should then be cut (shortcut K or Shft-K) at the correct frames.
   * タイムフレームに基づいて各アニメーションを分離します。たとえば、最初のアニメーションはフレーム 1 で始まり、2 番目のアニメーションはフレーム 500 で始まり、3 番目のアニメーションはフレーム 1000 で始まります。次に、シーン ストリップを正しいフレームでカットする必要があります (ショートカット K または Shft-K)。
   .. * You can also create a different layer for each animation (in the Layers panel of the Grease Pencil property) and keyframe the Set Layer Visibility property (Eye icon in the Layers panel) appropriately. In the example from above, set all Layers invisible at frame 0, and set them visible at respectively frame 1, 500 and 1000.
   * また、アニメーションごとに異なるレイヤーを作成し (グリース ペンシル プロパティの [Layers] パネル)、[Set Layer Visibility] プロパティ ([Layers] パネルの目のアイコン) を適切にキーフレームすることもできます。上の例では、すべてのレイヤーをフレーム 0 で非表示に設定し、それぞれフレーム 1、500、1000 で表示できるように設定します。
   .. * You can reserve a separate Grease Pencil object for each animation. Then you also have to set the Render visibility appropriately.
   * アニメーションごとに個別のグリース ペンシル オブジェクトを予約できます。次に、レンダリングの可視性も適切に設定する必要があります。
