Speed
-----

.. With the Speed Control strip, you can change the apparent speed of an action in a shot. In classic movies, this is done by inserting or skipping frames in the strip.

スピード コントロール ストリップを使用すると、ショット内のアクションの見かけの速度を変更できます。古典的な映画では、これはストリップにフレームを挿入またはスキップすることによって行われます。

.. figure:: /images/video_editing_edit_effects_speed-control-basic-concepts.svg
   :alt: Speed Control Basic concepts

   図1 速度制御 - 基本概念

.. The top strip in figure 1 contains a recording of a 0.5 second motion-trajectory of a red ball, recorded in camera with a frame rate of 24 frames per second (fps). You can create  a copy of this strip with each frame duplicated. This will result in slow-motion (see bottom strip of figure 1) if you preview this strip with the same frame rate (24 fps). The apparent speed of the ball is halved because it takes now 0.5 s or 12 frames for the ball to travel half of the original trajectory.  The mid strip illustrates a time lapse or speed-up. This is done by skipping each other frame in the preview. The trajectory is previewed in 0.25 s, whereas in the original strip half a second was needed. The ball seems to move twice as fast.


図 1 の上部のストリップには、24 フレーム/秒 (fps) のフレーム レートでカメラに記録された、赤いボールの 0.5 秒間の運動軌跡の記録が含まれています。各フレームを複製して、このストリップのコピーを作成できます。このストリップを同じフレーム レート (24 fps) でプレビューすると、スローモーションになります (図 1 の下のストリップを参照)。ボールが元の軌道の半分を移動するのに 0.5 秒または 12 フレームかかるため、ボールの見かけの速度は半分になります。中央のストリップは、タイムラプスまたはスピードアップを示しています。これは、プレビューで他のフレームをスキップすることによって行われます。軌道は 0.25 秒でプレビューされますが、元のストリップでは 0.5 秒かかりました。ボールが2倍の速さで動いているように見えます。


.. note::
   .. The above mentioned method of slow-motion is *not* a real slow-motion (slow-mo). For that, you need different recording and presentation frame rates. When you shoot a video, your camera records the action with a certain frame rate; e.g. 24 or 30 images or frames per second. For a regular replay, your presentation frame rate (Blender's project frame rate) need to be the same as the recording frame rate.

   上記のスローモーションの方法は、本当のスローモーション（スローモーション）ではありません。そのためには、異なる録画フレーム レートとプレゼンテーション フレーム レートが必要です。ビデオを撮影すると、カメラは特定のフレーム レートでアクションを記録します。たとえば、1 秒あたり 24 または 30 の画像またはフレーム。通常の再生では、プレゼンテーション フレーム レート (Blender のプロジェクト フレーム レート) が録画フレーム レートと同じである必要があります。

   .. Suppose however, that the recording frame rate of your camera is 60 fps; so 1 second of actual movement is spread over 60 frames. But, you can import this clip into a Blender project that is set with a 30 fps frame rate. So, in Blender, it will take 2 seconds to play this clip of 60 frames. The movement in the clip seems to be slowed down (1 second of actual movement is spread over 2 seconds of display time). This is real slow-motion; each frame is a real tiny movement. The slo-mo in figure 1 is done by inserting duplicate frames; so only half of the movement in figure 1 is real. The other half never actually took place at that moment in time.

   ただし、カメラの録画フレーム レートが 60 fps であると仮定します。したがって、1 秒の実際の動きは 60 フレームに分散されます。ただし、このクリップを 30 fps のフレーム レートに設定されている Blender プロジェクトにインポートすることはできます。したがって、Blender でこの 60 フレームのクリップを再生するには 2 秒かかります。クリップ内の動きが遅くなっているように見えます (実際の動きの 1 秒が表示時間の 2 秒にまたがっています)。これは本当のスローモーションです。各フレームは本当に小さな動きです。図 1 のスローモーションは、重複したフレームを挿入することで実行されます。したがって、図 1 の動きの半分だけが実際のものです。残りの半分は、その時点では実際には起こりませんでした。

.. With the Speed Control strip, you can simulate the time lapse or slow motion effect from figure 1. To add a Speed Control strip, you have to select a regular Movie, Image Sequence or Meta strip (in figure 2, this is the Target strip). With the menu :menuselection:`Add --> Effect --> Speed Control`  or :kbd:`Shft A` you can add a Speed control strip (green bar in figure 2). This strip is put above the original target strip and cannot be moved below it (but it can be moved higher up). You can look at it as a modified copy of the target strip, so you can hide the original target strip.

スピード コントロール ストリップを使用すると、図 1 のタイム ラプスまたはスロー モーション効果をシミュレートできます。
スピード コントロール ストリップを追加するには、通常のムービー、イメージ シーケンス、またはメタ ストリップを選択する必要があります (図 2 では、これがターゲット ストリップです) ）。
[Add]メニュー > [Effect] > [Speed Control] を使用するか、:kbd:`Shift-A` で Speed コントロール ストリップ (図 2 の緑色のバー) を追加できます。このストリップは元のターゲット ストリップの上に配置され、その下に移動することはできません (ただし、より上に移動することはできます)。これをターゲット ストリップの変更されたコピーとして見ることができるため、元のターゲット ストリップを非表示にすることができます。

.. figure:: /images/video_editing_edit_effects_speed-control-properties.png
   :alt: Speed control properties
   :scale: 50%
   :align: right

   図2 Speed Controlのプロパティ

Options
.......
.. With the Speed Control strip, you can choose between four methods to create the speed effect: Stretch, Multiply, Frame Number, and Length.
スピード コントロール ストリップを使用すると、ストレッチ、乗算、フレーム番号、長さの 4 つの方法からスピード エフェクトを作成できます。

Stretch
   .. The playback speed is determined by the relationship between the duration of the original target strip (purple strip + offset in fig 2) and its current visible duration (green strip in fig 2).
   再生速度は、元のターゲット ストリップの長さ (図 2 の紫色のストリップ + オフセット) とその現在表示されている長さ (図 2 の緑のストリップ) の関係によって決まります。

   .. * the Speed Control strip is *shorter* the the original target strip: ➽ time lapse or apparent speed-up
   * Speed Control ストリップが ターゲット ストリップよりも短い: ➽ time lapse または見かけのスピードアップ
   .. * the Speed Control strip has the same length as the target strip: ➽ no apparent speed change.
   * Speed Control ストリップ が ターゲット ストリップと同じ長さ: ➽ 明らかな速度変化はありません。
   .. *  the Speed Control strip is *longer* the the original target strip: ➽ slow-motion
   * Speed Control ストリップが ターゲット ストリップよりも長い: ➽ スローモーション

   **Time lapse**

   .. In figure 3, the original target strip has a duration of 100 frames (frame 0 - 99 with values 0 - 99). Dragging the right strip handle to the left will shorten the strip by introducing a Strip Offset End. So, the visible strip and also the Speed Control strip count only 60 frames. The hidden frames of the target strip are marked with a small purple line and indicated with the Strip Offset End field in the side panel.

   図 3 では、元のターゲット ストリップの継続時間は 100 フレームです (フレーム 0 ～ 99、値は 0 ～ 99)。右のストリップ ハンドルを左にドラッグすると、ストリップ オフセット エンドが導入されてストリップが短くなります。したがって、表示されるストリップとスピード コントロール ストリップは 60 フレームのみをカウントします。ターゲット ストリップの非表示のフレームは小さな紫色の線でマークされ、サイド パネルの [Strip Offset End] フィールドで示されます。

   .. figure:: /images/video_editing_edit_effects_speed-control-stretch.png
      :alt: Speed control - stretch option


      図3 Speed Control - フレームをスキップするストレッチ オプション

   .. The Speed Control strip in figure 3 seems to play faster because it skips some frames from the original target strip (e.g. 2, 4, 7, ...). The following frames are shown when playing the Speed Control strip in figure 3.

   図 3 のスピード コントロール ストリップは、元のターゲット ストリップからいくつかのフレーム (例: 2、4、7、…) をスキップするため、より速く再生されるように見えます。図 3 の Speed Control ストリップを再生すると、次のフレームが表示されます。


   0	1	3	5	6	8	10	11	13	15	16	18	20	21	23	25	26	28	30	31	33	35	36	38	40	41	43	45	46	48	50	51	53	55	56	58	60	61	63	65	66	68	70	71	73	75	76	78	80	81	83	85	86	88	90	91	93	95	96	98

   .. The original target strip of 100 frames is squeezed (stretched) into a playback strip of 60 frames. So, several frames are skipped and it seems to play faster.

   100 フレームの元のターゲット ストリップは、60 フレームの再生ストリップに圧縮 (引き伸ばされ??) されます。そのため、いくつかのフレームがスキップされ、より速く再生されるようです。

   .. Which frames are skipped and which are displayed? The following formula is used:
   どのフレームがスキップされ、どのフレームが表示されるのでしょうか?次の式が使用されます。

   ``Speed[i] = Target[(i/speed length) * target length]   (1)``

   .. In figure 3, frame 25 of the Speed Control strip gets the value of frame (25/60) * 100 = 41.67 or (rounded down) frame 41 of the target strip (left panel). In the right panel, frame 45 from the Speed control strip is selected and the preview shows the normally hidden frame (45/60) + 100 = 75 from the target strip.

   図 3 では、速度制御ストリップのフレーム 25 は、フレーム (25/60) * 100 = 41.67、またはターゲット ストリップ (左パネル) の (切り捨て) フレーム 41 の値を取得します。右側のパネルでは、速度コントロール ストリップのフレーム 45 が選択されており、プレビューにはターゲット ストリップの通常は非表示になっているフレーム (45/60) + 100 = 75 が表示されます。

   .. What will happen if you shorten the original target strip even more, for example up to two frames. The first frame of the Speed Control will again contain the value of 0 because 0/2 * 100 = 0 or the first frame in the target strip. The second frame of the Speed Control contains the value of 50 because 1/2 * 100 = frame 50 which contains the value "50". You could argue that if you want to speed up a 100 frame strip to only two frames, you should choose the first and last frame, in stead of the first and mid one.

   元のターゲット ストリップをさらに短くした場合、たとえば最大 2 フレームにするとどうなるでしょうか。 0/2 * 100 = 0、つまりターゲット ストリップの最初のフレームであるため、スピード コントロールの最初のフレームには再び 0 の値が含まれます。 1/2 * 100 = フレーム 50 には値「50」が含まれるため、速度コントロールの 2 番目のフレームには値 50 が含まれます。 100 フレームのストリップを 2 フレームのみに高速化したい場合は、最初と中間のフレームではなく、最初と最後のフレームを選択する必要があると主張する人もいるでしょう。

   **Slow motion**

   .. You can also increase the visual duration of the original strip by dragging the right handle to the right or increasing the Duration field. In figure 4, the Duration is set to 200 frames. This will introduce a Still Offset End (see :doc:`Time panel Movie strip <../montage/striptypes/movie>`); represented by a blueish purple. Because the Speed Control strip is longer than the original target strip, a slow-motion effect should be the result.

   右ハンドルを右にドラッグするか、 [Duration] フィールドを増やすことで、元のストリップの視覚的な継続時間を延長することもできます。図 4 では、Duration が 200 フレームに設定されています。これにより、Still Offset End が導入されます ( :doc:`Time panel Movie strip <../montage/striptypes/movie>` を参照)。青みがかった紫で表現されます。スピード コントロール ストリップは元のターゲット ストリップよりも長いため、スローモーション効果が得られます。

   .. figure:: /images/video_editing_edit_effects_speed-control-stretch-slo-mo.png
      :alt: Speed control with Still Offset End

      図4 Speed Control - フレームを挿入したストレッチ オプション

   .. In figure 4, the Speed Control strip is twice as long as the original target strip. So, each frame in the Target strip has two copies in the Speed Control strip. This will reduce the playback speed effectively to half. For example: frame 80 (in the speed strip) gets the value of 80/200 * 100 = 40. Frame 81 will point to the same target frame (40.5) because each value is rounded down. Frame 82, however, will point to target frame 41 as well as frame 83.

   図 4 では、速度制御ストリップは元のターゲット ストリップの 2 倍の長さです。したがって、ターゲット ストリップの各フレームには、スピード コントロール ストリップに 2 つのコピーがあります。これにより、再生速度が実質的に半分に低下します。たとえば、フレーム 80 (速度ストリップ内) は 80/200 * 100 = 40 の値を取得します。各値は切り捨てられるため、フレーム 81 は同じターゲット フレーム (40.5) を指します。ただし、フレーム 82 はフレーム 83 だけでなくターゲット フレーム 41 も指します。

   .. The effect of the stretch option is controlled by the amount of the *Strip Offset End* or the *Still Offset End*. The Speed Control strip is *not* influenced by a Strip Offset Start, Hold Offset Start, Hold Offset End or Still Offset Start. These Offsets will only change the length of the preview by skipping the first or last frames but will have no effect on the speed.

   ストレッチ オプションの効果は、Strip Offset EndまたはStill Offset Endの量によって制御されます。スピード コントロール ストリップは、ストリップ オフセット スタート、ホールド オフセット スタート、ホールド オフセット エンド、またはスティル オフセット スタートの影響を受けません。これらのオフセットは、最初または最後のフレームをスキップしてプレビューの長さを変更するだけで、速度には影響しません。

   .. tip::
      .. The Stretch option can be very handy if the video and audio strip haven't the same duration; mostly because of a mismatch between the framerate of the strip and the project. A change in video speed is often less noticeable than a change in audio speed (which will influence the pitch).
      ストレッチ オプションは、ビデオとオーディオ ストリップの長さが同じでない場合に非常に便利です。主な原因は、ストリップとプロジェクトのフレームレートの不一致です。ビデオ速度の変化は、オーディオ速度の変化 (ピッチに影響します) よりも目立たないことがよくあります。

      .. For example: a 10 seconds long 30 fps recorded movie has -of course- 10 seconds of audio and 300 visual frames. When you import this movie in a 24 fps project, you will still have 10 seconds of audio; represented by a greenish strip of 240 timeline frames (remember, the project is set to 24 fps). The blueish movie strip however will run for 300 timeline frames and will take 300 / 24 = 12.5 seconds. So, the audio strip is only 10/12.5 = 0.8 of the length of the movie strip. You have to slow-down the movie by setting the duration to 80% or adding a Strip Offset End of 60 frames.

      たとえば、10 秒の長さの 30 fps で録画されたムービーには、もちろん、10 秒のオーディオと 300 のビジュアル フレームが含まれます。このムービーを 24 fps プロジェクトにインポートすると、オーディオは 10 秒残ります。 240 タイムライン フレームの緑がかったストリップで表されます (プロジェクトは 24 fps に設定されていることに注意してください)。ただし、青っぽいムービー ストリップは 300 タイムライン フレームで実行され、300 / 24 = 12.5 秒かかります。したがって、オーディオ ストリップの長さは、ムービー ストリップの長さの 10/12.5 = 0.8 にすぎません。 [Duration] 80% に設定するか、60 フレームの Strip Offset End を追加して、ムービーの速度を下げる必要があります。

Multiply
   .. After selecting the Multiply option in the drop-down, an additional field (Multiply Factor) is shown (see figure 5 - side panel). A Multiply Factor > 1 will speed up the preview. A factor < 1 will slow down the action. If the value = 0 (default) then the preview speed is the same as the presentation speed of the project.

   ドロップダウンで [Multiply] オプションを選択すると、追加フィールド (乗算係数) が表示されます (図 5 - サイド パネルを参照)。 Multiply Factor > 1 にすると、プレビューが高速化されます。係数が 1 未満の場合、アクションが遅くなります。値 = 0 (デフォルト) の場合、プレビュー速度はプロジェクトのプレゼンテーション速度と同じになります。

   **Time lapse**

   .. figure:: /images/video_editing_edit_effects_speed-control-multiply-time-lapse.svg
      :alt: Speed Control with multiply option

      図5 乗算オプションを使用した速度制御 - タイムラプス


   .. The Multiply Factor in figure 5 is 1.5; so, the preview should be 50% faster than the presentation speed (fps).  Each frame in the Speed Control strip represents the duration of 1.5 frames of the target strip. So frame 30 of the Speed control contains the value of target frame 30 * 1.5 = 45. Frame 60 gets the content of target frame 90. Because, some frames are skipped, the Speed Control strip will run out of frames before the end frame. When this occurs, it will just keep repeating the last one; the action appears to freeze. The last frame of the Target Strip (e.g. frame 99) will be displayed at position 99/1.5 = frame 66 of the Speed Control strip. From then on, the preview will always show the value of 99; e.g. the last frame of the target strip.

   図 5 の乗算係数は 1.5 です。したがって、プレビューはプレゼンテーション速度 (fps) より 50% 高速である必要があります。スピード コントロール ストリップの各フレームは、ターゲット ストリップの 1.5 フレームの継続時間を表します。したがって、速度コントロールのフレーム 30 には、ターゲット フレーム 30 * 1.5 = 45 の値が含まれます。フレーム 60 は、ターゲット フレーム 90 の内容を取得します。一部のフレームがスキップされるため、速度コントロール ストリップは、終了フレームの前にフレームが不足します。これが発生すると、最後のものを繰り返し続けるだけになります。アクションがフリーズしているように見えます。ターゲット ストリップの最後のフレーム (フレーム 99 など) は、速度コントロール ストリップの位置 99/1.5 = フレーム 66 に表示されます。それ以降、プレビューには常に値 99 が表示されます。たとえば、ターゲット ストリップの最後のフレームです。

   **Slow motion**

   .. The Speed Control strip in Figure 6 has a Multiply Factor = 0.4. So, the duration of two frames of the target strip is even a little less than the duration of one Speed Control frame. The movie seems to play slower. There isn't even any action until frame 3. Because of this lower playback speed, not all frames from the target strip could be shown in the equal-sized Speed Control strip. The last visible value at frame 99 is 39 (99 * 0.4).

   図 6 の速度制御ストリップの乗算係数は 0.4 です。したがって、ターゲット ストリップの 2 フレームの長さは、1 つのスピード コントロール フレームの長さよりもわずかに短くなります。映画の再生が遅くなったように見えます。フレーム 3 まではアクションすらありません。再生速度が遅いため、ターゲット ストリップのすべてのフレームが同じサイズのスピード コントロール ストリップに表示されるわけではありません。フレーム 99 で表示される最後の値は 39 (99 * 0.4) です。

    .. figure:: /images/video_editing_edit_effects_speed-control-multiply-slow-mo.svg
      :alt: Speed Control with multiply option

      図6 乗算オプションを使用した速度制御 - スローモーション

   **The use of Offsets**

   .. Figure 7 is a special case because there is a Strip Offset Start and End. The Multiply Factor is set to 1.5. As a result of these Offsets, the visual duration of the Speed Control strip is reduced with the sum of both Offsets. The concept of Current Frame (see figure 6, side panel bottom) is very important here. Although the Playhead is located at frame 64 in the timeline, the Current Frame is actually 44. This is the number of frames, from the playhead (64) to the visual Start of the strip (20 or Strip Offset Start). The content of the Target strip, however is only reduced with the strip Offset Start. The first frame (frame 0) of the Target strip has value 20. The previous frames are no longer accessible. But frames 70 - 99 - even if they are not visible - are still accessible. Because of the Multiply factor of 1.5, the action seems to play faster (some frames are skipped).

   図 7 は、ストリップ オフセットの開始と終了があるため、特殊なケースです。乗算係数は 1.5 に設定されます。これらのオフセットの結果、スピード コントロール ストリップの視覚的な継続時間は両方のオフセットの合計で短縮されます。ここでは、現在のフレームの概念 (図 6、サイド パネル下部を参照) が非常に重要です。Playheadはタイムラインのフレーム 64 にありますが、現在のフレームは実際には 44 です。これは、Playhead (64) からストリップの視覚的な開始点 (20 またはストリップ オフセット開始) までのフレーム数です。ただし、ターゲット ストリップのコンテンツは、ストリップのオフセット スタートでのみ削減されます。ターゲット ストリップの最初のフレーム (フレーム 0) の値は 20 です。以前のフレームにはアクセスできなくなります。ただし、フレーム 70 ～ 99 は、表示されていなくてもアクセスできます。乗算係数が 1.5 であるため、アクションの再生が速くなったように見えます (一部のフレームがスキップされます)。

   .. figure:: /images/video_editing_edit_effects_speed-control-multiply-slow-mo-offsets.svg
      :alt: Speed Control with multiply option

      図7 乗算オプションを使用した速度制御 - スローモーションとオフセット

   .. You won't get any visual clues in the effect strip that point to the direction or size of the speed effect. You have to deduce it from the preview.
   エフェクト ストリップには、スピード エフェクトの方向やサイズを示す視覚的な手がかりは得られません。プレビューからそれを推測する必要があります。

.. note::
   .. It is possible to enter and keyframe a negative Multiply value. This will reverse play the strip. See video below, for an example.
   負の乗算値を入力してキーフレームすることができます。これにより、ストリップが逆再生されます。例として、以下のビデオをご覧ください。

.. raw:: html

   <video controls src="/_static/videos/video_editing_edit_effects_speed-control-multiply-negative.mp4" width ="640"></video>

図8 キーフレーム化された乗算係数による速度制御

.. The target strip has a duration of 100 frames (1 - 100). A keyframe is set on the Multiply factor with value = 1 at frame 1 and value = -1 at frame 100. Note that a F-curve appears in the Graph Editor that runs from +1 (frame 1) to -1 (frame 100). It crosses the zero value at about frame 50. So, from frame 50 on, the Multiply factor is negative and the play direction should be reversed. The preview shows a value of about 25. This is because the Multiply factor < 1 in the range 1 -50; so, the speed slows down.

ターゲット ストリップの継続時間は 100 フレーム (1 ～ 100) です。キーフレームは、フレーム 1 で値 = 1、フレーム 100 で値 = -1 の乗算係数に設定されます。+1 (フレーム 1) から -1 (フレーム 100) まで続く F カーブがグラフ エディタに表示されることに注意してください。 ）。およそフレーム 50 でゼロ値と交差します。したがって、フレーム 50 以降、乗算係数は負になり、再生方向は逆転する必要があります。プレビューには約 25 の値が表示されます。これは、1 ～ 50 の範囲で乗算係数が 1 未満であるためです。そのため、速度が遅くなります。


Frame Number
   .. This option provides you with maximum control. For each position of the Current Frame (playhead most of the timeline)), you can specify a frame number from the target strip to display in the Speed Control strip. Because you can :doc:`keyframe </animation/keyframes/index>` this Frame Number value, you are able to specify custom speed profiles. For example, suppose you want a slo-mo effect as in figure 6 *but* only between frames 50 - 69. The other frames (before and after) should play at normal speed. Because the 20 frames between 50 and 69 are played with a Multiplication Factor = 0.4; only 5 frames are actually played and the rest is duplicated and inserted. So, the sequence should be :

   このオプションを使用すると、最大限の制御が可能になります。現在のフレーム (タイムラインのほとんどのPlayhead) の各位置について、速度コントロール ストリップに表示するターゲット ストリップのフレーム番号を指定できます。このフレーム番号の値を :doc:`keyframe </animation/keyframes/index>`  化できるため、カスタムの速度プロファイルを指定できます。たとえば、図 6 のようなスローモーション効果が必要で、フレーム 50 ～ 69 の間のみであるとします。他のフレーム (前後) は通常の速度で再生する必要があります。 50 から 69 までの 20 フレームは乗算係数 = 0.4 で再生されるため、実際に再生されるのは 5 フレームのみで、残りは複製されて挿入されます。したがって、シーケンスは次のようになります。


   .. * Select the Speed Control strip with the option Frame Number and set the playhead at frame 0 (first frame). Normally, it should display the value 0; which is the first frame of the target strip.
   * フレーム番号オプションを使用してスピード コントロール ストリップを選択し、Playheadをフレーム 0 (最初のフレーム) に設定します。通常、値 0 が表示されます。これはターゲット ストリップの最初のフレームです。
   .. * Enter the value 0 in Frame Number. This means that the value to display comes from frame 0 from the Target strip.
   * [フレーム番号] に値 0 を入力します。これは、表示する値がターゲット ストリップのフレーム 0 から取得されることを意味します。
   .. * Keyframe the Frame Number attribute (press I when hovering over the field). The field becomes yellow a an indication of the existence of a keyframe.
   * フレーム番号アトリビュートにキーフレームを設定します(フィールド上にマウスを置いたときに I を押します)。フィールドが黄色になり、キーフレームが存在することを示します。
   .. * Set the playhead to frame 49. The Frame Number attribute is green; indicating that the value is governed by a keyframe that is not changed since. The value is still 0 and the preview is 0.
   * Playheadをフレーム 49 に設定します。フレーム番号属性は緑色です。それ以降変更されていないキーフレームによって値が管理されていることを示します。値は 0 のままで、プレビューも 0 です。
   .. * Change the Frame Number value to 49. The preview changes to 49 and the attribute color changes to brown. Keyframe this value (color changes to yellow)
   * フレーム番号の値を 49 に変更します。プレビューが 49 に変わり、属性の色が茶色に変わります。この値をキーフレーム化します (色が黄色に変わります)。
   .. * Set the playhead to frame 50 and enter the Frame Number 50. Keyframe this value.
   * Playheadをフレーム 50 に設定し、フレーム番号 50 を入力します。この値をキーフレーム化します。
   .. * Set the playhead to frame 69 and enter the Frame Number 55. Keyframe this value.
   * Playheadをフレーム 69 に設定し、フレーム番号 55 を入力します。この値をキーフレーム化します。
   .. * Set the playhead to frame 70 and enter the Frame Number 56. Keyframe this value.
   * Playheadをフレーム 70 に設定し、フレーム番号 56 を入力します。この値をキーフレーム化します。
   .. * Set the playhead to frame 115 and enter the Frame Number 99. Keyframe this value. You have to increase the duration of the strip.
   * Playheadをフレーム 115 に設定し、フレーム番号 99 を入力します。この値をキーフレーム化します。ストリップの継続時間を長くする必要があります。

   .. figure:: /images/video_editing_edit_effects_speed-control-frame-number-example.svg
      :alt: Speed Control with Frame Number option

      図9 フレーム番号オプションによる速度制御

Length
      .. As with the previous option *Frame Number*, this option will display a frame from the target strip but the frame number is specified as a percentage. For example, 50% will result in figure 7 as value 70. The strip length is 100 frames; so half of it is 50 frames. Because of the Strip Offset Start = 20; 50 frames from that point on will result in frame 70.
      前のオプションFrame Numberと同様に、このオプションはターゲット ストリップからのフレームを表示しますが、フレーム番号はパーセンテージで指定されます。たとえば、50% の場合、図 7 の値は 70 になります。ストリップの長さは 100 フレームです。したがって、半分は 50 フレームです。ストリップ オフセットの開始 = 20 のため、そこから 50 フレームすると、フレーム 70 になります。

      .. You can also keyframe this value as in the example from above.
      上の例のように、この値をキーフレーム化することもできます。

Frame Interpolation
   .. Crossfades between frames to reduce screen tearing when the speed is slower than the original frame rate.
   速度が元のフレーム レートよりも遅い場合に、フレーム間のクロスフェードを行い、画面のティアリングを軽減します。


Examples
........

.. Creating a Slow-Motion Effect
スローモーション効果の作成
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,

..
  Select the clip and :menuselection:`Add --> Effect --> Speed Control` effect strip.
  Set the Speed Control option to Multiply and the Speed factor to be the factor by which you want to adjust the speed.
  To cut the displayed speed by 50%, enter 0.5. Now, a 275-frame clip will play at half speed, and thus display only the first 137 frames.

  If you want the remaining frames to show in slow motion after the first set is displayed, double the Length of the source strip (Time Panel > Duration). If you are using a speed factor other than 0.5 then use the formula:
..

クリップを選択し、:menuselection:`Add --> Effect --> Speed Control` エフェクト ストリップを選択します。
[Speed Control] オプションを [Multiply] に設定し、[Speed factor] を速度を調整する係数に設定します。表示速度を 50% 削減するには、0.5 を入力します。 275 フレームのクリップは半分の速度で再生されるため、最初の 137 フレームのみが表示されます。

最初のセットが表示された後、残りのフレームをスローモーションで表示したい場合は、ソース ストリップの長さを 2 倍にします ([Time]パネル > [Duration])。 0.5 以外の速度係数を使用している場合は、次の式を使用します。

``new_length = real_length / speed_factor``



.. Creating a Time-Lapse + Freeze + Slow-mo sequence
タイムラプス + フリーズ + スローモーション シーケンスの作成
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,

.. Action movies often use the effect of a speeded action up until a certain momentum, then a freeze for a few seconds, followed by a slow-motion; e.g. bullets flying, impact, and slow-mo explosion.

アクション映画では、特定の勢いまでスピードを上げたアクション、その後数秒間のフリーズ、その後のスローモーションの効果がよく使用されます。たとえば、弾丸の飛行、衝撃、スローモーションの爆発などです。

.. Suppose, you have a 150 frames sequence. The first 100 frames should be played at twice, the speed. Frame 100 should be freezed for 20 frames, and the following frames (101 - 150) should be played in slow-motion (half of the speed).

150 フレームのシーケンスがあると仮定します。最初の 100 フレームは 2 倍の速度で再生する必要があります。フレーム 100 を 20 フレームの間フリーズし、次のフレーム (101 ～ 150) をスローモーション (半分の速度) で再生する必要があります。

.. You could this easily by splitting the strip into three parts (0-100, 100, and 101-150) and using the techniques described above. You can also accomplish this with one strip and the Frame Number option.

これは、ストリップを 3 つの部分 (0 ～ 100、100、および 101 ～ 150) に分割し、上記のテクニックを使用することで簡単に行うことができます。 1 つのストリップとフレーム番号オプションを使用してこれを実現することもできます。

.. * Place the playhead at frame 0 and keyframe the field Frame Number (to zero).
* Playheadをフレーム 0 に配置し、フィールド「フレーム番号」を (0 に) キーフレームします。
.. * Move the playhead to frame 49, change the value of Frame Number to 99 and keyframe again.
* Playheadをフレーム 49 に移動し、フレーム番号の値を 99 に変更して、再度キーフレームを設定します。
.. * Move the playhead to frame 50, change the value of Frame Number to 100 and keyframe.
* Playheadをフレーム 50 に移動し、フレーム番号の値を 100 に変更してキーフレームを設定します。
.. * Move the playhead to frame 69, leave the value of Frame Number to 100 and keyframe.
* Playheadをフレーム 69 に移動し、フレーム番号の値を 100 のままにしてキーフレームを設定します。
.. * Move the playhead to frame 170, change the value of Frame Number to 150 and keyframe.
* Playheadをフレーム 170 に移動し、フレーム番号の値を 150 に変更してキーフレームを設定します。

.. To get even finer control over your clip timing, you can use the Graph Editor (see figure 10).
クリップのタイミングをさらに細かく制御するには、グラフ エディターを使用します (図 10 を参照)。

.. figure:: /images/video_editing_edit_effects_speed-control-frame-numbers.svg
   :alt: Speed control in combination with Graph Editor

   図10: グラフ エディターと組み合わせた速度制御 (オプションのフレーム番号)

.. The horizontal axis represents the Sequencer timeline. The vertical axis represents the internal frame sequence of the Target strip. As you can see, the first 50 frames in the Sequencer timeline run from frame 0 to frame 99 in the Target strip frame sequence, so, in fact, skipping each other frame. Frame 100 (from the Target strip) remains in place until frame 69 of the Sequencer timeline (=freeze). The slo-mo is illustrated by the fact that you need 100 frames from the Sequencer timeline to play only 50 frames from the internal Target strip frame sequence. Because the original Target strip only took 150 frames on the Sequencer timeline, you have to expand its duration up to 170 (the dark purple region at the right).

横軸はシーケンサーのタイムラインを表します。縦軸は、ターゲット ストリップの内部フレーム シーケンスを表します。ご覧のとおり、シーケンサー タイムラインの最初の 50 フレームは、ターゲット ストリップ フレーム シーケンスのフレーム 0 からフレーム 99 まで実行されるため、実際には各フレームをスキップします。フレーム 100 (ターゲット ストリップから) は、シーケンサー タイムラインのフレーム 69 まで所定の位置に残ります (= フリーズ)。スローモーションは、内部のターゲット ストリップ フレーム シーケンスから 50 フレームだけを再生するのに、シーケンサー タイムラインから 100 フレームが必要であるという事実によって説明されます。元のターゲット ストリップはシーケンサー タイムライン上で 150 フレームしか必要としないため、その継続時間を 170 まで拡張する必要があります (右側の濃い紫色の領域)。

.. While it is possible to keyframe the Multiply factor, usually you want to keyframe the Frame number directly. The curve interpolation is set to Linear by default but you can change it to Bézier to create Ease In and/or OUT effects.

乗算係数をキーフレーム化することは可能ですが、通常はフレーム番号を直接キーフレーム化する必要があります。カーブ補間は​​デフォルトでリニアに設定されていますが、ベジェに変更してイーズイン効果やイーズアウト効果を作成できます。

.. _video_editing-change_fps:

.. Changing Video Frame Rates
ビデオのフレームレートの変更
,,,,,,,,,,,,,,,,,,,,,,,,,,

..
  You can use the speed control to change the frame rate in frames per second (fps) of a video.
  If you are rendering your video to a sequence set, you can effectively increase or decrease the number of individual image files created, by using the Multiply option with the Multiply Factor.
..
速度コントロールを使用して、ビデオのフレーム レート (fps) を変更できます。ビデオをシーケンス セットにレンダリングしている場合は、[Multiply] オプションと [Multiply factor] を使用することで、作成される個々のイメージ ファイルの数を効果的に増減できます。

..
  For example, if you captured a five-minute video at 30 fps and want to transfer that to film, which runs at 24 fps, you would enter a Multiply Factor of 30/24, or 1.25
  (and Enable Frame Interpolation to give that film blur feel).
..
たとえば、5 分間のビデオを 30 fps でキャプチャし、それを 24 fps で動作するフィルムに転送したい場合は、乗算係数に 30/24、つまり 1.25 を入力します (そして、フレーム補間を有効にして、そのフィルムにぼやけた感じ）。

..
  Instead of producing ``5 × 60 × 30 = 9000`` frames, Blender would produce ``9000 / 1.25 = 7200 = 5 × 60 × 24`` frames. In this case, you set a *start* = 1 and *end* = 7200, set your Format output to for example ``jpeg`` 30fps, and image files ``0001.jpg`` through ``7200.jpg`` would be rendered out, but those images cover the entire 9000 frames. The image file ``7200.jpg`` is the same at frame 9000. Be aware that there can be a quality degradation, due to the encoding.

  When you read those images back into your film blend-file at 24 fps, the strip will last exactly 5 minutes.
..

Blender は ``5 × 60 × 30 = 9000`` フレームを生成する代わりに、 ``9000 / 1.25 = 7200 = 5 × 60 × 24`` フレームを生成します。
この場合、開始= 1 および終了= 7200 に設定し、フォーマット出力をたとえば` `jpeg`` 30fps に設定すると、``0001.jpg`` から ``7200.jpg`` までの 画像ファイルがレンダリングされますが、これらの画像は 9000 フレーム全体をカバーします。画像ファイル ``7200.jpg`` のフレーム 9000 は同じです。エンコードにより品質が低下する可能性があることに注意してください。





