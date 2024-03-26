.. Timeline
タイムライン
--------

.. _timeline:

.. The concept *Timeline* can refer to different things. In Blender, it denotes in the first place the `Timeline Editor <https://docs.blender.org/manual/en/dev/editors/timeline.html>`_ , identified by a clock icon and used for manipulating keyframes and scrubbing the playhead (see figure 1). This Timeline Editor was originally intended for editing the animations in 3D modeling. For video editing, this editor is less useful.

*タイムライン* という概念は、様々ものを指すことができます。Blenderでは、まず、`Timeline Editor <https://docs.blender.org/manual/en/dev/editors/timeline.html>`_ のことを指します。Timeline Editorは 時計のアイコンで識別され、キーフレームの操作とPlayheadを動かす時に使用されます(図1)。

このTimeline Editorは、本来3Dモデリングでアニメーションを編集することを目的としていました。動画編集の場合、あまり役に立ちません。[#f1]_

.. figure:: /images/editors_vse_timeline-editor.svg
   :alt: Timeline editor

   図1: BlenderのTimeline Editor

.. You can find the Timeline Editor also in the :doc:`Video Sequence Editor workspace </video_editing/setup/workspace>`, all the way at the bottom of the screen. Only the header is visible; so you have to drag the horizontal top border to reveal the time units and eventual keyframes.

Timeline Editor は :doc:`Video Sequence Editor workspace </video_editing/setup/workspace>` の画面下部にあります。
ヘッダーのみが表示されます。Timeline Editorの時刻とキーフレームを表示するには、上部の水平境界線をドラッグする必要があります。

.. The use of *this* Timeline Editor within the Video Editor workspace is rather *limited* and a case could be made to remove it from the Video Editing workspace. Its functions can easily be overtaken by the Sequencer (see figure 2), which is right on top of it in the Video Editing Workspace.

Video Editor workspace内でのこのTimeline Editorの使用はかなり限定されており、場合によっては、Video Editor workspaceから削除することもありえます。その機能は、Video Editor workspaceのすぐ上にあるSequencer(図2) に簡単に置き換えられます。

.. The Sequencer has indeed also a kind of timeline on its own. Practically all the regular operations like zoom, move, ... can be done here. Only the Frame and Transport controls are missing. These can however easily be added to the workspace (see the addon by TintwoTin; `Playback_control_in_VSE_header.zip <https://github.com/tin2tin/Sequence_Editing>`_ ).

確かに、Sequencerは自身で一種のタイムラインを持っています。ズーム、移動などの通常の操作はほぼすべてここで実行できます。Frame および Transport コントロールのみが欠落しています。ただし、これらはワークスペースに簡単に追加できます (TintwoTin によるアドオンを参照 `Playback_control_in_VSE_header.zip <https://github.com/tin2tin/Sequence_Editing>`_) [#f2]_ 。


.. figure:: /images/editors_vse_sequencer_timeline_sequencer.svg
   :alt: Sequencer timeline

   図2: BlenderのSequencerのタイムライン

.. The timeline of the sequencer is divided horizontally in channels and vertically in time units. The default *Visible Range* is from channel 0 to channel 7 and from time 0 to time 10s.

Sequencerのタイムラインは、水平方向にチャネル、垂直方向に時間に分割されます。デフォルトの表示範囲は、1〜7チャネル、0〜10 秒です。[#f3]_

.. The header of the timeline is formed by a kind of ruler with time units. As you can see from figure 2, the time units are displayed in so-called SMPTE timecodes. A SMPTE timecode is a standard format, adopted by the Society of Motion Picture and Television Engineers (SMPTE) in the late 1960s. It is written as HH:MM:SS:FF, e.g. 00:01:12:06. This means the time after 1 minute, 12 seconds, and 6 frames. If your project has a framerate of 24 fps, the 6 frames will add another 0.25 seconds to the timecode.

タイムラインのヘッダーは、時間単位を持つ一種の定規から構成されます。図2 からわかるように、時間はいわゆる SMPTE タイムコードで表示されます。SMPTE タイムコードは、1960 年代後半に映画テレビ技術者協会 (SMPTE) によって採用された標準形式です。これは、HH:MM:SS:FF (例: 00:01:12:06) と書かれます。1分12秒6フレーム後の時間を指します。プロジェクトのフレームレートが 24 fps の場合、6 フレームによりタイムコードにさらに 0.25 秒が追加されます。

.. You can change the timecode style. It's rather well hidden in User Preferences > Animation > Timeline (see figure 3). By default, the time units are shown with Minimal Info; see table 1 for the other options.

タイムコードのスタイルを変更できます。これは、[Preferences] > [Animation] > [Timeline] にうまく隠されています (図3 を参照)。デフォルトでは、時間単位は最小限の情報で表示されます。他のオプションについては表1 を参照してください。

.. figure:: /images/editors_vse_sequencer_timeline_timecode-style.png
   :alt: Timecode style

   図3: User Preferencesのタイムコードスタイル

.. csv-table:: 表1: タイムコードスタイル
   :header: "Type", "Style", "Comment"
   :widths: 35, 10,350

   Minimal info, 1+18, 1 second and 18 frames
   SMPTE (Full), 00:00:01:18,
   SMPTE (Compact), 00:01:18,
   Compact with Milliseconds, 00:01:6, with fps = 30
   Only Seconds, 1.6,

.. In Blender, you can choose to show the timeline in *seconds* or in *frames*. Use the command :kbd:`Ctrl + T` or the menu View > Show seconds. In figure 4, the timeline is shown in frames. As a video editor, you probably are most interested in time. It seems more natural to refer to a video fragment with a time indication, e.g. 00:01:15:10 or 1' 15'' and 10 frames than with a frame number, e.g. frame 55. You cannot enter the SMPTE timecode directly in the side panel, you have to enter the frame number.

Blender では、タイムラインを *秒単位* で表示するか *フレーム単位* で表示するかを選択できます。:kbd:`Ctrl + T` コマンドまたはメニューの [View] > [Show seconds] を使用します。
図4 では、タイムラインがフレーム単位で示されています。動画編集者であれば、おそらく時間に最も関心があるでしょう。
動画の一部分を、フレーム番号(例: フレーム 55)ではなく、時間表示(例: 00:01:15:10や1' 15'' and 10 frames')で参照するほうが自然でしょう。
ただし、SMPTE タイムコードを直接入力することはできません。サイドパネルでは、フレーム番号を入力する必要があります。

.. Because each project has a frame-per-seconds `fps` parameter, you can always derive one code from the other. In a 30 fps project:

各プロジェクトには `fps`(フレーム/秒) パラメーターがあるため、いつでも一方のコードをもう一方のコードから派生させることができます。

30 fps プロジェクトの場合:

.. * frame 155 is at time 115/30 = 3.8333 seconds or in SMPTE (Compact) notation: 00:03+25.
* フレーム 155 の時間は 155/30 = 3.8333 秒 もしくは SMPTE (Compact) 表記で00:03+25 になります。
.. * time 2.5s falls somewhere within frame  2.5 * 30 = 75.
* 時間 2.5s は 2.5 * 30 = 70フレーム 内のどこかに収まります。

.. The conversion from frame to SMPTE code is done by a Python function *smpte_from_frame*. This function takes one parameter (the frame number) and converts it to a timecode.

フレームから SMPTE コードへの変換は、Python 関数smpte_from_frameによって行われます。この関数は 1 つのパラメータ (フレーム番号) を受け取り、それをタイムコードに変換します。

.. Strips are placed in channels; rows stacked upon each other (see for example figure 2 with 2 channels). There are 128 channels available; although you can zoom out much further. The first channel 0 is unusable as a place to put strips. This is because it is used by the Sequencer Display to show a composite of all strips above channel 0.

ストリップはチャンネルに配置されます。行が互いに積み重ねられています (図2の場合 2つのチャンネルを使用)。128 チャンネルが利用可能です。さらにズームアウトすることもできます。最初のチャンネル 0 はストリップを配置する場所としては使用できません。これは、チャンネル 0 より上のすべてのストリップの合成を表示するためにシーケンサー ディスプレイによって使用されるためです。[#f4]_

.. Theoretically, the Timeline can span the frames from - |infinity| to + |infinity| and from channel 0 to channel 32. In practice, only a limited amount of frames and channels can be seen in the Sequencer. This range is called the *Visible Range*. There are three basic operations you can perform in the Timeline (see figure 1).

理論的には、タイムラインは - ∞ から + ∞ まで、およびチャネル 0 からチャネル 32 までのフレームにまたがることができます [#f5]_ 。実際には、Sequencer で表示できるフレームとチャネルの量は限られています。この範囲は *表示範囲* と呼ばれます。タイムラインで実行できる基本的な操作は 3 つあります (図4)。


- 移動: 表示範囲は同じ量をカバーしますが、異なるフレームとチャネルをカバーします。
- ズーム: 表示範囲内のフレームとチャンネルをより多く (ズームアウト)、またはより少なく (ズームイン) 詰め込みます。
- ナビゲート: Playheadを移動して、Preview に別のフレームが表示されるようにします。

.. Please note that in a Move operation, the Visible Range can be moved horizontally, vertically or both. The area will not change. As a result of the Move, the playhead could fall out of view. The Zoom operation always start from the current Visible Range and will shrink or expand its area. Again, as a result the playhead could fall fall outside the Visible Range. In a Navigate operation, the Visible Range will never change, only the playhead will move.

移動操作では、表示範囲を水平、垂直、またはその両方に移動できることに注意してください。エリアは変わりません。移動の結果、再生ヘッドが表示されなくなる可能性があります。ズーム操作は常に現在の可視範囲から開始され、その領域が縮小または拡大されます。繰り返しになりますが、その結果、再生ヘッドが可視範囲外に落ちてしまう可能性があります。ナビゲート操作では、表示範囲は変更されず、再生ヘッドのみが移動します。

.. figure:: /images/editors_vse_sequencer_timeline_move-size.svg
   :alt: Sequencer window

   図4: Sequencerでの移動, ズーム および ナビゲーション操作

.. |infinity| unicode:: 0x221E

.. toctree::

   move
   zoom
   navigate


.. rubric:: 脚注

.. [#f1] (訳注) 動画編集でキーフレームアニメーションを利用する場合は、3Dモデリングで利用する場合と同様に便利です。

.. [#f2] (訳注) このアドオンも4年前から更新されていないため利用しないほうが良さそうです。

.. [#f3] (訳注) Blender4.0にはchannel0は存在しません。デフォルトでは0〜7チャンネルが表示されます。

.. [#f4] (訳注) Blender4.0から?? channel0はマニュアルに記載がなくなっています。

.. [#f5] (訳注) Blender4.0ではチャンネルは1〜128までのようです。
