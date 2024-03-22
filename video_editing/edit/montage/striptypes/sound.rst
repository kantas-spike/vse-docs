.. _bpy.types.SoundSequence:

***********
サウンドストリップ
***********

.. The input source of a Sound strip is an audio file with extension
.. ``.AAC``, ``.AC3``, ``.FLAC``, ``.MP2``, ``.MP3``,  ``.opus``, ``.PCM``,  or ``.vorbis``
サウンド ストリップの入力ソースは、拡張子が以下のオーディオファイルです。(参照 `audio formats <https://docs.blender.org/manual/en/dev/files/media/video_formats.html>`_)

``.AAC``, ``.AC3``, ``.FLAC``, ``.MP2``, ``.MP3``,  ``.opus``, ``.PCM``, ``.vorbis``

.. (see `audio formats <https://docs.blender.org/manual/en/dev/files/media/video_formats.html>`_).

..
  You can add a Sound strip directly from one of the above-mentioned filetypes.
  It is also indirectly created when you add a Movie strip from a video file with an embedded audio channel.
  Blender will automatically extract the sound strip and put it in the channel beneath the video strip (if there is room).
  There is no linking between the source video file and the embedded audio.
  So, you can move the sound strip without moving the movie strip and vice versa;
  thereby creating a synchronization problem.
  The :ref:`default <default-color>` color of the Sound strip bar is: :sound:`███`
..

サウンド ストリップは、上記のファイルタイプのいずれかから直接追加できます。
また、オーディオチャネルが埋め込まれたビデオファイルからムービー ストリップを追加するときにも間接的に作成されます。
Blender は自動的にサウンド ストリップを抽出し、ビデオ ストリップの下のチャンネルに配置します (スペースがある場合)。
ソースビデオファイルと埋め込みオーディオの間にリンクはありません。
したがって、ムービー ストリップを移動せずにサウンド ストリップを移動することも、その逆も可能です。
そのため、同期の問題が発生します。サウンドストリップバーのデフォルトの色は :sound:`███` です。

.. warning::

   .. Sometimes, after adding a Movie strip, you will notice that the Movie and Sound strip have not the same length.
   .. This is the result of a mismatch between the Frame rate (fps) of the project and the video clip.
   ムービー ストリップを追加した後、ムービー ストリップとサウンド ストリップの長さが同じではないことに気づく場合があります。
   これは、プロジェクトとビデオ クリップのフレーム レート (fps) の不一致の結果です。

.. figure:: /images/vse_setup_project_striptypes_sound.svg
   :alt: Synchronization problem
   :align: Right

   図 1: fps の不一致による同期の問題

..
  Suppose, you are adding a 30 fps video with a duration of 1 second or 30 frames to a 24 fps project.
  The embedded audio in the video file is of course synchronized with the frame sequence of the video.
  Frame 1 of the video file is synced with a specific time code in the audio, and so is frame 2, frame 3, ect...
  In figure 1, there is a beep at timecode 0.27 s (frame 8) and at 0.73 s (frame 22).
  But, the project runs at 24 fps.
  The beeps still occur at 0.27 and 0.73 s but frame 8 and 22 are shifted to the right.
  Frame 24 in the project is after all at time code 1 s, so,
  frame 22 is lightly before that at timecode 0.91 s.
  The Sound strip therefore will end at frame 24 because sound cannot be compressed without changing the Pitch.
..
1 秒または 30 フレームの長さの 30 fps ビデオを 24 fps プロジェクトに追加するとします。
動画ファイルに埋め込まれた音声は、当然ながら動画のフレームシーケンスと同期しています。
ビデオ ファイルのフレーム 1 はオーディオの特定のタイム コードと同期され、フレーム 2、フレーム 3 なども同期されます。
図 1 では、タイムコード 0.27 秒 (フレーム 8) と 0.73 秒 (フレーム 22) でビープ音が鳴ります。
ただし、プロジェクトは 24 fps で実行されます。ビープ音は引き続き 0.27 秒と 0.73 秒で発生しますが、フレーム 8 と 22 は右にシフトされます。
プロジェクトのフレーム 24 は結局タイムコード 1 秒なので、フレーム 22 はその少し前のタイムコード 0.91 秒です。
したがって、ピッチを変更せずにサウンドを圧縮することはできないため、サウンド ストリップはフレーム 24 で終了します。


Options
=======

.. note:: Panels documented elsewhere!

   .. The following panels are identical to those of the Movie strip:
   .. :ref:`Time <time-panel>`, :ref:`Source <source-panel>` and :ref:`Custom <custom-panel>`.
   パネルは他の場所で文書化されています。

   以下ののパネルは、ムービー ストリップのパネルと同じです。

   - :ref:`Time <time-panel>`
   - :ref:`Source <source-panel>`
   - :ref:`Custom <custom-panel>`

.. There are **no** *Compositing*, *Transform*, *Crop*, *Video*, and *Color* panels for the Sound strip.
.. The following properties are **specific** for sound strips.

サウンド ストリップには、 以下のパネルはありません。

- *Compositing*
- *Transform*
- *Crop*
- *Video*
- *Color*

以降のプロパティはサウンド ストリップで *固有* のものです。

Sound
-----

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Sound
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-sound.svg
   :scale: 80%
   :alt: Sound Panel
   :align: Right

   Figure 2: Sound Panel

Volume
  ..
   The volume or loudness of the sound. Setting the Volume to zero will mute the sound
   A value of 0 - 1 will reduce the volume, while a value = 1 results in the original sound level.
   Above 1 will increase the sound level. However, does a sound with value = 2 sound double
   as loud or with value = 0.5 half as loud as the original? Not at all!

   For more detailed information about the interpretation of the sound level in terms of decibels;
   see :doc:`Volume level </video_editing/edit/sound/measuring/volume>`.
  ..
  音の音量または音量。音量をゼロに設定するとサウンドがミュートされます。値を 0 ～ 1 の間にすると音量が下がり、
  値 = 1 にすると元のサウンド レベルになります。
  1 を超えると音声レベルが増加します。
  しかし、値 = 2 のサウンドは元の 2 倍の大きさに聞こえますか、それとも値 = 0.5 のサウンドは元の半分の大きさでしょうか? そうではありません！

  デシベル単位での騒音レベルの解釈についての詳細は、 :doc:`Volume level </video_editing/edit/sound/measuring/volume>` を参照してください。

Pitch
  ..
   Pitch (lower versus higher tones) is closely related to the frequency of a sound.
   The Pitch value of the Sound strip will change the playback speed or frequency of the sound.
   Increasing the value will make the sound appear higher in tone, decreasing will lower the tone.
   Because the playback rate is also changed, the length of the sound is changed.

   This is however not visually represented in the timeline.
   Neither the length nor the shape of the waveform is changed.
   The Sound strip appears equally long as before but the sound
   will stop earlier or premature in case of a reduction of the speed.
  ..

  ピッチ (低音と高音) は音の周波数と密接に関係しています。サウンド ストリップのピッチ値は、サウンドの再生速度または周波数を変更します。
  値を大きくすると音が高くなり、小さくすると音が低くなります。再生レートも変わるので音の長さも変わります。

  ただし、これはタイムラインでは視覚的に表現されません。波形の長さも形も変わりません。
  サウンド ストリップは以前と同じ長さで表示されますが、速度が低下するとサウンドはより早くまたは途中で停止します。


.. figure:: /images/vse_setup_project_striptypes_sound-waveform.svg
   :alt: Sound waveform

   図3 Blender でピッチを変更しても音の波形は変化しない

..
  Figure 3 shows the waveform of a countdown audio file. Whatever pitch you select,
  this waveform and length will not change in Blender.
  The middle waveform is from the same file in Audacity with a speed value (= pitch value in Blender) of 1.
  As you can see the length of this wave is the same; ~ 13 s. When the speed is changed to 1.4,
  the length of the wave is reduced to 9.5 s (~13s /1.4) in Audacity but visually not in Blender.
  However, playing the audio will reveal that the tone height (and speed)
  is about the same and that the sound will stop at ~9.5 s.
  Please, note also that the file is stereo in Audacity but mono in Blender.
..
図 3 は、カウントダウン音声ファイルの波形を示しています。どのようなピッチを選択しても、この波形と長さは Blender で変更されません。
中央の波形は、Audacity の同じファイルからのもので、スピード値 (= Blender ではピッチ値) が 1 です。
ご覧のとおり、この波形の長さは同じ 13秒 です。
速度を 1.4 に変更すると、Audacity では波の長さが 9.5 秒 (~13 秒 /1.4) に短縮されますが、
Blender では視覚的には短縮されません。ただし、オーディオを再生すると、音の高さ (および速度) がほぼ同じで、
サウンドが約 9.5 秒で停止することがわかります。
ファイルは Audacity ではステレオですが、Blender ではモノラルであることにも注意してください。

..
  So, changing the pitch or duration of a sound file can -and is usually- also done
  with the :doc:`speed control </video_editing/edit/effects/speed>` in Blender.
  :doc:`Strip types </video_editing/edit/montage/striptypes/index>`
..
したがって、サウンド ファイルのピッチや長さの変更は、 Blender の :doc:`speed control </video_editing/edit/effects/speed>` を使用しても行うことができます。

Pan
  ..
   Depending on your sound system, you have one, two, or more speakers.
   Panning is the distribution of the sound over those speakers.
   It is mainly used to pan (distribute) the audio from left and right channels.
   Pan values can be between -2 and 2 (see figure 4). A value of zero means front/center (12 o'clock).
   An equal amount of sound is sent to the left and right speakers.
   A value of -1 means that all sound is sent to the left channel (10 o'clock).
   And a value of +1 means that the sound will appear at 2 o'clock).
   In the case of multichannel audio (rear speakers),
   you can pan to those with the higher values: -2 (7 o'clock) and +2 (5 o'clock).
   So this value basically represents the angle at which the sound is played. Only works for mono sources.
  ..
  サウンド システムに応じて、1 つ、2 つ、またはそれ以上のスピーカーがあります。
  パンとは、スピーカー全体にサウンドを分配することです。
  これは主に、左右のチャンネルからのオーディオをパン（分配）するために使用されます。
  パン値は -2 ～ 2 の間で指定できます (図 4 を参照)。値 0 は、前面/中央 (12 時) を意味します。
  左右のスピーカーに同じ量の音が送られます。値 -1 は、すべてのサウンドが左チャンネル (10 時) に送信されることを意味します。
  +1 の値は、サウンドが 2 時位置に表示されることを意味します)。
  マルチチャンネル オーディオ (リア スピーカー) の場合は、より高い値、-2 (7 時) および +2 (5 時) にパンできます。
  したがって、この値は基本的にサウンドが再生される角度を表します。モノラルソースでのみ機能します。

   .. figure:: /images/vse_setup_project_striptypes_sound-pan.svg
      :scale: 50%
      :alt: Pan values

      図4 Panの値

Display Waveform
  ..
   Display an approximate waveform of the sound file inside of the sound strip.
   The waveform reflects strip volume. This volume can be animated using keyframes.
   If the waveform is not displayed, you'll have to turn on the Show Overlays (button at the top right; see figure 1).
  ..
  サウンド ストリップ内にサウンド ファイルのおおよその波形を表示します。
  波形はストリップのボリュームを反映します。このボリュームはキーフレームを使用してアニメーション化できます。
  波形が表示されない場合は、[Show Overlays] (右上のボタン、図 1 を参照) をオンにする必要があります。

Mono
   .. Mixdown all audio channels into a single one.
   すべてのオーディオチャンネルを単一のチャンネルにミックスダウンします。


Source
------

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Source
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

Pack
  ..
   Packing the sound file means that the sound is embedded -not linked- in the blend-file.
   This can ease the job of transferring a project to another computer because you have to distribute only one file.
   But, remember, we advocate the use of a single, all-containing project folder
   (see :doc:`/video_editing/setup/directory-structure`).
   Packing the file will only increase the size of the Blend-file
   and is in any case already included in the distribution of the project folder.
  ..

  サウンド ファイルをパックするということは、サウンドがブレンド ファイルに (リンクではなく) 埋め込まれることを意味します。
  これにより、配布する必要があるファイルが 1 つだけになるため、プロジェクトを別のコンピュータに転送する作業が容易になります。
  ただし、すべてを含む単一のプロジェクト フォルダーの使用を推奨していることに注意してください ( :doc:`/video_editing/setup/directory-structure` を参照)。
  ファイルを圧縮しても Blend ファイルのサイズが増加するだけであり、いずれの場合もプロジェクト フォルダーの配布にすでに含まれています。

Caching
   .. The sound file is decoded and loaded into RAM for fluent playing.
   サウンド ファイルはデコードされて RAM にロードされ、スムーズな再生が可能になります。
