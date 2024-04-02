Transition
----------

.. A video transition is a post-production technique to connect one shot to another. The simplest transition is a basic cut where the first image is instantly replaced by the next.

ビデオ トランジションは、あるショットを別のショットに接続するためのポストプロダクション技術です。最も単純なトランジションは、最初の画像が次の画像に即座に置き換えられる basic cut です。


.. figure:: /images/video_editing_edit_effects_transition_basic-cut.svg
   :alt: Basic cut

   図1 Sprite Fright の basic cut の例 - Blender Open Movie

.. A basic cut, such as in figure 1, is fine because the image content of the frames is very different and the viewer should have no problem to understand the change in the story ( in this case; it's also a very clever choice because the girl is peeping through a hole in the fence to discover a new world). In other cases, the change in the story is not that obvious and a video transition could help this other point of view.

図 1 のような basic cut は、フレームの画像内容が大きく異なり、視聴者がストーリーの変化を問題なく理解できるため、問題ありません (この場合、これは非常に賢い選択でもあります。フェンスの穴から覗いて新しい世界を発見します。）
場合によっては、ストーリーの変化がそれほど明らかではないため、ビデオのトランジションがこの別の視点に役立つ可能性があります。

.. With the menu Add, shortcut key :kbd:`Shft-A` or the shortcut menu :kbd:`RMB`, you can add transitions to two strips. It is not possible to add transitions to more than two strips at once.

[Add] メニュー、ショートカット キー :kbd:`Shft-A` 、または :kbd:`RMB-Click`で表示されるコンテキストメニューを使用して、2 つのストリップにトランジションを追加できます。一度に 3 つ以上のストリップにトランジションを追加することはできません。

.. The classic and most self-explanatory procedure is to place the two strips on different channels and let them overlap in time. The channels are normally consecutive (e.g. channel 1 & 2), but that has not to be the case.  An extra transition strip is placed at the first free channel above both strips with a run length of the overlap. Each frame of the transition strip is a blending of the two corresponding frames from input 1 and input 2 strip.

古典的で最もわかりやすい手順は、2 つのストリップを異なるチャンネルに配置し、時間内でオーバーラップさせることです。通常、チャネルは連続しています (例: チャネル 1 と 2) が、必ずしもそうである必要はありません。追加のトランジション ストリップは、オーバーラップのランレングスを持つ両方のストリップの上の最初のフリー チャネルに配置されます。トランジション ストリップの各フレームは、入力 1 および入力 2 ストリップの 2 つの対応するフレームをブレンドしたものです。

.. figure:: /images/video_editing_edit_effects_transition_add-methods.svg
   :alt: Add methods

   図2 2 つのストリップ間にトランジションを追加する 2 つの方法

.. In order not to occupy additional channels, you can put the two input strips also on the same channel and leave a small gap between them. The gap will then be filled with the transition strip (see figure 2, second method). The gap can be zero frames, in other words, the input strips are placed next to each other. After adding the transition, nothing seems to be happened. However, the transition strip is created and if you drag the End handle of the first strip or the Start handle of the second strip, the transition strip will appear between the two strips.

追加のチャンネルを占有しないようにするために、2 つの入力ストリップを同じチャンネルに配置し、それらの間に小さなギャップを残すことができます。次に、ギャップはトランジション ストリップで埋められます (図 2、2 番目の方法を参照)。ギャップはゼロフレームにすることもできます。つまり、入力ストリップは互いに隣り合って配置されます。トランジションを追加した後、何も起こっていないようです。ただし、トランジション ストリップが作成され、最初のストリップの終了ハンドルまたは 2 番目のストリップの開始ハンドルをドラッグすると、トランジション ストリップが 2 つのストリップの間に表示されます。


.. This is also how you have to shorten or lengthen the transition strip. You cannot change the Duration of the strip it self. The Duration is determined by the overlap of the two input strips. So, by dragging the handles of the input strips, and therefore changing the overlap, the length of the transition is likewise changed..

これは、トランジション ストリップを短くしたり長くしたりする方法でもあります。
ストリップ自体のデュレーションを変更することはできません。デュレーションは 2 つの入力ストリップの重なりによって決まります。したがって、入力ストリップのハンドルをドラッグしてオーバーラップを変更すると、トランジションの長さも同様に変更されます。

.. important::
   .. If the strips are still images, the content of both images is used to create the transition. Each frame in the transition is a combination of the same two images. If the two strips are movies, each frame in the transition contains a combination of the corresponding images in the offset range.
   ストリップが静止画像の場合、両方の画像のコンテンツを使用してトランジションが作成されます。トランジション内の各フレームは、同じ 2 つの画像を組み合わせたものです。 2 つのストリップがムービーの場合、トランジション内の各フレームには、オフセット範囲内の対応する画像の組み合わせが含まれます。

   .. figure:: /images/video_editing_edit_effects_transition_blending.svg
      :alt: Transition with Strip Offset


      図3 ストリップ オフセット開始または終了を使用したスト​​リップ上のトランジション


   .. In figure 3, the second frame in the transition is a combination of the corresponding images (E & 1) in the offset range. For the first and last frame in the transition, there is only one corresponding image in the Offset. The second image is filled in with the last used image (1 & E).
   図 3 では、トランジションの 2 番目のフレームは、オフセット範囲内の対応する画像 (E と 1) の組み合わせです。トランジションの最初と最後のフレームでは、オフセット内に対応する画像が 1 つだけあります。 2 番目のイメージには、最後に使用されたイメージ (1 および E) が入力されます。

.. figure:: /images/video_editing_edit_effects_transition-direction.png
   :alt: Switch direction of transition
   :scale: 50%
   :align: right

   図4 スイッチの方向

.. The order of selection of the two strips is important for the direction of the transition; e.g. from strip-1 to strip-2 or vice versa. The active strip (the one with the white rectangle) is the target strip; the transition runs from the non-active (but selected) strip to the active strip. In other words, the non-active strip is assigned to Input 1 and the active strip is assigned to Input 2. You can always change the direction of the transition by switching the Input 1 and Input 2 field in the side bar (see figure 4 and 5). You can also use the shortcut :kbd:`Alt-S` or :kbd:`RMB menu`  and Effect Strip > Change Effect Input > A --> B.

2 つのストリップの選択順序は、トランジションの方向にとって重要です。たとえば、ストリップ 1 からストリップ 2 へ、またはその逆。アクティブなストリップ (白い四角形のストリップ) がターゲット ストリップです。トランジションは、非アクティブな (ただし選択されている) ストリップからアクティブなストリップまで実行されます。つまり、非アクティブなストリップは入力 1 に割り当てられ、アクティブなストリップは入力 2 に割り当てられます。サイド バーの [入力 1] フィールドと [入力 2] フィールドを切り替えることで、いつでもトランジションの方向を変更できます (図 4 を参照)および5）。ショートカット  :kbd:`Alt-S` または :kbd:`RMB-Click` によるコンテキストメニュー使用し て、[Effect Strip] > [Chnage Effect Input] > [A --> B] を使用することもできます。


.. figure:: /images/video_editing_edit_effects_transition_direction.svg
   :alt: Direction of transition

   図5 遷移の方向 (入力 1 対入力 2)

Cross & Gamma Cross Fade
........................

.. The Cross and Gamma Cross effect is a dissolve between the Red, Green and Blue color component and the alpha of the input 1 and input 2 strip. The input 1 strip is faded out (starts fully opaque and becomes gradually more transparent). The input 2 strip starts the transition fully transparent and becomes fully opaque. So, the second strip in time should be the input 2 strip; otherwise there will be a glitching effect.

Cross および Gamma Cross Fade エフェクトは、赤、緑、青のカラー コンポーネントと入力 1 および入力 2 ストリップのアルファの間のディゾルブです。
入力 1 ストリップはフェードアウトします (最初は完全に不透明で、徐々に透明になります)。入力 2 ストリップは完全に透明な状態でトランジションを開始し、完全に不透明になります。したがって、時間内の 2 番目のストリップは入力 2 ストリップである必要があります。そうしないと、グリッチ効果が発生します。

.. Figure 6 has two color strips with the following color:
図 6 には、次の色の 2 つのカラー ストリップがあります。

.. * strip-1: RGBA(1,0,0,0.4); red color with alpha = 0.4
.. * strip-2: RGB(0,1,0, 0.6); green color with alpha = 0.6
* strip-1: RGBA(1,0,0,0.4); red color with alpha = 0.4
* strip-2: RGB(0,1,0, 0.6); green color with alpha = 0.6

.. figure:: /images/video_editing_edit_effects_transition_cross.svg
   :alt: Cross Fade

   図6 2 つの色のクロス フェード (ストリップ 1 とストリップ 2 は両方とも PNG イメージです)

.. The Cross fade takes 4 frames and the playhead is at the second frame. So, the Red component of the Cross fade has to go from 1 (input 1) to 0 (input 2) and the Green component from 0 (input 1) to 1 (input 2). The Blue component does not change between input 1 and input 2 and the alpha value goes from 0.4 to 0.6. To make this transition, the effect has 4 frames available. So, the Red component should be decremented by 0.25 each frame and the Green component should be incremented with the same value. The alpha should increment with 0.05 each frame.

クロス フェードには 4 フレームかかり、Playheadは 2 番目のフレームにあります。したがって、クロス フェードの赤コンポーネントは 1 (入力 1) から 0 (入力 2) に、緑コンポーネントは 0 (入力 1) から 1 (入力 2) に変化する必要があります。青コンポーネントは入力 1 と入力 2 の間で変化せず、アルファ値は 0.4 から 0.6 になります。このトランジションを行うために、エフェクトには 4 つのフレームが使用可能です。したがって、赤のコンポーネントはフレームごとに 0.25 ずつ減分し、緑のコンポーネントは同じ値で増分する必要があります。アルファはフレームごとに 0.05 ずつ増加する必要があります。

.. As you can see in figure 6, at the second frame, the Red component = 0.74902 and the Green component = 0.24706 (+- 0.25 ). The alpha = 0.4471 or is incremented by about 0.05.

図 6 からわかるように、2 番目のフレームでは、赤の成分 = 0.74902、緑の成分 = 0.24706 (+- 0.25 ) です。アルファ = 0.4471、つまり約 0.05 ずつ増加します。

.. note::
   .. The alpha value of Color strips is *not* taken into account. The Cross Fade strip has always an alpha = 1, regardless the opacity of the input Color strips. Although the strips in figure 5 seems to be Color strips, they are in realty PNG's with an alpha channel.
   カラー ストリップのアルファ値は考慮されません。クロス フェード ストリップは、入力カラー ストリップの不透明度に関係なく、常に alpha = 1 になります。図 5 のストリップはカラー ストリップのように見えますが、実際にはアルファ チャネルを持つ PNG です。

.. Of course, this is done for each pixel in the preview window. The transition effect is applied *after* all transformations (crop, scale, modifiers, ...) on the input strips.

もちろん、これはPreview ウィンドウ内のピクセルごとに行われます。トランジション エフェクトは、入力ストリップのすべての変換 (crop, scale, modifiers など) の後に適用されます。

.. The Cross and Gamma Cross fade are very similar. According to the docs: "Gamma Cross uses color correction in doing the fade, resulting in a smooth transition that is easier on the eye".

クロスフェードとガンマクロスフェードは非常に似ています。ドキュメントによると、「ガンマ クロスはフェードを実行する際に色補正を使用するため、目に優しいスムーズな移行が実現します。」

.. todo::
   .. To be elaborated.
   詳しく説明する。

Wipe
....

.. figure:: /images/video_editing_edit_effects_wipe-properties.png
   :alt: Wipe properties
   :scale: 50%
   :align: right

   図7 ワイプトランジションのプロパティ

.. In a Wipe transition, two shots are connected with some sort of sliding animation. It looks as if one shot is wiped out to reveal the next one. The Wipe transition can be easily overdone; so use it sparingly and only to enhance the content. For example in a falling scene, the vertical wipe can strengthen the movement.
ワイプ トランジションでは、2 つのショットが何らかのスライド アニメーションで接続されます。まるで 1 つのショットが消えて次のショットが現れるかのように見えます。ワイプ トランジションは簡単にやりすぎてしまう可能性があります。したがって、コンテンツを強化する目的でのみ使用し、慎重に使用してください。例えば落下シーンでは縦ワイプで動きを強化できます。

.. The Effect Strip Input 1 and Input 2 properties are already covered above; see figure 5 for an explanation. Remember that the first frames of the transition resembles more the Input 1 and the last frames more the Input 2 strip.
エフェクト ストリップの入力 1 と入力 2 のプロパティについてはすでに上で説明しています。説明については、図 5 を参照してください。トランジションの最初のフレームは入力 1 に似ており、最後のフレームは入力 2 ストリップに似ていることに注意してください。

Transiton Type:
  .. There are four types of Wipe transitions; each with a Fade In or Out direction; resulting in 8 different variants (see figure 8).
  ワイプ トランジションには 4 つのタイプがあります。それぞれにフェードインまたはフェードアウトの方向があります。その結果、8 つの異なるバリアントが生成されます (図 8 を参照)。

  ..
    * Single: reveals the next strip by uncovering it in a straight line moving across the image. The Direction Out corresponds with a top to bottom or left to right (depending on the angle) reveal.
    * Double: similar to Single, but uses two lines either starting from the middle of the image or the outside. Like the blink of an eye; opening or closing, depending of the direction of the transition. With direction Out, Input strip 2 starts small at the middle of the frame and becomes larger.
    * Iris: reveals the next strip through an expanding (or contracting) circle. Like the aperture of a camera or pupil of an eye. You can blur the transition, so it looks like ink bleeding through a paper.
    * Clock: like the hands of an analog clock, it sweeps clockwise or (if Wipe In is enabled) counterclockwise from the 9:00 position. As it sweeps, it reveals the next strip.
  ..
  * Single: 画像上を直線的に移動して次のストリップを明らかにします。 Direction Out は、上から下、または左から右 (角度に応じて) のリビールに対応します。
  * Double: シングルと似ていますが、画像の中央または外側から始まる 2 本の線を使用します。瞬きのように。トランジションの方向に応じて、開閉します。方向が Out の場合、入力ストリップ 2 はフレームの中央で小さく始まり、大きくなります。
  * Iris: 拡大 (または縮小) する円を通して次のストリップを表示します。カメラの絞りや目の瞳孔のようなものです。トランジションをぼかして、インクが紙ににじんでいるように見せることができます。
  * Clock: アナログ時計の針のように、9 時の位置から時計回りまたは (ワイプインが有効な場合) 反時計回りに動きます。スイープすると、次のストリップが表示されます。

  .. figure:: /images/video_editing_edit_effects_transition_direction-in-out.svg
    :alt: Direction In Out

    図 8: 8 つのトランジション バリアント (4 種類 x 2 方向)

.. Direction: controls whether to fade In or Out. See figure 8 for the movement that corresponds with the In or Out direction.
Direction:
  フェードインするかフェードアウトするかを制御します。イン方向またはアウト方向に対応する動きについては、図 8 を参照してください。

.. Blur Width: in figure 8, the border of the sweeping line is very sharp (from green to red in one pixel. You can however blur this line, resulting in a more smooth gradient from the two colors. The width is specified in percentage of the the width of total image.
Blur Width:
  図 8 では、掃引線の境界線が非常に鮮明です (1 ピクセル内で緑から赤まで)。ただし、この線をぼかすことができ、2 つの色のより滑らかなグラデーションが得られます。幅はパーセントで指定されます。画像全体の幅。

.. Angle: controls the angle of the line for Single and Double transition types. An angle of -45° will show a sweeping triangle from top left to bottom right.
Angle:
  シングルおよびダブルトランジションタイプの線の角度を制御します。 -45°の角度では、左上から右下に向かって広がる三角形が表示されます。

.. The default Fade automatically calculates a linear fade over the length of the strip. So, if the transition strip is 4 frames, then the Single Fade Type will cover respectively 0, 0.25, 0.50, and 0.75 of the image area for frames 1 to 4 of the transition strip. If the default Fade is not enabled, then you can specify a custom Effect Fader. You can keyframe this field, so that each frame of the transition has a different Fader value. This allows you to create custom ease in or out effects (smaller areas in the beginning and end of the animation).

デフォルトのフェードでは、ストリップの長さ全体にわたって直線的なフェードが自動的に計算されます。したがって、トランジション ストリップが 4 フレームの場合、シングル フェード タイプは、トランジション ストリップのフレーム 1 ～ 4 の画像領域のそれぞれ 0、0.25、0.50、および 0.75 をカバーします。デフォルトのフェードが有効になっていない場合は、カスタムのエフェクト フェーダーを指定できます。このフィールドをキーフレーム化して、トランジションの各フレームに異なるフェーダー値を持たせることができます。これにより、カスタムのイーズインまたはイーズアウト効果 (アニメーションの最初と最後の小さな領域) を作成できます。

Sound Crossfade
...............

.. The Sound Crossfade transition works by animating the Volume of two overlapping Sound strips to evenly fade between them. Because this simply animates a value it does not create a strip like other effects or transitions. To apply the effect however, the two sound strips have to overlap (you cannot use method 2 from figure 1). To see the F-curves and the sound wave form, you have to enable them in Show Overlay (top right) and Display Waveform (bottom). As you can see in figure 9, the cross fade is implemented by keyframing the volume from the initial value to zero and vice versa.

サウンド クロスフェード トランジションは、2 つの重なり合うサウンド ストリップのボリュームをアニメーション化して、それらの間で均等にフェードすることで機能します。これは値をアニメーション化するだけなので、他のエフェクトやトランジションのようなストリップは作成されません。ただし、エフェクトを適用するには、2 つのサウンド ストリップをオーバーラップさせる必要があります (図 1 の方法 2 は使用できません)。 F カーブとサウンド波形を表示するには、[Show Overlay] (右上) と [Display Waveform] (下) でそれらを有効にする必要があります。図 9 からわかるように、クロス フェードは、初期値からゼロへ、またはその逆にボリュームをキーフレーム化することによって実装されます。

.. figure:: /images/video_editing_edit_effects_transition_sound-cross-fade.svg
   :alt: Sound Cross Fade effect

   図9 サウンドのクロスフェード効果

   .. Because both strips in figure 9 have an initial volume = 1, the cross fade goes from 1 to zero for sound-1 and vice versa for sound-2. The animation has an ease in (starting slowly and accelerating) and ease out (slowing down at the end).

   図 9 の両方のストリップの初期ボリュームは 1 であるため、クロス フェードはサウンド 1 では 1 からゼロになり、サウンド 2 ではその逆になります。アニメーションにはイーズイン (ゆっくり始まり加速) とイーズアウト (最後に減速) があります。
