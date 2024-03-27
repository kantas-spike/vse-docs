Project settings
================

.. figure:: /images/video_editing_setup_project-settings-output-categories.png
   :alt: Output panels
   :align: right
   :scale: 40%

   図0: Output パネル

.. The Project Settings for your video project are grouped in the `Output Properties <https://docs.blender.org/manual/en/dev/render/output/index.html>`_ tab of the `Properties Editor <https://docs.blender.org/manual/en/latest/editors/properties_editor.html>`_. This editor is located at the top right area in the default Video Editing workspace and is shared with the other modules, e.g. 3D modeling. The Properties has several categories, which can be chosen via tabs (the icons column to its left). Each tab regroups properties and settings of a data type. For the VSE, only the Output properties are commonly used. This tab is selected by default on opening the Video Editor Workspace. It contains 6 categories (panels): Format, Frame Range, Stereoscopy, Output, Metadata, & Post Processing.

ビデオ プロジェクトのプロジェクト設定は、 `Properties Editor <https://docs.blender.org/manual/en/latest/editors/properties_editor.html>`_ の[`Output <https://docs.blender.org/manual/en/latest/render/output/index.html>`_]タブにグループ化されています。

この エディター はデフォルトの Video Editing Workspace の右上領域にあり、3D モデリングなどの他のモジュールと共有されます。プロパティにはいくつかのカテゴリがあり、タブ (左側のアイコン列) から選択できます。各タブには、データ型のプロパティと設定が再グループ化されています。

VSE [#f2]_ の場合、一般的に使用されるのは [Output]タブ のみです。このタブは、Video Editing Workspace を開くとデフォルトで選択されます。これには、6 つのカテゴリ (パネル) が含まれています。

- Format
- Frame Range
- Stereoscopy
- Output
- Metadata
- Post Processing

.. admonition:: Reference
   :class: refbox

   =============   ==============================================================
   **Name**:       *Dimensions*
   **Context**:    Video Sequence Editor > Properties
   **Location**:   Tabs > Output Properties > **Format**
   =============   ==============================================================

.. figure:: /images/video_editing_setup_project-settings.png
   :alt: Project Settings
   :align: right
   :scale: 40%

   図1: Dimensions パネル

Resolution
   .. The resolution X and Y refer to the number of pixels in the horizontal and vertical axis of the output video. Common video resolutions are:

   解像度 X と Y は、出力ビデオの水平軸と垂直軸のピクセル数を指します。一般的なビデオ解像度は次のとおりです。

   - High Definition (HD) or 720p (1280 x 720)
   - Full HD or 1080p (1920 x 1080)
   - Ultra HD (UHD) 4K or 2160p (3840 x 2160).

   .. Figure 2 shows these three common resolutions more visually. Note how small the HD resolution is, compared to the UHD or 4K version. Of course, there are many more formats for social media, film theater, .... A rather exhaustive list can be found at `Wikipedia <https://en.wikipedia.org/wiki/List_of_common_resolutions>`_.

   図 2 は、これら 3 つの一般的な解像度をより視覚的に示しています。 UHD または 4K バージョンと比較して、HD 解像度がいかに小さいかに注目してください。もちろん、ソーシャル メディア、映画館など、他にも多くの形式があります。かなり網羅的なリストは `Wikipedia <https://en.wikipedia.org/wiki/List_of_common_resolutions>`_ にあります。

   .. figure:: /images/vse_setup_project_resolutions.svg
      :alt: Resolutions
      :align: right
      :scale: 100%

      図2: Ultra HD, FHD and HD resolution

   .. With the Render Presets button (see figure 1), you can choose between common video render settings (HDTV 1080p, HDTV720p, ...). The resolution, resolution %, the aspect ratio and the fps will be set accordingly.  You can also create your own preset: change the settings in the Dimensions panel to your liking, enter a name in the New Preset field and press the + button. The Presets are stored in the scripts/presets/render directory as a Python file.

   [Render Presets] ボタン (図 1) を使用すると、一般的なビデオ レンダリング設定 (HDTV 1080p、HDTV720p など) から選択できます。解像度、解像度 %、アスペクト比、fps は、選択したプリセットに応じて設定されます。
   独自のプリセットを作成することもできます。[Dimensions] パネルの設定を好みに合わせて変更し、[New Prests] フィールドに名前を入力して、[+] ボタンを押します。プリセットは、Python ファイルとして scripts/presets/render ディレクトリに保存されます。

Resolution %
   .. You can set the Resolution % (default = 100%) to a lower percentage to render the video temporarily in a lower resolution. For example, if set to 10%, a full HD movie will then render at the resolution of 192 x 108 pixels. You can check this by :kbd:`RMB` + Click & hold at the top right corner of the preview of the Video Sequencer. In the status bar, you will notice something like: ``X : 190  Y: 100 ...``, meaning that the location you clicked is at resolution X = 190 and resolution Y = 100. So the full render image is effectively 192 x 108 pixels. Of course, the picture will look terrible; you only have 192 x 108 = 20736 pixels at your disposal to draw the picture.

   [Resolution %] (デフォルト = 100%) を低いパーセンテージに設定して、ビデオを一時的に低い解像度でレンダリングすることができます。たとえば、10% に設定すると、フル HD ムービーは 192 x 108 ピクセルの解像度でレンダリングされます。
   :kbd:`LMB-Click` して, Video Sequence Editor の Preview の右上隅を 押し続けることで 確認できます [#f1]_ 。
   Statusbarに、``X : 190  Y: 100 ...`` のような表示が表示されます。
   これは、クリックした場所が、解像度 X = 190 および解像度 Y = 100 であることを意味します。したがって、完全なレンダリング イメージは実質的に 192 x 108 ピクセルになります。もちろん、写真はひどいものになります。絵を描くために自由に使えるのは 192 x 108 = 20736 ピクセルだけです。

   .. Figures 3 - 4 show the render result with the percentage set to 10% and 5% of the 4K image of figure 2. Please note, that a 10% render of the UHD image still gives us an image of 386 x 216 pixels. The images are scaled up to have a clear view and the same dimensions of figure 2. Figure 4 is in reality only 192 pixels wide x 108 pixels tall.

   図 3 ～ 4 は、図 2 の 4K 画像の割合を 10% と 5% に設定したレンダリング結果を示しています。UHD 画像を 10% レンダリングしても、依然として 386 x 216 ピクセルの画像が得られることに注意してください。画像は、鮮明に見えるように拡大され、図 2 と同じ寸法になっています。図 4 は、実際には、幅 192 ピクセル x 高さ 108 ピクセルのみです。

   .. figure:: /images/vse_setup_project_tree-10.png
      :alt: Resolutions
      :scale: 200%

      図3: 10% でレンダリングされた図 2

   .. figure:: /images/vse_setup_project_tree-05.png
      :alt: Resolutions
      :scale: 400%

      図4: 5% でレンダリングされた図 2

   .. Lowering the resolution % is not meant to speed up the preview or the scrubbing of the timeline. For that, you need :doc:`proxies <proxies>`. Because proxies are enabled by default (see Edit > Preferences > System Video Sequencer > Proxy Setup), you will not notice much improvement in navigating the timeline with a small resolution %.  Only the render time is affected. You can use this option if you want to create a quick test render, for example to check the audio synchronization of your video.

   [Resolution %] を下げることは、プレビューやタイムラインのスクラブを高速化することを意味するものではありません。
   そのためには、 :doc:`プロキシ <proxies>` が必要です。プロキシはデフォルトで有効になっているため ([Edit] > [Preferences] > [System] > [Video Sequencer] > [Proxy Setup] を参照)、[Resolution %] が小さい場合、タイムラインのナビゲーションに大きな改善は見られません。レンダリング時間のみが影響を受けます。このオプションは、ビデオの音声同期を確認するなど、簡単なテスト レンダリングを作成する場合に使用できます。

Aspect X/Y
   .. We tend to view the pixels of our computer display as little squares and for most modern computers, they are in fact squares. In the world of cinema and television, especially with older equipment, non-square pixels are commonplace. All movies on DVD and BluRay for example use rectangular pixels. Shooting with anamorphic lenses also gives a distorted raw image on a computer screen, due to the use of non-square pixels.

   私たちはコンピューター ディスプレイのピクセルを小さな正方形として見る傾向がありますが、ほとんどの最新のコンピューターでは、実際には正方形です。映画やテレビの世界では、特に古い機器では、非正方形ピクセルが一般的です。たとえば、DVD や BluRay のすべてのムービーは長方形のピクセルを使用します。アナモフィック レンズで撮影すると、非正方形ピクセルが使用されるため、コンピューター画面上で生の画像が歪んで表示されます。

   .. Figure 5 shows an example of a raw image, taken with an *anamorphic lens* with a horizontal compression of 1.33. Anamorphic lenses are typically used in cinema to achieve an ultra wide screen view. To achieve this, the image is horizontally squeezed. Although perhaps not immediately that obvious, figure 5 looks a little bit distorted.
   図 5 は、水平圧縮 1.33 のアナモルフィック レンズで撮影した生の画像の例を示しています。アナモフィック レンズは通常、超ワイド スクリーン ビューを実現するために映画で使用されます。これを実現するために、画像は水平方向に圧縮されます。すぐには明らかではないかもしれませんが、図 5 は少し歪んで見えます。

   .. figure:: /images/vse_setup_project_anamorphic-squeezed.jpg
      :alt: Image from an anamorphic lens (squeezed)
      :scale: 100%

      図5: アナモフィック レンズからの Raw イメージ

   .. With ffmpeg, you can retrieve the aspect ratio of this image. The result is:
   ffmpeg を使用すると、この画像のアスペクト比を取得できます。結果は次のとおりです。

   ``590x332 [SAR 96:96 DAR 295:166]``

   .. According to ffmpeg, the image is 590 x 332 pixels (so does Blender)
   ffmpeg によると、画像は 590 x 332 ピクセルです (Blender も同様です)

   .. figure:: /images/vse_setup_project_anamorphic-desqueezed.jpg
      :alt: Image from an anamorphic lens (desqueezed)
      :scale: 100%

      図6: アナモルフィック レンズからの後処理画像


   .. This can give all sort of problems when you want to play an old DVD movie on your computer. Sometimes, the characters are squeezed or stretched. Why? And what can you do about it?
   これにより、古い DVD ムービーをコンピュータで再生するときに、あらゆる種類の問題が発生する可能性があります。場合によっては、文字が圧縮されたり、引き伸ばされたりすることがあります。なぜ？それに対して何ができるでしょうか?

   .. todo::
      .. Describe in more detail and use example of anamorphic lens. For some examples, see The Pixel Aspect Ratio Acid Test: http://frs.badcoffee.info/PAR_AcidTest/ and https://ia800900.us.archive.org/11/items/TvTestCard/TvTestCard_512kb.mp4 and https://www.dpreview.com/articles/5787493634/shooting-photos-with-anamorphic-lenses-is-a-fun-way-to-get-out-of-a-creative-rut

      アナモルフィックレンズの詳しい説明と使用例。いくつかの例については、以下の「ピクセル アスペクト比 Acid テスト」を参照してください。
      - http://frs.badcoffee.info/PAR_AcidTest/
      - https://ia800900.us.archive.org/11/items/TvTestCard/TvTestCard_512kb.mp4
      - https://ia800900.us.archive.org/11/items/TvTestCard/TvTestCard_512kb.mp4
      - https://www.dpreview.com/articles/5787493634/shooting-photos-with-anamorphic-lenses-is-a-fun-way-to-get-out-of-a-creative-rut)

RenderRegion/Crop to Render Region
   .. These options cannot be used in the VSE and, if set, will result in an error message ``Border rendering is not supported by sequencer``.
   これらのオプションは VSE では使用できず、設定するとエラー メッセージ ``Border rendering is not supported by sequencer`` が表示されます。

Frame Rate
   .. The number of frames that are displayed per second. The drop-down menu gives several common frame rates (23.98, 24, 25, 29.97, 30, ...). These presets refer to the different standards: NTSC (30 fps, mostly in North-America) and PAL/SECAM (25 fps, mostly Europe) and the necessary adjustments made in the 1950's to adapt  to color TV (23.98 and 29.97). Other frame rates can be used by selecting Custom. You can enter then a FPS and base number. The custom framerate is the result of: ``FPS / base number``. For example, to simulate a 25 fps preset, you can enter FPS = 25 and base = 1 or FPS = 50 and base = 2.

   1 秒あたりに表示されるフレーム数。ドロップダウン メニューには、いくつかの一般的なフレーム レート (23.98、24、25、29.97、30 など) が表示されます。

   これらのプリセットはさまざまな規格を参照しています: NTSC (30 fps、主に北米) と PAL/SECAM (25 fps、主にヨーロッパ)と、1950 年代にカラーテレビ (23.98 および 29.97)を採用するために行われた必要な調整です。

   [Custom]を選択すると、他のフレーム レートを使用できます。FPS とベースの値を入力できます。カスタム フレームレートは ``FPS / base number`` の結果です。たとえば、25 fps プリセットをシミュレートするには、FPS = 25 および Base = 1 または FPS = 50 および Base = 2 を入力できます。

   .. When the first video strip is added to the sequencer, the frame rate of the project is automatically set to the frame rate of that strip. Adding a second strip with a different frame rate -even if the first strip is deleted- will not change that setting. Blender VSE cannot handle different frame rates in one project. You will not get a warning, besides some odd-looking audio strips and slow or fast motion effects.

   最初のビデオ ストリップが Sequencer に追加されると、プロジェクトのフレーム レートがそのストリップのフレーム レートに自動的に設定されます [#f3]_ 。
   フレーム レートが異なる 2 番目のストリップを追加しても、最初のストリップが削除された場合でも、その設定は変更されません。
   Blender VSE は 1 つのプロジェクト内で異なるフレーム レートを処理できません。奇妙なオーディオ ストリップやスローまたはファスト モーション効果を除いて、警告は表示されません。

   .. figure:: /images/video_editing_setup_project-settings-fps.png
      :alt: Mixing of different FPS in one project


      図7: 1 つのプロジェクト内での異なるフレーム レートの混合

   .. Figure 6 contains 3 strips that were recorded at different frame rates. Their capture frame rate was respectively 30 fps, 60 fps and 120 fps. Each recording took about 15 seconds. The strip with fps = 30 was first added. This has set the presentation frame rate of the entire project to 30 fps. Later on, strips of 60 fps and 120 fps were added. This does not change the project presentation frame rate, but, of course, the capture frame rate of the strips remains unchanged.

   図7 には、異なるフレーム レートで記録された 3 つのストリップが含まれています。キャプチャ フレーム レートはそれぞれ 30 fps、60 fps、120 fps でした。それぞれ記録には約 15 秒かかりました。

   fps = 30 のストリップが最初に追加されました。これにより、プロジェクト全体のプレゼンテーション フレーム レートが 30 fps に設定されました。その後、60 fps と 120 fps のストリップが追加されました。これによってプロジェクトのプレゼンテーションのフレーム レートは変更されません。そして、当然のことながら、ストリップのキャプチャ フレーム レートは変更されません。

   .. All the audio strips have a duration of about 15 seconds because the audio is independent of the presentation frame rate. The movie strip with capture fps = 30 has also a duration of about 15 seconds. This is because the capture and presentation frame rate is equal. The strips with capture frame rate of 60 and 120 fps are much longer. The image of the watch in the preview shows that after about 15 seconds (first watch), only 6.55 and 2.83 s are passed on the second and third watch. This is because the second strip (60 fps) contains 16.877 s x 60 fps = 1012.62 (captured) frames that were presented at a framerate of 30 fps, which takes about 33.754 s. The real time on the watch is about 6.55 s. With a capture frame rate of 60 fps, this represents the image of frame 393. Again, frame 393 will be presented at time 13.1 s with a presentation frame rate of 30 fps. This is approximately the time you can see on the first watch (allow some differences due to different starting times). If these were real animation movies, you would see a slow-motion effect with strip 60 fps and even more with strip 120 fps.

   オーディオはプレゼンテーションのフレーム レートに依存しないため、すべてのオーディオ ストリップの長さは約 15 秒です。
   キャプチャ fps = 30 のムービー ストリップの長さも約 15 秒です。これは、キャプチャとプレゼンテーションのフレーム レートが等しいためです。

   キャプチャ フレーム レートが 60 fps および 120 fps のストリップは、はるかに長くなります。プレビューの時計の画像では、約 15 秒後 (最初の時計)、2 番目と 3 番目の時計では 6.55 秒と 2.83 秒しか経過していないことがわかります。

   これは、2 番目のストリップ (60 fps) には、30 fps のフレームレートで表示された 16.877 s x 60 fps = 1012.62 (キャプチャされた) フレームが含まれており、これには約 33.754 秒かかります。時計の実時間は約6.55秒です。
   60 fps のキャプチャ フレーム レートで、これはフレーム 393 の画像を表します。ここでも、フレーム 393 は 30 fps のプレゼンテーション フレーム レートで時間 13.1 秒に表示されます。これは、最初の時計で確認できるおおよその時間です (開始時間の違いによる多少の違いは許容してください)。

   これらが実際のアニメーション ムービーである場合、ストリップ 60 fps でスローモーション効果が見られ、ストリップ 120 fps ではさらに効果が得られます。

   .. So, it's important to set the presentation frame rate equal to the capture frame rate of the strips. You can find the capture frame rate of a strip in the Properties > Source > FPS.

   したがって、プレゼンテーション フレーム レートをストリップのキャプチャ フレーム レートと同じに設定することが重要です。ストリップのキャプチャ フレーム レートは、Sequencer の Sidebarにある [Strip]タブ > [Source] > [FPS] で確認できます。

   .. note::
      .. The determination of the capture frame rate of video can sometimes be a rabbit hole. Most devices (in particular smart phones) do not mention that they capture in Variable Frame Rate mode. So, when setting the capture frame rate to 30 FPS, in reality, the frame rate can vary between 29 fps and 31 fps. This has no repercussion for the Start and End of the strip but it can cause (small) problems with the synchronization of video and audio.

      ビデオのキャプチャ フレーム レートの決定は、場合によっては難しい場合があります。ほとんどのデバイス (特にスマートフォン) では、可変フレーム レート モードでキャプチャすることについて言及していません。したがって、キャプチャ フレーム レートを 30 FPS に設定すると、実際にはフレーム レートは 29 fps から 31 fps の間で変化する可能性があります。これはストリップの開始と終了には影響しませんが、ビデオとオーディオの同期に（小規模な）問題が発生する可能性があります。

      .. In the section Extra Tools, we have provided a solution to convert a video from variable rate to fixed and to change the FPS.

      :doc:`Extra Tools > FFMPEG </extra-tools/ffmpeg>` セクションでは、ビデオを可変レートから固定レートに変換し、FPS を変更するソリューションを提供しました。 [#f4]_

.. admonition:: Reference
   :class: refbox

   =============   ==============================================================
   **Name**:       *Dimensions*
   **Context**:    Video Sequence Editor > Properties
   **Location**:   Tabs > Output Properties > **Frame range**
   =============   ==============================================================

Frame Start/End/Step
   .. The sequencer timeline can contain multiple strips, spread over over several hundreds of frames. You don't need to render all these frames. With the Start and End fields, you can limit the output range.
   Sequencer のタイムラインには、数百のフレームにまたがる複数のストリップを含めることができます。これらすべてのフレームをレンダリングする必要はありません。 Start フィールドと End フィールドを使用して、出力範囲を制限できます。

Step
   .. Controls the number of frames to advance by for each frame in the timeline. If the strip in the Sequencer contains 10 frames, then a step of 2 will render 5 frames (frames 1,3,5,7,9).
   タイムライン内の各フレームごとに進むフレーム数を制御します。Sequencer のストリップに 10 フレームが含まれている場合、ステップ 2 では 5 フレーム (フレーム 1、3、5、7、9) がレンダリングされます。


Time Stretching
   .. You can use this to speed up or slow down the playback of the whole project. For example, in figure 7, there are two indicators of the Current Frame. The Playhead is split into a blue line (the old frame number) and a blue box with the new frame number (which you actually see in the preview).
   これを使用して、プロジェクト全体の再生を高速化または低速化できます。たとえば、図8 には、現在のフレームの 2 つのインジケーターがあります。再生ヘッドは、青い線 (古いフレーム番号) と新しいフレーム番号を含む青いボックス (実際にプレビューで表示されます) に分割されます。

   Old
      .. The length in frames of the original animation.
      元のアニメーションのフレームの長さ。

   New
      .. The length in frames of the new animation.
      新しいアニメーションのフレームの長さ。


   .. figure:: /images/video_editing_setup_project-settings-time-remapping.png
      :alt: Time Remapping (Old:1, New:2)


      図8: 時間のリマッピング (Old:1, New:2)

.. admonition:: Reference
   :class: refbox

   =============   ==============================================================
   **Name**:       *Stereoscopy*
   **Context**:    Video Sequence Editor > Properties
   **Location**:   Tabs > Output Properties > **Stereoscopy**
   =============   ==============================================================

.. Stereoscopy is a technique to create the illusion of three-dimensional depth from a pair of two-dimensional images. These images resemble the way our left and right eye would perceive the real image. In Blender, it is very easy to create stereoscopic images or movies; just enable the option in Output Properties > Stereoscopy > Stereo 3D. For more information; see `Stereoscopy <https://docs.blender.org/manual/en/dev/render/output/properties/stereoscopy/index.html>`_ in the Blender manual.

Stereoscopyは、一対の 2 次元画像から 3 次元の奥行きの錯覚を作り出す技術です。これらの画像は、私たちの左目と右目が実際の画像を認識する方法に似ています。 Blender では、立体的な画像やムービーを非常に簡単に作成できます。 [Output]プロパティー > [Stereoscopy] > [Stereo 3D] でオプションを有効にするだけです。詳細については; Blender マニュアルの `Stereoscopy <https://docs.blender.org/manual/en/dev/render/output/properties/stereoscopy/index.html>`_ を参照してください。

.. Editing a stereoscopic movie in the Blender VSE is a two-step process:
Blender VSE での Stereoscopy ムービーの編集は、次の 2 段階のプロセスです。

 .. * Enable the Stereoscopy option under output Properties > Stereoscopy > Stereo 3D. This will also add a new panel in the Source properties.
 .. * Select the stereoscopic strip and enable the *Use Multi-View* option in the Source panel of the movie strip. This option is only available after you have completed step 1. Choose the appropriate Views Format. This depends on the format of the source file. If the image pair is saved as two individual files; select *Individual*. If the image pair is saved as one file, with both images side-by-side, select Stereo 3D and set the Stereo Mode to Side-by-Side.
 * [Output]プロパティー > [Stereoscopy] > [Stereo 3D] で、 Stereoscopy オプションを有効にします。これにより、ストリップの [Source]プロパティに新しいパネルも追加されます。
 * Stereoscopyが有効になったストリップを選択し、ムービー ストリップの [Source] パネルで[Use Multi-View]オプションを有効にします。このオプションは、ステップ 1 を完了した後にのみ使用できます。適切なビュー形式を選択します。これはソース ファイルの形式によって異なります。画像ペアが 2 つの個別のファイルとして保存される場合。[Individual] を選択します。画像ペアが両方の画像を並べて 1 つのファイルとして保存する場合は、[Stereo 3D] を選択し、[Stereo Mode] を [Side-by-Side] に設定します。

.. admonition:: Reference
   :class: refbox

   =============   ==============================================================
   **Name**:       *Output*
   **Context**:    Video Sequence Editor > Properties
   **Location**:   Tabs > Output Properties > **Output**
   =============   ==============================================================


.. figure:: /images/video_editing_setup_project-settings-output.png
   :alt: Render Output properties
   :align: right
   :scale: 70%

   図9: レンダリング出力プロパティ

.. Figure 8 shows the expanded Output panel of the Output properties. Here you define the location and file format of your rendered project. In figure 8, the FFmpeg Video File Format is selected. The other possible file formats are shown in figure 9.
図9は、[Output] プロパティの展開された [Output]パネルを示しています。ここでは、プロジェクトのレンダリング結果の保存場所とファイル形式を定義します。図9 では、FFmpeg ビデオ ファイル形式が選択されています。他の可能なファイル形式を図10 に示します。

Output Path
   .. In the :doc:`previous section </video_editing/setup/directory-structure>`, we described a possible directory structure to hold all files that are related to your video project. In this structure, the rendered output could be stored in 3-2-Render. Because the Blend-file is stored at 3-1-Blend-file, the Output File Path should be ``//../3-2-render/``. The first // is the Blender-notation for the directory containing the current Blend-file. Depending on your choices about the File Format, you can add a file name or a directory name. The File Path ``//../3-2-render/myProject-v01.mp4`` will create a file *myProject-v01.mp4* in the specified directory (3-2-render). If you omit the extension (e.g. ``//../3-2-render/myProject-v01``) and enable *Saving File Extensions* , then a file *myProject-v010001-0020.mp4* is generated for a 20 frames project. If you render an image sequence, it is best to specify a subdirectory; place a / at the end as in ``//../3-2-render/myProject-v01/``. Rendering the project will then create the files *0001.png*, *0002.png*, *0003.png*, ... in the folder *3-2-render/myProject-v01*.

   :doc:`前のセクション </video_editing/setup/directory-structure>` では、ビデオ プロジェクトに関連するすべてのファイルを保持するために考えられるディレクトリ構造について説明しました。この構造では、レンダリングされた出力を 3-2-Render に保存できます。 blend ファイルは 3-1-Blend-file に保存されているため、出力ファイル パスは ``//../3-2-render/`` である必要があります。

   最初の **//** は、現在の blend ファイルを含むディレクトリの Blender 表記です。

   ファイル形式に関する選択に応じて、ファイル名またはディレクトリ名を追加できます。
   ファイル ``//../3-2-render/myProject-v01.mp4`` パスにより、指定されたディレクト(3-2-render)にファイル *myProject-v01.mp4* が作成されます 。

   拡張子を ``//../3-2-render/myProject-v01`` のように省略した場合、*Saving File Extensions* を有効にすると、20 フレームのプロジェクトに対してファイル *myProject-v010001-0020.mp4* が生成されます。

   イメージ シーケンスをレンダリングする場合は、サブディレクトリを指定することをお勧めします。 ``//../3-2-render/myProject-v01/`` のように最後に / を置きます。プロジェクトをレンダリングすると、ファイル0001.png、0002.png、0003.png ... がフォルダー *3-2-render/myProject-v01* に作成されます。


   Saving File Extensions
      .. Enabling this option will add the appropriate file extension to the file name (see figure 9 for the possible file formats).
      このオプションを有効にすると、ファイル名に適切なファイル拡張子が追加されます (使用可能なファイル形式については、図10 を参照)。
   Cache result
      .. Enabling tis option will save the render Cache to EXR files. This is useful for heavy compositing but it affects indirectly the rendered scenes.

      このオプションを有効にすると、レンダー キャッシュが EXR ファイルに保存されます。これは大量の合成に役立ちますが、レンダリングされたシーンに間接的に影響します。
Color
   .. Choose BW for saving grayscale images, RGB for saving color images (red, green and blue channels), and RGBA for saving color images with transparency enabled (red, green, blue and alpha channels). The RGBA option is only available with certain file formats (see below). For example, the JPG file format does not have an alpha channel, while the PNG format does. Also, most video file formats don't have a transparency option.

   用途に応じて以下を選択します。

   - BW: グレースケール イメージを保存
   - RGB: カラー イメージ (赤、緑、青のチャネル) を保存
   - RGBA: 透明度を有効にしたカラー イメージ (赤、緑、青、アルファ チャネル) を保存

   RGBA オプションは、特定のファイル形式でのみ使用できます (下記を参照)。たとえば、JPG ファイル形式にはアルファ チャネルがありませんが、PNG 形式にはアルファ チャネルがあります。また、ほとんどのビデオ ファイル形式には透明度オプションがありません。


File Format
   .. You can render the sequencer content as as series of images (BMP, Iris, PNG, ..., TIFF; see figure 9) or as a movie which is, of course, also an *embedded* series of images.
   Sequencerのコンテンツは、一連の画像 (BMP、Iris、PNG、…、TIFF、 参照 図10) として、またはもちろん一連の画像が埋め込まれたムービーとしてレンダリングできます。

   .. figure:: /images/video_editing_setup_project-settings-output-file-format.png
      :alt: File formats


      図10: ファイルフォーマット

   .. Which one should you choose? Depending on your choice, several additional fields are added in the sidebar. All possible Image and Movie formats are described in detail in the `section Output <https://docs.blender.org/manual/en/dev/render/output/properties/output.html>`_ of the docs with an overview of all `Video & Audio Formats <https://docs.blender.org/manual/en/dev/files/media/video_formats.html>`_ and `graphics <https://docs.blender.org/manual/en/dev/files/media/image_formats.html>`_ formats (see figure 9 for a list).

   どれを選ぶべきですか?

   選択された画像形式に応じて、いくつかのフィールドが Sidebar に追加されます。

   考えられるすべての画像およびムービー形式については、すべての `Video & Audio Formats <https://docs.blender.org/manual/en/dev/files/media/video_formats.html>`_ と `graphics <https://docs.blender.org/manual/en/dev/files/media/image_formats.html>`_ 形式の概要とともに、ドキュメントの `Output セクション <https://docs.blender.org/manual/en/dev/render/output/properties/output.html>`_ で詳しく説明されています(リストについては図10を参照)。

   .. Warning::
      .. It's important to keep in mind that Blender is foremost a 3D and 2D modeling and animation program. Artwork is mostly created and rendered from within the 3D View or Grease Pencil workspace. As an artist, you have full control on resolution, composition, speed, color, .... As a video editor, however, you usually work with existing material from camera output; where many parameters are already fixed. The Output settings therefore are for a great deal dictated by the imported footage.
      Blender は何よりも 3D および 2D モデリングおよびアニメーション プログラムであることを心に留めておくことが重要です。アートワークは主に、3D ビューまたはグリース ペンシル ワークスペース内から作成およびレンダリングされます。アーティストは、解像度、構成、速度、色などを完全に制御できます。ただし、ビデオ編集者は通常、カメラ出力からの既存の素材を使用して作業します。ここでは、多くのパラメータがすでに固定されています。したがって、出力設定はインポートされた映像によって大きく左右されます。

   .. If you are in the Video Editing Workspace, the default is set to a FFmpeg Video with H.264 as default video codec and AAC as audio codec. Other workspaces set the default to PNG Image Sequence and the Blender docs and many tutorials favor this approach. It's easier to stop & restart the render process (for example, in case of a crash or when you need your computer for something else). You can choose a high-quality, lossless format (e.g. OpenEXR) that's ideal for post-processing such as color grading or VFX. You can use a render farm, ... These advantages, however, are much more obvious in a 3D-animation creation process (which is the main focus of Blender), where you have full-control over the image quality. It is less obvious in a video editing workflow, where the quality of the source material is usually fixed; e.g. your footage is already shot and for example, creating a openEXR image sequence from H.264 footage will not increase the quality of it. If you saved your project as an image sequence, you also need to save the audio separately. And, in the end, you probably will need a single movie-file to hand over to your client. So, in a typical video editing workflow a single movie file format (FFMpeg Video) is much more common.

   Video Editing Workspace にいる場合、デフォルトでは、以下に設定されています。

   - File Format: **FFmpeg Video**
   - Video Codec: **H.264**
   - Audio Codec: **AAC**

   他のワークスペースではデフォルトが、以下に設定されており、

   - File Format: **PNG** (Image Sequence)

   Blender ドキュメントや多くのチュートリアルではこのアプローチが好まれています。

   レンダリング プロセスを停止して再起動することが簡単になります (たとえば、クラッシュが発生した場合や、別の目的でコンピュータが必要な場合)。

   カラー グレーディングや VFX などの後処理に最適な、高品質のロスレス形式 (OpenEXR など) を選択できます。

   レンダー ファームを使用することもできます。ただし、これらの利点は、画質を完全に制御できる 3D アニメーション作成プロセス (Blender の主な焦点) でより顕著になります。

   ソース素材の品質が通常固定されているビデオ編集ワークフローでは、このことはあまり明らかではありません。たとえば、映像はすでに撮影されており、たとえば、H.264 映像から openEXR イメージ シーケンスを作成しても、その品質は向上しません。プロジェクトを画像シーケンスとして保存した場合は、オーディオも個別に保存する必要があります。そして最終的には、おそらく 1 つのムービー ファイルをクライアントに渡す必要があるでしょう。

   したがって、一般的なビデオ編集ワークフローでは、単一のムービー ファイル形式 (FFMpeg Video) がはるかに一般的です。

   .. note::
      .. A 1080P video with 30 fps and 10 seconds duration has an uncompressed file size of 1080 x 1920 (dimension) x 3 (color channels) x 30 (fps) x 10 (duration) =  1.866.240.000 bytes or 1.73 GB. In most cases, this file is too big and should be compressed with for example, the H.264 codec. This codec can yield compression ratios from 1:50 to about 1:200 (200 bytes are compressed into 1 byte), reducing the above file size to about 36 MB - 9 MB. The following concepts are important to keep in mind:
      30 fps、10 秒の 1080P ビデオの非圧縮ファイル サイズは、1080 x 1920 (dimension) x 3 (カラー チャネル) x 30 (fps) x 10 (秒) = 1.866.240.000 バイトまたは 1.73 GB です。ほとんどの場合、このファイルは大きすぎるため、H.264 コーデックなどで圧縮する必要があります。このコーデックは、1:50 ～ 約 1:200 (200 バイトが 1 バイトに圧縮される) の圧縮率を実現し、上記のファイル サイズを約 36 MB ～ 9 MB に削減します。次の概念に留意することが重要です。

      .. * intraframe compression: instead of coding every pixel of a frame, only the differences between pixels are encoded. For example, for a completely black frame you need only to encode the color and the info that it applies to the whole frame (or to certain blocks, ...).
      .. * interframe compression: the frames in an image sequence are not all completely different. So, in theory, it's sufficient to encode the first frame (called a key frame or I-frame) and from then on only the differences.  This could work very well in a play-forward stream. In a typical video editing environment (with scrubbing, play backwards, jumping) however, this is a bad compression technique. To move one frame backwards, you have to process all the previous frames until the last keyframe. The term GOP (Group of Pictures) refers to the number of frames that are connected to one keyframe. The bigger the GOP size, the more compression but also the more processing needed to edit.
      .. * Lossy compression: the result of the compression is that some information is deleted from the file. Most of the time, this is not or hardly noticeable with the human eye. The JPEG image format is a lossy file format. WEBM/VP9 and Theora are lossy video codes. AAC is a lossy audio codec.
      .. * Lossless compression: the compressed file -although smaller- contains exact the same information as the uncompressed one. It is possible to reconstruct the original image from the lossless compressed file. The PNG image format is a lossless file format.  FFmpeg video codec #1 and HuffYUV are lossless video codecs. FLAC is a lossless audio codec.

      * フレーム内圧縮: フレームのすべてのピクセルをコーディングする代わりに、ピクセル間の差分のみがエンコードされます。たとえば、完全に黒いフレームの場合、フレーム全体 (または特定のブロックなど) に適用される色と情報をエンコードするだけで済みます。

      * フレーム間圧縮: イメージ シーケンス内のフレームがすべて完全に異なるわけではありません。したがって、理論的には、最初のフレーム (キー フレームまたは I フレームと呼ばれます) をエンコードし、それ以降は差分のみをエンコードすれば十分です。これは、再生ストリームでは非常にうまく機能する可能性があります。ただし、一般的なビデオ編集環境 (スクラブ、逆再生、ジャンプなど) では、これは不適切な圧縮手法です。 1 フレーム後方に移動するには、最後のキーフレームまで前のフレームをすべて処理する必要があります。 GOP (Group of Pictures) という用語は、1 つのキーフレームに接続されているフレームの数を指します。 GOP サイズが大きいほど圧縮率は高くなりますが、編集に必要な処理も多くなります。

      * 非可逆圧縮: 圧縮の結果、一部の情報がファイルから削除されます。ほとんどの場合、これは人間の目では気づかないか、ほとんどわかりません。 JPEG 画像形式は非可逆ファイル形式です。 WEBM/VP9 および Theora は非可逆ビデオ コードです。 AAC は非可逆オーディオ コーデックです。

      * 可逆圧縮: 圧縮ファイルには、圧縮されていないファイルとまったく同じ情報が含まれていますが、サイズは小さくなります。可逆圧縮ファイルから元の画像を復元することが可能です。 PNG 画像形式はロスレス ファイル形式です。 FFmpeg ビデオ コーデック #1 および HuffYUV はロスレス ビデオ コーデックです。 FLAC はロスレス オーディオ コーデックです。

      .. Some codecs have a lossy and lossless variant (for example DNxHD, H.264). Wikipedia maintains an extensive `list of lossy and lossless video and audio codecs <https://en.wikipedia.org/wiki/List_of_codecs#Lossless_compression>`_ .
      一部のコーデックには、不可逆および可逆のバリアントがあります (DNxHD、H.264 など)。 Wikipedia は、`list of lossy and lossless video and audio codecs <https://en.wikipedia.org/wiki/List_of_codecs#Lossless_compression>`_ を管理しています。

   AVI JPEG
      .. In the first two choices of figure 9 (AVI JPEG and AVI Raw), the term AVI (Audio Video Interleaved) refers to the container: a file format developed by Microsoft in 1992. AVI JPEG uses the Motion JPEG (M-JPEG or MJPEG) codec in which each video frame is compressed separately as a JPEG image. So, this codec uses only intraframe compression and is thus very well suited for video editing purposes but also results in a bigger file size (because it's only intraframe compression). It is also a lossy compression because it uses the JPEG codec. Audio is not embedded in the container and should be exported separately.
      図10 の最初の 2 つの選択肢 (AVI JPEG および AVI Raw)にあります。 AVI (Audio Video Interleaved) という用語は、1992 年に Microsoft によって開発されたファイル形式であるコンテナを指します。AVI JPEG は、Motion JPEG (M-JPEG または MJPEG) を使用します。 ) 各ビデオ フレームが JPEG 画像として個別に圧縮されるコーデック。したがって、このコーデックはフレーム内圧縮のみを使用するため、ビデオ編集の目的に非常に適していますが、(フレーム内圧縮のみであるため) ファイル サイズも大きくなります。 JPEG コーデックを使用するため、非可逆圧縮でもあります。オーディオはコンテナに埋め込まれないため、個別にエクスポートする必要があります。
   AVI Raw
      .. AVI Raw doesn't use a codec as such and stores the raw images into the AVI-container. The file size is thus much greater but the quality and processing speed (besides the bigger frame size) are better. Audio is also not embedded. For a comparison, the original Spring Open movie (container: MPEG-4, video codec: AVC (Advanced Video Codec), Audio codec: AAC LC (Advanced Audio Codec Low Complexity) has a file size of 29.6 MB. The AVI Raw has a file size of 64.5 GB, the AVI JPEG has a file size of 1.87 GB; both without audio.
      AVI Raw はコーデック自体を使用せず、生の画像を A​​VI コンテナに保存します。したがって、ファイル サイズははるかに大きくなりますが、品質と処理速度は (フレーム サイズが大きくなることを除けば) 優れています。音声も埋め込まれていません。比較のために、オリジナルの Spring Open ムービー (コンテナ: MPEG-4、ビデオ コーデック: AVC (Advanced Video Codec)、オーディオ コーデック: AAC LC (Advanced Audio Codec Low Complexity)) のファイル サイズは 29.6 MB です。AVI Raw はファイル サイズは 64.5 GB、AVI JPEG のファイル サイズは 1.87 GB で、どちらも音声はありません。

      .. note::
         .. Due to this huge file size and the absence of audio, both formats should probably not be used as delivery format but as fallback.
         この巨大なファイル サイズと音声がないため、どちらの形式も配信形式としてではなく、フォールバックとして使用する必要があると考えられます。

   FFmpeg Video
      .. figure:: /images/video_editing_setup_project-settings-output-containers-codecs.png
         :alt: FFMpeg video settings
         :align: right
         :scale: 60%

         図11: FFmpeg Video settings


      .. FFmpeg video is an umbrella term for several containers and codecs. It uses the ffmpeg libraries under the hood to create the video file. When selecting this option, several *presets* are available: ``DVD``, ``H264 in Matroska``, ``H264 in Matroska for scrubbing``, ``H264 in MP4``, ``Ogg Theora``, ``WebM (VP9+Opus)``, and ``Xvid``.  Selecting one of these presets will set the encoding, video and audio options below to a pre-defined value. We describe only the very popular *H264 in MP4* and the related concepts. These are also applicable to the other presets.

      FFmpeg Video は、いくつかのコンテナとコーデックを総称した用語です。内部で ffmpeg ライブラリを使用してビデオ ファイルを作成します。

      このオプションを選択すると、いくつかのプリセットが使用可能になります: ``DVD``, ``H264 in Matroska``, ``H264 in Matroska for scrubbing``, ``H264 in MP4``, ``Ogg Theora``, ``WebM (VP9+Opus)``, ``Xvid`` 。

      これらのプリセットのいずれかを選択すると、以降につづく、エンコード、ビデオ、およびオーディオのオプションが事前定義された値に設定されます。ここでは、非常に人気のある *H264 in MP4* と関連する概念のみについて説明します。これらは他のプリセットにも適用されます。

      Encoding
         .. Selecting the FFmpeg Video File Format will add the Encoding, Video, and Audio section to the side panel. A distinction should be made between the concepts *container* and *codec*. For example, in figure 10, the container is MPEG-4 (with file extension mp4), the Video Codec is H.264 and the Audio Codec is AAC. A container "contains" the various components of a video: the stream of images, the sound, subtitles, metadata. A codec is software or hardware that compresses and decompresses digital video or audio.

         FFmpeg ビデオ ファイル形式を選択すると、サイド パネルにエンコーディング、ビデオ、およびオーディオ セクションが追加されます。コンテナとコーデックという概念を区別する必要があります。たとえば、図 11 では、コンテナは MPEG-4 (ファイル拡張子は mp4)、ビデオ コーデックは H.264、オーディオ コーデックは AAC です。コンテナには、画像のストリーム、サウンド、字幕、メタデータなど、ビデオのさまざまなコンポーネントが「含まれています」。コーデックは、デジタル ビデオまたはオーディオを圧縮および解凍するソフトウェアまたはハードウェアです。

         Container
            .. A container specifies how the data (audio, video, subtitles, ...) is stored in the video file, and how transporting and presenting this info can be organized. You can recognize the container through the file extension (.mp4, .mov, ...). This is not a waterproof method however. For example, you can easily change the file extension from .mp4 to .mov or .avi and still be able to view the video with most players. To detect the container signature (within the file), you need extra-software such as FFprobe or MediaInfo (see `Extratools </extra-tools>`_).

            コンテナは、データ (オーディオ、ビデオ、字幕など) をビデオ ファイルに保存する方法と、この情報の転送と表示をどのように構成するかを指定します。コンテナはファイル拡張子 (.mp4、.mov など) によって識別できます。ただし、これは完全な識別方法ではありません。たとえば、ファイル拡張子を .mp4 から .mov または .avi に簡単に変更しても、ほとんどのプレーヤーでビデオを表示できます。 (ファイル内の) コンテナーの署名を検出するには、FFprobe や MediaInfo などの追加ソフトウェアが必要です ( `Extratools </extra-tools>`_ を参照)。

            .. The available container file formats are: ``MPEG-1``, ``MPEG-2``, ``MPEG-4``, ``AVI``, ``Quicktime``, ``DV``, ``Ogg``, ``Matroska``, ``Flash``, and ``WebM``.

            使用可能なコンテナ ファイル形式は ``MPEG-1``, ``MPEG-2``, ``MPEG-4``, ``AVI``, ``Quicktime``, ``DV``, ``Ogg``, ``Matroska``, ``Flash``, ``WebM`` です。

            .. A container can be tied to a specific codec. For example, the ``MPEG-1``and ``MPEG-2`` containers *enforce* the video codec (you cannot choose one), so that you can only define quality parameters, and the audio codec. For the ``MPEG-1`` container the only valid audio codecs are AC3, MP2, and MP3; *although all audio codecs are available*. You can select the AC3 audio codec without any render error but the sound however is not stored. And, if the MP2 audio codec is selected, then the Bitrate must be less than 128 bps. Another example: the webM and Ogg file format can only contain a Vorbis and Opus codec.

            コンテナは特定のコーデックに関連付けることができます。たとえば、 ``MPEG-1`` と ``MPEG2`` コンテナではビデオ コーデック を *強制* (選択することはできません) します。 品質パラメータとオーディオ コーデックのみを定義できます。 ``MPEG-1`` コンテナーの場合、有効なオーディオ コーデックは AC3、MP2、および MP3 のみです。ただし、すべてのオーディオ コーデックが利用可能です。レンダリング エラーなしで AC3 オーディオ コーデックを選択できますが、サウンドは保存されません。また、MP2 オーディオ コーデックが選択されている場合、ビットレートは 128 bps 未満である必要があります。
            別の例としては: webM および Ogg ファイル形式には、Vorbis および Opus コーデックのみを含めることができます。

            .. note::
               .. If you combine incompatible codecs or containers, the Render Animation command will show an (easy to miss) error message in the statusbar such as ``Could not initialize streams, probably unsupported codec combination``. However, a non-playable output file is yet produced.
               互換性のないコーデックまたはコンテナを組み合わせると、[Render Animation] コマンドによりステータス バーに  ``Could not initialize streams, probably unsupported codec combination`` エラー メッセージ (見逃しやすい) が表示されます。にもかかわらず、再生できない出力ファイルはまだ生成されています。

            .. Wikipedia has a very extensive documentation on all available `container formats <https://en.wikipedia.org/wiki/Comparison_of_video_container_formats>`_ with an overview table of the valid `container-codec combinations <https://en.wikipedia.org/wiki/Comparison_of_video_container_formats#Video_coding_formats_support>`_. A very good YouTube tutorial about the difference between container and codec is `Explaining Digital Video: Formats, Codecs & Containers <https://www.youtube.com/watch?v=-4NXxY4maYc>`_

            Wikipedia には、有効な `container-codec combinations <https://en.wikipedia.org/wiki/Comparison_of_video_container_formats#Video_coding_formats_support>`_  の概要表を含む、利用可能なすべての `container formats <https://en.wikipedia.org/wiki/Comparison_of_video_container_formats>`_ に関する非常に広範なドキュメントがあります。

            コンテナとコーデックの違いについての非常に優れた YouTube チュートリアルは、`Explaining Digital Video: Formats, Codecs & Containers <https://www.youtube.com/watch?v=-4NXxY4maYc>`_ です。

         Autosplit
            .. If the output file is bigger than 2 GB, you can *Autosplit* the output in chunks of max. 2 GB. Each chunk  can be played separately.
            出力ファイルが 2 GB より大きい場合は、出力を最大 2 GB のチャンクに自動分割できます。 2GB。各チャンクは個別に再生できます。
         Video
            Video Codec
               .. The name CODEC stands for Compressor/Decompressor (sometimes also referred to as coding/decoding). It is the software that compresses the file (see above). Available options are: ``No Video``, ``DNxHD``, ``DV``, ``FFmpeg video codec #1``, ``Flash Video``, ``H.264``, ``HuffYUV``, ``MPEG-1``, ``MPEG-2``, ``MPEG-4 (divx)``, ``PNG``, ``QT rle/QT Animation``, ``Theora``, and  ``WEBM/VP9``.
               CODEC という名前は、Compressor/Decompressor (コーディング/デコーディングとも呼ばれる) の略です。ファイルを圧縮するソフトウェアです (上記を参照)。使用可能なオプションは以下です。

               ``No Video``, ``DNxHD``, ``DV``, ``FFmpeg video codec #1``, ``Flash Video``, ``H.264``, ``HuffYUV``, ``MPEG-1``, ``MPEG-2``, ``MPEG-4 (divx)``, ``PNG``, ``QT rle/QT Animation``, ``Theora``,  ``WEBM/VP9``.

               .. The goal of (lossy) video encoding is to reduce the file size of the original input file, while retaining as much quality as possible. So, there is a tradeoff between size and quality.
               (非可逆) ビデオ エンコードの目標は、品質を可能な限り維持しながら、元の入力ファイルのファイル サイズを削減することです。したがって、サイズと品質の間にはトレードオフがあります。

               .. Depending on the selected video codec, some of the fields below are not displayed. For example, if you select the No Video codec, no additional fields are shown.
               選択したビデオ コーデックによっては、以降のフィールドの一部が表示されません。たとえば、[No Video] コーデックを選択した場合、追加のフィールドは表示されません。

               .. Warning::
                  .. The description below is based on the popular H.264 video codec. Blender has opted to hide some of the complexity of this codec. Other codecs require that you explicitly specify all necessary attributes. In the text we will refer to those implicit settings.
                  以下の説明は、一般的な H.264 ビデオ コーデックに基づいています。 Blender は、このコーデックの複雑さの一部を隠すことを選択しました。他のコーデックでは、必要な属性をすべて明示的に指定する必要があります。本文では、これらの暗黙的な設定について言及します。

            Output quality
               .. The default is set to Medium Quality. The image quality of a video is dependent of the bitrate; i.e. the number of bits used per unit time. Setting a high bitrate will result in a higher quality because you have more bits per unit time to dislay the image.
               デフォルトは [Medium Quality] に設定されています。ビデオの画質はビットレートに依存します。つまり、単位時間あたりに使用されるビット数です。高いビットレートを設定すると、画像を表示する単位時間あたりのビット数が増えるため、品質が向上します。

               .. With FFmpeg, you can use a constant bitrate or settle with one of the predefined Quality levels. With a constant bitrate the number of bits per unit of time is always the same, no matter how complex the image stream is. A variable bitrate can adapt to the complexity of the stream and use a lower bitrate with for example a motionless video. A variable bitrate is automatically set if you select one of the predefined quality levels.
               FFmpeg を使用すると、一定のビットレートを使用することも、事前定義された品質レベルの 1 つで解決することもできます。ビットレートが一定の場合、画像ストリームがどれほど複雑であっても、単位時間あたりのビット数は常に同じです。可変ビットレートはストリームの複雑さに適応し、動きのないビデオなどではより低いビットレートを使用できます。事前定義された品質レベルの 1 つを選択すると、可変ビットレートが自動的に設定されます。

               Quality levels (variable bitrate)
                  .. You need to give some indication about the desired quality of the output; otherwise the codec could always settle for the lowest bitrate, which is of course also the lowest quality.
                  出力の望ましい品質について何らかの指示を与える必要があります。そうしないと、コーデックは常に最低のビットレートに落ち着く可能性があり、これは当然ながら最低の品質でもあります。

                  .. Blender has opted to use `verbal labels <https://blender.stackexchange.com/questions/93048/what-numerical-crf-values-do-the-assorted-output-qualities-correspond-to-in-the>`_; which are a translation of FFmpeg's `Constant Rate Factor <http://trac.ffmpeg.org/wiki/Encode/H.264>`_ (CRF): a value between 0 and 51, where lower values would result in better quality (more bits per frame), at the expense of higher file sizes. Higher values mean more compression, but at some time you will notice the quality degradation. A change of ± 6 should result in about half/double the file size.

                  Blender は `verbal labels <https://blender.stackexchange.com/questions/93048/what-numerical-crf-values-do-the-assorted-output-qualities-correspond-to-in-the>`_ を使用することを選択しました。これは FFmpeg の `Constant Rate Factor <http://trac.ffmpeg.org/wiki/Encode/H.264>`_ (CRF)の変換です。0 から 51 までの値で、値が低いほど、ファイル サイズは大きくなりますが、品質が向上します (フレームあたりのビット数が増加します)。値が大きいほど圧縮率が高くなりますが、ある時点で品質の低下に気づくことがあります。 ± 6 の変更により、ファイル サイズは約半分または 2 倍になります。

                  .. figure:: /images/video_editing_setup_project-settings-output-quality.png
                     :alt: Output Quality

                     図12: 出力品質と FFmpeg の Constant Rate Factor (CRF) 値

               Constant Bitrate
                  .. In FFmpeg, there is no native or true CBR mode, but Blender "simulates" a constant bit rate setting by tuning the parameters of a one-pass average bitrate encode. You need to set the following, additional input fields. However, Bitrate, Minimum, and Maximum can all be set to the same value.

                  FFmpeg にはネイティブまたは真の CBR モードはありませんが、Blender はワンパス平均ビットレート エンコードのパラメーターを調整することで、固定ビット レート設定を「シミュレート」します。次の追加の入力フィールドを設定する必要があります。ただし、ビットレート、最小値、および最大値はすべて同じ値に設定できます。

                  Bitrate
                     .. Bitrate is the amount of data encoded for a unit of time. For streaming, it is usually expressed in megabits per second (Mbps) for video, and in kilobits per second (kbps) for audio. The default is set to 6000 bps. As a comparison, the recommended video bitrate for YouTube uploads is set to 8 Mbps for 1080p and 5 Mbps for 720p.
                     ビットレートは、単位時間あたりにエンコードされるデータの量です。ストリーミングの場合、通常、ビデオの場合はメガビット/秒 (Mbps)、オーディオの場合はキロビット/秒 (kbps) で表されます。デフォルトは 6000 bps に設定されています。比較として、YouTube アップロードの推奨ビデオ ビットレートは、1080p の場合は 8 Mbps、720p の場合は 5 Mbps に設定されています。
                  Minimum
                     .. Although the Constant Bitrate option is selected, the encoder will fluctuate around this number. You can set a minimum.
                     [Constant Bitrate] オプションが選択されていますが、エンコーダーはこの数値を中心に変動します。最小値を設定できます。
                  Maximum
                     .. However, the maximum is probably more important. If you suspect that your viewer has limited bandwidth, you can specify this maximum. The encoder will never encode in a higher bitrate.
                     ただし、最大値の方がおそらくより重要です。ビューアの帯域幅が制限されていると思われる場合は、この最大値を指定できます。エンコーダーは、これより高いビットレートでエンコードすることはありません。
                  Buffer
                     .. This is the "rate control buffer", so it will enforce your requested "average" (the value you set with Bitrate) over the buffer window. It is assumed that the receiver / player will buffer that much data, meaning that a fluctuation within that range is acceptable. The default is set to 1792 bits.
                     これは「レート制御バッファ」であるため、バッファ ウィンドウ全体で要求された「平均」（ビットレートで設定した値）を強制します。受信機/プレーヤーはその量のデータをバッファーすると想定されており、その範囲内の変動は許容されることを意味します。デフォルトは 1792 ビットに設定されています。
                  Mux Rate
                     .. Multiplexing is the process of combining separate video and audio streams into a single file, similar to packing a video file and .mp3 audio file in a zip-file. The value of Mux Rate is the maximum bit rate of the multiplexed stream. The default is set to 10080000.
                     Multiplexingとは、ビデオ ファイルと .mp3 オーディオ ファイルを zip ファイルにパックするのと同様に、別々のビデオ ストリームとオーディオ ストリームを 1 つのファイルに結合するプロセスです。 Mux Rate の値は、多重化ストリームの最大ビットレートです。デフォルトは 10080000 に設定されています。
                  Mux Packet size
                     .. Default: 2048. Reduces data fragmentation or muxer overhead depending on the source. The default is set to 2048.
                     デフォルト: 2048。ソースに応じて、データの断片化またはマルチプレクサのオーバーヘッドを削減します。デフォルトは 2048 に設定されています。
            Encoding speed
               .. Presets to change between a fast encode (bigger file size) and more compression (smaller file size). The available options: Slowest, Good, Realtime
               高速エンコード (より大きなファイル サイズ) とより多くの圧縮 (より小さなファイル サイズ) の間で変更するためのプリセット。利用可能なオプション: Slowest, Good, Realtime
            Keyframe Interval
               .. The number of pictures per Group of Pictures. The default value is 18. Set to 0 for “intraframe only” compressing, which disables inter-frame video compression. A higher number generally leads to a smaller file but needs a higher-powered device to replay it.
               画像グループごとの画像の数。デフォルト値は 18 です。「フレーム内のみ」圧縮の場合は 0 に設定すると、フレーム間ビデオ圧縮が無効になります。一般に、数値が大きいほどファイルは小さくなりますが、再生するには高性能のデバイスが必要です。

               .. The value of the Keyframe Interval depends on your goal. If you want to use this outputed video for further editing, then a small interval is better. To recreate a non-keyframe, you need to find the associated keyframe and apply all differences in between. If all frames are keyframes, then each frame can be recreated on its own; but, of course, the compression is minimal and the file size will be larger.
               キーフレーム間隔の値は目的によって異なります。この出力されたビデオをさらに編集に使用する場合は、間隔を短くすることをお勧めします。非キーフレームを再作成するには、関連するキーフレームを見つけて、その間のすべての差異を適用する必要があります。すべてのフレームがキーフレームの場合、各フレームを独自に再作成できます。ただし、当然のことながら、圧縮は最小限であり、ファイル サイズは大きくなります。

            Max B-frames
               .. B-frames are bi-directional frames. They use both previous and forward frames for data reference to get the highest amount of compression. The value is the maximum number of B‑frames between non-B-frames. Again, a small value will be beneficial for a video that needs to be edited.
               B フレームは双方向フレームです。最高の圧縮率を得るために、データ参照に前フレームと前フレームの両方を使用します。この値は、非 B フレーム間の B フレームの最大数です。繰り返しますが、編集が必要なビデオの場合は、値が小さい方が有利です。

         Audio
            .. Only certain audio codecs will be able to fit in your target output file; see `Guidelines for high quality lossy audio encoding <https://trac.ffmpeg.org/wiki/Encode/HighQualityAudio>`_ for an overview table.
            ターゲット出力ファイルに適合できるのは、特定のオーディオ コーデックのみです。概要表については、 `Guidelines for high quality lossy audio encoding <https://trac.ffmpeg.org/wiki/Encode/HighQualityAudio>`_ を参照してください。

            .. According to the FFmpeg docs, the quality of the available audio encoders could be ranked as folllows:
            .. Opus > Vorbis >= AAC > MP3 >= AC3 > aac > libtwolame > vorbis > mp2 > wmav2/wmav1

            FFmpeg ドキュメントによると、利用可能なオーディオ エンコーダの品質は次のようにランク付けされます:

            Opus > Vorbis >= AAC > MP3 >= AC3 > aac > libtwolame > vorbis > mp2 > wmav2/wmav1

            Audio Codec
               .. Available options: ``No Audio``, ``AAC``, ``AC3``, ``FLAC``, ``MP2``, ``MP3``, ``Opus``, ``PCM``, and ``Vorbis``.
               利用可能なオプション: ``No Audio``, ``AAC``, ``AC3``, ``FLAC``, ``MP2``, ``MP3``, ``Opus``, ``PCM``, and ``Vorbis``
               .. Advanced Audio Coding (AAC) is the successor format to MP3 and defined in MPEG-4 part 3.
               Audiocoding (AAC) は MP3 の後継フォーマットであり、MPEG-4 パート 3 で定義されています。
            Audio channels
               .. Available options: Mono, Stereo, 4 channels, 5.1 Surround, 7.1 Surround
               利用可能なオプション: Mono, Stereo, 4 channels, 5.1 Surround, 7.1 Surround
            Sample Rate
               .. The sample (sampling) rate is analogous to the frame rate or FPS (frames per second) measurement for videos. An analogue sound wave is measured or sampled at a regular interval and the result is stored in the audio stream/file. For audio, the minimum number of samples per second to unambiguously represent English speech is 8000 Hz or 8000 samples per second. Other common values are 44.100 Hz or 44.1kHz (music CD quality), and 48kHz (most common for audio tracks in movies). The default setting is 48000.
               サンプル (サンプリング) レートは、ビデオのフレーム レートまたは FPS (フレーム/秒) 測定に似ています。アナログ音波は一定の間隔で測定またはサンプリングされ、結果はオーディオ ストリーム/ファイルに保存されます。オーディオの場合、英語の音声を明確に表現するための 1 秒あたりの最小サンプル数は 8000 Hz、つまり 1 秒あたり 8000 サンプルです。その他の一般的な値は、44.100 Hz または 44.1 kHz (音楽 CD 品質)、および 48 kHz (映画のオーディオ トラックで最も一般的) です。デフォルト設定は 48000 です。
            Bit Rate
               .. For each codec, you can control the bit rate (quality) of the sound in the movie. Higher bit rates are bigger files that stream worse but sound better. Use powers of 2 for compatibility.
               コーデックごとに、動画の音声のビットレート（品質）を制御できます。ビット レートが高くなると、ファイルが大きくなり、ストリーミングは悪くなりますが、音質は良くなります。互換性を保つために 2 の累乗を使用します。

               .. For music, 64 (AAC)/96 (MP3) kbps is a good general-purpose setting that will sound good most listeners. This is the standard bitrate for podcasts, and it sounds great on most contemporary devices, including smart speakers and mobile devices. If bandwidth cost is a concern, you might consider using a lower setting. For enhanced listening, go higher.
               音楽の場合、64 (AAC)/96 (MP3) kbps は、ほとんどのリスナーが良好に聞こえる汎用的な設定です。これはポッドキャストの標準ビットレートであり、スマート スピーカーやモバイル デバイスなど、ほとんどの最新のデバイスで素晴らしい音質で聞こえます。帯域幅のコストが懸念される場合は、より低い設定の使用を検討してください。リスニングを強化するには、より高いレベルを設定します。

               .. As a rule of thumb, for audible transparency, use 64 kBit/s for each channel (so 128 kBit/s for stereo, 384 kBit/s for 5.1 surround sound) (see https://trac.ffmpeg.org/wiki/Encode/AAC )
               経験則として、可聴透明度を得るには、各チャンネルに 64 kBit/s を使用します (つまり、ステレオの場合は 128 kBit/s、5.1 サラウンド サウンドの場合は 384 kBit/s) ( https://trac.ffmpeg.org/wiki/Encode/AAC を参照)

               .. For talk, 32 (AAC)/64 (MP3) kbps is a good standard setting for most purposes. If you are particularly budget conscious, you can use a lower setting for talk radio and few people will notice the difference.

               会話の場合、32 (AAC)/64 (MP3) kbps がほとんどの目的に適した標準設定です。特に予算を重視している場合は、トークラジオに低い設定を使用できますが、違いに気づく人はほとんどいません。

               .. The minimum is 32 and maximum is 384 kbps. The default is set at 192
               最小値は 32、最大値は 384 kbps です。デフォルトは 192 に設定されています
            Volume
               .. Slider: default at 1
               スライダー: デフォルトは 1


.. admonition:: Reference
   :class: refbox

   =============   ==============================================================
   **Name**:       *Output*
   **Context**:    Video Sequence Editor > Properties
   **Location**:   Tabs > Output Properties > **Metadata**
   =============   ==============================================================


.. todo::
   Describe metadata

.. admonition:: Reference
   :class: refbox

   =============   ==============================================================
   **Name**:       *Output*
   **Context**:    Video Sequence Editor > Properties
   **Location**:   Tabs > Output Properties > **Post Processing**
   =============   ==============================================================




.. The Post Processing panel is used to control different options used to process your image after camera rendering have taken place.
[Post Processing] パネルは、カメラのレンダリングが行われた後に画像を処理するために使用されるさまざまなオプションを制御するために使用されます。


   .. figure:: /images/video_editing_setup_project-settings-output-post-processing.png
      :alt: Post processing options
      :align: right
      :scale: 60%

      図13: Post processing オプション

Compositing
   .. The output of the render process comes from the the Composite Output node of the compositor. Note that this option should be enabled *but* also the Use Nodes option in the compositor. If both conditions are not fulfilled, then the output of the active camera is used to render the images.
   レンダリング プロセスの出力は、コンポジターの Composite Output ノードから取得されます。このオプション *だけでなく* 、Compositer の [Use Note] オプションも有効にする必要があることに注意してください。両方の条件が満たされない場合は、アクティブな Camera の出力を使用してイメージがレンダリングされます。

Sequencer
   .. Renders the output of the Video Sequence editor, instead of the active camera or Compositor. If the sequence contains Scene strips, these will also be rendered as part of the pipeline. If Compositing is enabled (but see above), the Scene strip will be the output of the Compositor.

   アクティブな Camera または Compositer の代わりに、Video Sequence Editor の出力をレンダリングします。Sequencer  にシーン ストリップが含まれている場合、これらもパイプラインの一部としてレンダリングされます。[Compositing] が有効な場合 (ただし上記を参照)、シーン ストリップは Compositer の出力になります。

   .. If the Video Sequence Editor contains *only* audio strips, then the visual render output comes from the Composite Output node of the compositor or the active camera and the audio from the Sequencer.
   Video Sequence Editorにオーディオ ストリップのみが含まれている場合、ビジュアル レンダー出力は Compositer またはアクティブな Camera のコンポジット出力ノードから、オーディオは Sequencer から取得されます。

   .. If the Video Sequence Editor is *empty*, then the active camera or Composite Output node is rendered, even if the option Sequencer is enabled.
   Video Sequence Editor が空の場合は、Sequencer オプションが有効であっても、アクティブな Camera またはコンポジット出力ノードがレンダリングされます。

Dither
    .. Dithering is a technique for blurring pixels to prevent banding that is seen in areas of gradients, where stair-stepping appears between colors. Banding artifacts are more noticeable when gradients are longer, or less steep. Dithering was developed for graphics with low bit depths, meaning they had a limited range of possible colors.
    ディザリングは、色の間に階段状の段差が現れるグラデーション領域に見られるバンディングを防ぐためにピクセルをぼかす技術です。バンディング アーティファクトは、勾配が長い場合、または勾配が緩やかな場合により目立ちます。ディザリングは、ビット深度が低いグラフィックス向けに開発されました。つまり、使用できる色の範囲が限られています。

    .. Dithering works by taking pixel values and comparing them with a threshold and neighboring pixels then does calculations to generate the appropriate color. Dithering creates the perceived effect of a larger color palette by creating a sort of visual color mixing. For example, if you take a grid and distribute red and yellow pixels evenly across it, the image would appear to be orange.
    ディザリングは、ピクセル値を取得し、それらをしきい値と比較し、隣接するピクセルを計算して適切な色を生成することによって機能します。ディザリングは、一種の視覚的な色の混合を作成することにより、より大きなカラー パレットの知覚効果を作成します。たとえば、グリッドを作成し、赤と黄色のピクセルを均等に配置すると、画像はオレンジ色に見えます。

Some useful links:
----

* Discrete Cosine Transformation: https://www.youtube.com/watch?v=Q2aEzeMDHMA&t=33s
* JPEG compression: https://www.youtube.com/watch?v=Ba89cI9eIg8
* Video compression: https://www.youtube.com/watch?v=QoZ8pccsYo4
* Rate Control mode: https://slhck.info/video/2017/03/01/rate-control.html

.. rubric:: 訳注

.. [#f2] VSEは、Video Sequence Editorの略称
.. [#f1] Blender4.0の私の環境ではVSEのPreviewを :kbd:`LMB-Click` でステータスバーに情報が表示されました。一方 Renderウィンドウでは、 :kbd:`RMB-Click` で表示されました。
.. [#f3] :doc:`Edit > Montage > Add の'Use Movie Frame Rate'オプション </video_editing/edit/montage/add>` も確認してください。
.. [#f4] :doc:`Extra Tools > FFMPEG </extra-tools/ffmpeg>` には可変レートから固定レートへの変換の記述がない。 `video - FFMPEG: How to convert VFR to CFR without messing up the timing - Super User <https://superuser.com/a/1805395>`_ が参考になりそう。
