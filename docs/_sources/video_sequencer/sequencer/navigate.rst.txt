.. Navigate
ナビゲーション
........

.. Navigating in your timeline is done by moving the playhead, so that you can see the selected frame in the preview window. The playhead is the blue vertical line with the previewed frame number at the top.

タイムライン内を閲覧するには、Playheadを移動して、選択したフレームをプレビュー ウィンドウに表示します。Playheadは青い縦線で、上部にプレビューされたフレーム番号が表示されます。

.. figure:: /images/editors_vse_sequencer_timeline_playhead.svg
   :alt: Playhead

   図1: Playheadの詳細

.. In figure 1, the playhead is positioned between frame 3 & 4 and indicates with the little blue square at the top that frame 4 is in the Preview window. So, the playhead is always positioned at the start of the previewed frame.

図1 では、Playheadはフレーム 3 と 4 の間に配置されており、上部の小さな青い四角形でフレーム4 がPreviewウィンドウにあることを示しています。したがって、Playheadは常にプレビューされるフレームの先頭に配置されます。


.. |notequal| unicode:: 0x2260

.. Warning::
   .. There could be some confusing regarding the term Current Frame. According to the Strip properties > Time panel, the Current Frame is frame 3, although the playhead and the Preview window show frame 4. This is because the Current Frame field in the Time panel is a relative measure: it is the position of the Playhead relative to the visual start (|notequal| the Start field) of the active strip.

   「現在のフレーム」という用語に関しては、混乱を招く可能性があります。 [Strip プロパティ] > [Time] パネルによると、現在のフレームはフレーム 3 ですが、PlayheadとPreviewウィンドウにはフレーム 4 が表示されます。これは、[Time] パネルの [Current Frame] フィールドが相対的な尺度であるためです。これは、Playheadの位置です。アクティブストリップの視覚的な開始点 (|notequal| Start フィールド) を基準にします。

   .. * In figure 1: playhead is at frame 4; the strip starts at frame 1; Current frame = 3; you have to move 3 frames from the playhead to get at the visual start frame.
   .. * If the strip should start at frame 0, then the Current frame should be 4.
   .. * If the strip starts at frame 5 and the playhead is at frame 8, then the Current Frame = 3.

   * 図1: Playheadはフレーム4 にあり、ストリップはフレーム 1 から始まります。そして、[Current Frame] = 3 です。 ストリップの開始フレームを表示するには、Playheadを3フレーム分動かす必要があります。
   * ストリップがフレーム 0 から開始していれば、[Current Frame] は 4 であるはずです。
   * ストリップがフレーム 5 から開始していれば、Playheadはフレーム8にあり、[Current Frame] は 3 であるはずです。

.. Jumping
ジャンピング
,,,,,,,

.. Jumping to a specific frame
特定のフレームへのジャンプ
   .. The Playhead can be set or moved to a new position by pressing or dragging with the  :kbd:`LMB` in the scrubbing area at the top of the timeline. This is the area with the frame numbers or time codes.
   Playheadは、タイムライン上部のスクラブ領域で :kbd:`LMB` を押すかドラッグすることで、新しい位置に設定または移動できます。スクラブ領域はフレーム番号またはタイムコードが記載されている領域です。

   .. This can also be done by pressing or dragging with the  :kbd:`Shift RMB` in the scrubbing area of the sequencer. The scrubbing area of the sequencer is the entire area, including the existing strip bars. See figure 2 for a visualization of the scrubbing areas.
   この操作は、Sequencerのスクラブ領域で :kbd:`Shift RMB` を押すかドラッグすることによっても実行できます。Sequencerのスクラブ領域は、既存のストリップ バーを含む領域全体です。スクラブ領域については、図2 を参照してください。

   .. The playhead can be set to a specific frame by entering the frame number in the Current Frame field of the Timeline Editor; usually at the very bottom right hand side.
   タイムライン エディタの [Current Frame] フィールドにフレーム番号を入力することで、Playheadを特定のフレームに設定できます。通常は右下にあります。

.. Moving frame by frame
フレームごとに移動する
   .. The Playhead can be moved in single-frame increments by pressing the cursor keys :kbd:`Left` or :kbd:`Right`.
   カーソルキーの :kbd:`Left` や :kbd:`Right` を押すと、Playheadを 1 フレームずつ移動できます。

   .. Rolling with the :kbd:`MMB` while holding :kbd:`Alt` (:kbd:`Alt-Wheel`) will also move the playhead frame by frame.
   :kbd:`Alt` を押しながら :kbd:`MMB` を回転させると、Playhead がフレームごとに移動します。

.. Jump to boundaries
境界にジャンプする
   .. You can jump to the Frame Start or Frame End of the project by pressing :kbd:`Shift-Left` or :kbd:`Shift-Right`. These two fields are set in the Properties Editor > Dimensions panel or in the Timeline Editor (bottom right).

   :kbd:`Shift-Left` または :kbd:`Shift-Right` を押すと、プロジェクトのフレーム開始位置またはフレーム終了位置にジャンプできます。
   これらの2つのフィールドは、[Properties Editor] > [Dimensions] パネル [#f1]_ または Timeline Editor (右下) で設定します。

   .. The same could be done by clicking the Jump to Endpoint transport controls in the Timeline Editor
   Timeline Editorの Transport コントロールにある[Jump to Endpoint]ボタン をクリックしても、同じことができます。

   .. Pressing :kbd:`PgUp` or :kbd:`PgDn` will move the playhead to the start of the next or previous strip (over all channels). The same could be obtained by holding :kbd:`Ctrl` *after* you have started dragging with the :kbd:`LMB` in the scrubbing area of the timeline.
   :kbd:`PgUp` または :kbd:`PgDn` を押すと、Playhead が次または前のストリップ(すべてのチャンネルにわたる)の先頭に移動します 。
   タイムラインのスクラブ領域でを :kbd:`LMB` 使用してドラッグを開始した後、:kbd:`Ctrl` を押し続けることによっても同じことができます。

   .. Pressing :kbd:`Alt PgUp` or :kbd:`Alt PgDn` will move the playhead to the *center* of the next or previous strip (over all channels).
   :kbd:`Alt PgUp` または :kbd:`Alt PgDn` を押すと、Playheadが次または前のストリップ（すべてのチャンネルにわたる）の中央に移動します。

.. Scrubbing
スクラブ
,,,,,,,,,

   .. Scrubbing is used to quickly review a project in the preview window, without much concern about the exact timing. This can be a very processor intensive job: jumping around and previewing dozens of frames within a split of a second. So, there can be some lag or stuttering. The use of :doc:`proxies </video_editing/setup/proxies>` (eventually with a very low resolution) is indicated here.

   スクラブは、正確なタイミングをあまり気にせずに、Preview ウィンドウでプロジェクトをすばやく確認するために使用されます。これは、1 秒以内に数十のフレームを飛び回ったりプレビューしたりするため、非常にプロセッサを集中的に使用するジョブになる可能性があります。そのため、多少の遅れや途切れが発生する可能性があります。:doc:`proxies </video_editing/setup/proxies>` の使用(最終的には非常に低い解像度になります) がここに示されています。

   .. Scrubbing is done by dragging with the :kbd:`LMB` in the scrubbing area (see figure 2, yellow text and arrows) at the top of the timeline or with the :kbd:`Shift RMB` in the scrubbing area of the sequencer (see figure 2, orange text).

   スクラブは、タイムラインの上部にあるスクラブ領域 (図 2、黄色のテキストと矢印を参照) で :kbd:`LMB` を使用してドラッグするか、Sequencerのスクラブ領域 (図 2、オレンジ色のテキストを参照) で :kbd:`Shift RMB` をドラッグして実行します。

   .. figure:: /images/editors_vse_sequencer_timeline_scrubbing.svg
      :alt: Scrubbing area

      図2: スクラブ領域

   .. As can be seen in figure 2, you can use *both* timelines: from the sequencer at the top or from the Timeline Editor at the bottom. Scrubbing at the timeline at the bottom will also move the playhead at the top. Please note, that both timelines are also synced (same frame range, same playhead position). For this, you need to set the option ``Sync Visible Range`` under the View menu for both timelines.

   図2 からわかるように、上部のSequencer または下部のTimeline Editorから、両方のタイムラインを使用できます。下部のタイムラインをスクラブすると、上部のPlayheadも移動します。両方のタイムラインを同期 (同じフレーム範囲、同じPlayhead位置)させる場合、 *両方* のタイムラインの [View]メニューで[``Sync Visible Range``]でオプションを設定する必要があることに注意してください。

   .. When you drag with :kbd:`Shift-RMB` directly on a sequence strip, this will show the strip *solo*, temporarily disregarding effects and other strips, showing only this strip's output (indicated with the white text and arrows in figure 2). For example, if you have two color strips on top of each other, normally you see the strip from the highest channel in the Preview window. Drag with :kbd:`Shift-RMB` on the lower color strip will show only this color strip in the Preview window. This works also with sound. :kbd:`Shift-RMB` on the sound strip will only produce the audio.

   Sequencerのストリップ上で :kbd:`Shift-RMB` を直接ドラッグすると、ストリップ *ソロ* が表示され、エフェクトや他のストリップは一時的に無視され、このストリップの出力のみが表示されます (図2 の白いテキストと矢印で示されています)。
   たとえば、2つのカラー ストリップが重なっている場合、通常はPreviewウィンドウで最上位のチャンネルのストリップが表示されます。下のカラーストリップを :kbd:`Shift-RMB` で ドラッグすると、このカラーストリップのみがPreviewウィンドウに表示されます。これはサウンドでも機能します。サウンドストリップでは音声のみが生成されます。

   .. Dragging the strip handle will normally shrink or extend the strip but will not change the Preview (you keep viewing the frame at the playhead). With the option *Preview during Transform* of the Preview window set, dragging the handle will also display the frame at the position of the handle.

   通常、ストリップ ハンドルをドラッグするとストリップが縮小または拡張されますが、Previewは変更されません (Playheadのフレームを表示し続けます)。Previewウィンドウの[View]メニュー > [*Preview during Transform*]オプション を設定すると、ハンドルをドラッグ時にハンドル位置のフレームも表示されます。

.. Playing
再生
,,,,,,,

   .. The Transport controls are located at the very bottom of the Video Editor workspace. They are part of the Timeline Editor. They could also be integrated with the Sequencer; see :doc:`Video Editing Workspace </video_editing/setup/workspace>`.

   Transportコントロールは、Video Editor workspace の最下部にあります。これらはTimeline Editorの一部です。これらは Sequencer と統合することもできます。参照 :doc:`Video Editing Workspace </video_editing/setup/workspace>`

   .. figure:: /images/editors_vse_sequencer_timeline_transport-controls.png
      :alt: Transport controls
      :align: center


      図5: Transportコントロール

   .. These controls are probably self-explanatory. Pressing the Play/Reversed Play button will start playing the movie from the playhead in forward or reversed direction. The shortcut key is :kbd:`Spacebar` for play forward. The shortcut :kbd:`Shift - Ctrl - Spacebar` is for reversed play.

   これらのコントロールはおそらく一目瞭然です。再生/逆再生ボタンを押すと、Playheadから順方向または逆方向で動画の再生が開始されます。順方向に再生するためのショートカットキーは :kbd:`Spacebar` キーです。:kbd:`Shift - Ctrl - Spacebar` は逆再生のショートカットです。

   .. note::
      .. When installing Blender for the first time, you have to enter some basic choices, e.g. the function of the spacebar (in previous versions it was assigned the Help function). You can check or reset this in User Preferences > Keymap > Spacebar Action.

      Blender を初めてインストールするときは、:kbd:`Spacebar` の機能など、いくつかの基本的な選択肢を入力する必要があります (以前のバージョンでは、ヘルプ機能が割り当てられていました)。これは、[User Preferences] > [Keymap] > [Spacebar Action] で確認またはリセットできます。 [#f2]_

   .. When the movie is playing, the Play button is replaced with a Pauze button. Pressing the spacebar also toggles between Play and Pauze.
   ムービーの再生中、再生ボタンは一時停止ボタンに置​​き換えられます。:kbd:`Spacebar` を押すと、再生と一時停止が切り替わります。

   .. The Jump to Keyframe buttons will only work when there are keyframes in the timeline.
   [Jump to Keyframe] ボタンは、タイムラインにキーフレームがある場合にのみ機能します。

   .. todo::
      .. Insert link to section about keyframes
      キーフレームに関するセクションへのリンクを挿入

   .. The Jump to Endpoint buttons will bring the playhead to the first or last frame in the Framerange (see :doc:`Project settings  </video_editing/setup/project-settings>`). The shortcut keys are: :kbd:`Shift Leftarrow` or :kbd:`Shift Rightarrow`.

   [Jump to Endpoint] ボタンを使用すると、Playheadがフレーム範囲の最初または最後のフレームに移動します (参照 see :doc:`Project settings  </video_editing/setup/project-settings>`)。ショートカットキーは :kbd:`Shift Leftarrow` または :kbd:`Shift Rightarrow` です。


.. Playback settings
Playback設定
,,,,,,,,,,,,,,,,,

.. role:: red
.. figure:: /images/editors_vse_sequencer_timeline_playback-menu.png
   :alt: Playback menu
   :scale: 40%
   :align: right

   図3: Playbackメニュー

.. In the top left corner of the Preview window, you can find the ongoing framerate e.g. :red:`23 fps` during playback. A red number indicates that the running framerate is slower than the framerate set by the project.

Previewウィンドウの左上隅に、再生中の進行中のフレームレート (例: :red:`23 fps`) が表示されます。赤い数字は、実行中のフレームレートがプロジェクトで設定されたフレームレートよりも遅いことを示します。

高負荷時などの再生の動作設定は、Timelineウィンドウの左側にある[Playback]メニューで設定できます。

Sync
   .. - *Play Every Frame*: plays every frame even if playback is slow; the framerate can drop beneath the desired fps.
   .. - *Frame Dropping*: Drop frames if playback becomes slower than the scene’s frame rate. Under high pressure, this will become very noticeable as apparent jumps within the movie.
   .. - *Sync to Audio* (default): drop frames if playback becomes too slow to remain synced with audio.

   - *Play Every Frame*: 再生が遅い場合でもすべてのフレームを再生します。フレームレートが希望の fps を下回る可能性があります。
   - *Frame Dropping*: 再生がシーンのフレームレートより遅くなった場合、フレームをドロップします。高負荷時では、これは動画のコマ落ちとして非常に目立ちます。
   - *Sync to Audio* (default): 再生がシーンのフレームレートより遅くなった場合、フレームをドロップします。

Audio
   .. - *Scrubbing*: scrubbing a timeline with audio strips can sometimes be annoying. The sound is distorted, due to the speed of scrubbing. You can toggle on or off the audio while scrubbing with this option.
   .. - *Mute*: with this option, you can mute the sound of *all* sound strips.
   - *Scrubbing*: オーディオ ストリップを使用してタイムラインをスクラブするのは、煩わしい場合があります。スクラブの速度が速いため、音が歪みます。このオプションを使用すると、スクラブ中にオーディオのオンとオフを切り替えることができます。
   - *Mute*: このオプションを使用すると、すべてのサウンド ストリップのサウンドをミュートできます。

Playback
   .. - *Limit to Frame Range*: don’t allow selecting frames outside of the playback range using the mouse.
   .. - *Follow Current Frame*: during playback, the playhead moves across the timeline. In figure 2, the Frame Range (e.g. 1 - 1580) lies completely within the timeline window. However, most of the time, this is not the case. But what if the frame range is larger than the timeline window? What will happen if the Playhead reaches the border of the timeline window? If Follow Current Frame is disabled, the playhead runs off the screen. If enabled, the timeline window will be panned and show the next range of frames of the same width.
   - *Limit to Frame Range*: マウスを使用して再生範囲外のフレームを選択することを許可しません。
   - *Follow Current Frame*: 再生中に、Playheadがタイムライン上を移動します。図2 では、フレーム範囲 (例: 1 ～ 1580) がTimelineウィンドウ内に完全に収まっています。ただし、ほとんどの場合、そうではありません。しかし、フレーム範囲がTimelineウィンドウよりも大きい場合はどうなるでしょうか? PlayheadがTimelineウィンドウの境界に達するとどうなりますか?  [Follow Current Frame] が無効になっている場合、Playheadは画面からはみ出します。有効にすると、Timelineウィンドウがパンされ、同じ幅の次のフレーム範囲が表示されます。


Play In
   .. When you pressed the Play button, you see the movie playing in the preview window. If all options are disabled, then the preview window will not be updated. So, at least the checkbox *Animation Editors* (updates the Timeline, Dope Sheet, Graph Editor, Video Sequencer) or *Video Sequencer* must be enabled to preview the movie.
   再生ボタンを押すと、Previewウィンドウでムービーが再生されます。すべてのオプションが無効になっている場合、Previewウィンドウは更新されません。したがって、動画をプレビューするには、少なくとも *Animation Editors* (Timeline、Dope Sheet、Graph Editor、Video Sequencerを更新) または *Video Sequencer* のチェックボックスを有効にする必要があります。

.. _using_markers:

.. Using markers
マーカーの使用
.............
.. With a long timeline, it could be useful to insert some markers.
.. Markers are used to name specific frames with a meaningful name. They are shown as small white triangles at the bottom of the Sequencer timeline.
.. In figure 2, the second marker (Appearance dog) is selected. You can see by the white fill-color of the triangle, the slightly elevated text and the white dotted vertical line. The other markers are not selected (only a grey outline and a black dotted line). The first marker (F_01) is the result of the menu Marker > Add Marker (:kbd:`M`). This marker is added at the location of the playhead and has a standard name F_XXX, where XXX is the framenumber. The text is slightly elevated as indication that the playhead is at the marker location. In order to get more meaningful names, you have to rename (Marker > Rename Marker of :kbd:`Ctrl M` shortcut).

タイムラインが長い場合は、マーカーを挿入すると便利な場合があります。
マーカーは、特定のフレームに意味のある名前を付けるために使用されます。これらはシーケンサーのタイムラインの下部に小さな白い三角形として表示されます。
図2 では、2番目のマーカー(Appearance dog) が選択されています。
白塗りの三角形、わずかに浮き上がったテキストと、白い点線の垂直線によって確認できます。
他のマーカーは選択されていません (灰色の輪郭と黒い点線のみ)。最初のマーカー (F_01) は、メニューの [Marker]メニュー > [Add Marker] (:kbd:`M`) の実行結果です。このマーカーはPlayheadの位置に追加され、標準名は F_XXX です。XXX はフレーム番号です。テキストはわずかにわずかに浮き上がっており、Playheadがマーカーの位置にあることを示しています。より意味のある名前をつけるには、名前を変更する必要があります。
([Marker] > [Rename Marker] か ショートカットキー :kbd:`F2` か マーカーを :kbd:`LMB-DoubleClick` [#f3]_)

.. figure:: /images/editors_vse_sequencer_markers.svg
   :alt: Markers

   Figure 2: Markers in the Sequencer timeline

.. More detailed information is in `Animation & Rigging > Markers <https://docs.blender.org/manual/en/latest/animation/markers.html>`_.  To summarize the most important commands for the Video Sequencer:

詳細については、`Animation & Rigging > Markers <https://docs.blender.org/manual/en/latest/animation/markers.html>`_ を参照してください。
Video Sequencerの最も重要なコマンドを要約すると、次のようになります。

.. - The display of markers in the timeline can be toggled on or off with the menu View > Show Markers.
.. - Add a marker: select the frame and press :kbd:`M`. You can also add markers during playback *while viewing the movie*. Just press :kbd:`M` when the playhead is at the desired frame. The markers have a name like F_514 (frame 514).
.. -  Select a marker: :kbd:`LMM - Click` on marker triangle. To select all markers, press :kbd:`A` when over the marker timeline. To select multiple markers, press :kbd:`LMB` and drag over the markers.
.. - Rename a marker: select marker and press :kbd:`Ctrl+M`.
.. - Move marker: select marker and press :kbd:`G`. Move the markers and :kbd:`LMB-Click` to confirm or :kbd:`RMB-Click` to cancel.
.. - Delete marker: select marker and press :kbd:`X`.
- タイムライン内のマーカーの表示は、[View]メニュー > [Show Markers] でオンとオフを切り替えることができます。
- マーカーの追加: フレームを選択して :kbd:`M` を押します。*動画を見ながら*、再生中にマーカーを追加することもできます。Playheadが目的のフレームにあるときに :kbd:`M` 押すだけです。マーカーには F_514 (フレーム514のマーカーの場合) のような名前が付きます。
- マーカーの選択: マーカーの三角形を :kbd:`LMM-Click` して選択。すべてのマーカーを選択するには、マーカーのタイムライン上で :kbd:`A` を押します。複数のマーカーを選択するには、:kbd:`LMB` を押して、複数のマーカーをドラッグして選択します。
- マーカー名の変更：マーカーを選択して :kbd:`F2` を押します。(:kbd:`LMB-DoubleClick` でも同様)
- マーカーの移動: マーカーを選択して :kbd:`G` を押します。カーソルを動かし、マーカーを移動して :kbd:`LMB-Click` で確定、 :kbd:`RMB-Click` でキャンセルします。
- マーカーの削除: マーカーを選択して :kbd:`X` を押します。.

.. rubric:: 脚注

.. [#f1] Blender4.0では、[Properties Editor] > [Output]タブ > [Frame Range]パネル のこと??
.. [#f2] Blender4.0はインストール時に :kbd:`Spacebar` の設定は不要なようです。デフォルトで :kbd:`Spacebar` アクションは再生になっているようです。
.. [#f3] Blender4.0では、マーカー名の変更は :kbd:`Ctrl M` ではなく、:kbd:`F2` か ::kbd:`LMB-DoubleClick` のようです。
