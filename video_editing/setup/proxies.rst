Proxies & cache
===============

Proxies
-------
.. _proxies:

.. Proxies are low-quality copies of high-quality raw footage. They are used as a substitute to ease the playback of high-quality source videos. Creating proxies can be done by either decreasing the resolution and/or decompressing the source files. They are transcoded in such a way that is optimal for real-time editing.  Nowadays, a 4K video file (3840 × 2160) is no exception anymore. With 30 fps, this can quickly become a burden to your computer's performance.

プロキシは、高品質の生映像の低品質コピーです。これらは、高品質のソース ビデオの再生を容易にするための代替品として使用されます。プロキシを作成するには、解像度を下げるか、ソース ファイルを解凍します。これらは、リアルタイム編集に最適な方法でトランスコードされます。今では4K動画ファイル（3840×2160）も例外ではなくなりました。 30 fps では、これはすぐにコンピュータのパフォーマンスに負担をかける可能性があります。


.. note::
   .. You can try it yourself by creating a 4K test movie (see :doc:`test files </video_editing/setup/creating-test-files>`) and adding it to the sequencer. Without proxies you will notice that scrubbing through the strip will stutter. Adding an effect (e.g. Gaussian Blur) will aggravate the problem.
   4K テスト ムービー ( :doc:`test files </extra-tools/creating-test-files>` を参照) を作成し、それをシーケンサーに追加することで、自分で試すことができます。プロキシを使用しないと、ストリップのスクラブが途切れることに気づくでしょう。エフェクト（ガウスぼかしなど）を追加すると、問題がさらに悪化します。

.. Using a 720p (1280×720) or a more optimized format will reduce the load on your computer. Proxies are only used to speed up the editing. For rendering out the final project, the original, high quality source files are used.

720p (1280×720) またはより最適化された形式を使用すると、コンピューターの負荷が軽減されます。プロキシは編集を高速化するためにのみ使用されます。最終プロジェクトのレンダリングには、オリジナルの高品質のソース ファイルが使用されます。

.. A very instructive video tutorial (for version 2.92) is made by `Blender Frenzy <https://www.youtube.com/watch?v=kfTJ2Wsmc9c>`_.
非常に有益なビデオ チュートリアル (バージョン 2.92 用) が `Blender Frenzy <https://www.youtube.com/watch?v=kfTJ2Wsmc9c>`_ によって作成されています。

.. The use of proxies is much simplified in Blender 2.93 and an average user shouldn't be worried about it any longer. Of course, understanding what happens under the hood can't harm! The following default settings take care of this automatic creation of the proxy files and make sure that everything will work right out of the box.

Blender 2.93 ではプロキシの使用が大幅に簡素化されており、平均的なユーザーはプロキシについて心配する必要はなくなりました。もちろん、内部で何が起こっているかを理解することは害にはなりません。次のデフォルト設定は、このプロキシ ファイルの自動作成を処理し、すべてがすぐに機能することを確認します。

.. * ``Proxy Setup`` : default set to ``Automatic`` (see figure 1-a)
.. * ``Proxy Render Size``: default set at ``100%`` (see figure 1-b)
.. * ``Use Proxies``: default set to ``True`` (see figure 1-b)
.. * ``Proxy Settings: Storage``: default set to ``Per Strip`` (see figure 1-g)

* ``Proxy Setup`` : デフォルト設定は ``Automatic`` (図1-a)
* ``Proxy Render Size``: デフォルト設定は ``100%`` (図1-b)
* ``Use Proxies``: デフォルト設定は ``True`` (図1-b)
* ``Proxy Settings: Storage``: デフォルト設定は ``Per Strip`` (図1-g)

.. figure:: /images/vse_setup_environment_proxies.svg
   :alt: Proxies

   図1: Proxy 構築プロセスの概要


.. 1. First and foremost, by default, proxies are now built automatically in the background. To enable or disable the Automatic Proxy Setup, go to the Edit > Preferences menu and select the System tab (see figure 1-a). You can choose between Manual or Automatic. If Automatic is chosen, several things occur after adding a movie or image sequence strip to the sequencer or after changing the View Settings of a strip (see figure 1-b).

1. 何よりもまず、デフォルトでプロキシがバックグラウンドで自動的に構築されるようになりました。自動プロキシ セットアップを有効または無効にするには、[Edit]メニュー > [Preferences] に移動し、[System]タブを選択します (図 1-a を参照)。[Manual] または [Automatic] から選択できます。 [Automatic] が選択されている場合、ムービーまたはイメージ シーケンス ストリップをシーケンサーに追加した後、またはストリップの表示設定を変更した後、いくつかの処理が行われます (図 1-b を参照)。

   .. 1. A small progress indicator with a percentage shows up in the status bar (see figure 1-c). Depending on your system and the resolution of the clip, this can take a while. You can continue working however, because the building process occurs in the background.
   .. 2. A directory BL_proxy is created as a subdirectory of the source folder of the strip (see figure 1-d). Within this directory a subdirectory is created with the name of the active strip; e.g. testfile_4K_10s_30fps.mp4 (figure 1-e). And within this folder, the proxy file is created; e.g. proxy_100.avi (figure 1-f), together with some other supplemental files. Note that the proxy files are quite larger in size (even for 25%) but also faster because they use a more optimized compression format that the original H.264 (MP4) codec.
   .. 3. Scrubbing through the strip should be much smoother now.
   1. パーセンテージ付きの小さな進行状況インジケータがステータス バーに表示されます (図 1-c を参照)。システムとクリップの解像度によっては、これには時間がかかる場合があります。ただし、構築プロセスはバックグラウンドで実行されるため、作業を続けることができます。
   2. ディレクトリ BL_proxy は、ストリップのソース フォルダのサブディレクトリとして作成されます (図 1-d を参照)。このディレクトリ内に、アクティブなストリップの名前でサブディレクトリが作成されます。たとえば、testfile_4K_10s_30fps.mp4 (図 1-e)です。そして、このフォルダー内にプロキシ ファイルが作成されます。たとえば、proxy_100.avi (図 1-f) とその他の補足ファイルです。プロキシ ファイルのサイズは (25% であっても) 非常に大きくなりますが、元の H.264 (MP4) コーデックよりも最適化された圧縮形式を使用するため、高速になることに注目してください。
   3. ストリップのスクラブがはるかにスムーズになるはずです。

.. todo::
   .. At the moment, proxies can only be generated for movie strips, not image sequences! In general, proxies are only used for video files, not audio.
   現時点では、プロキシはムービー ストリップに対してのみ生成でき、イメージ シーケンスに対しては生成できません。一般に、プロキシはビデオ ファイルにのみ使用され、オーディオには使用されません。

.. 2. The Proxy Render Size is set by default to 100%. You can change it in the View Settings (see figure 1-b) of the Preview window. If 100% is selected, the resolution of the Preview window is set to 100% of the strip resolution AND the original video clip (e.g. testfile_4K_10s_30fps.mp4) will be replaced by the proxy (e.g. proxy_100.avi). If you select afterwards another Proxy Render Size; e.g. 25%, a supplemental proxy will be created (proxy_25.avi) and there will be two proxy files (see figure 1-f) from which the second (25%) will be used for previewing.
2. [Proxy Render Size] はデフォルトで 100% に設定されています。これは、Preview ウィンドウ > Sidebar > [View]タブ の [View Settings] (図 1-b を参照) で変更できます。 100% を選択すると、Preview ウィンドウの解像度がストリップ解像度の 100% に設定され、元のビデオ クリップ (例: testfile_4K_10s_30fps.mp4) がプロキシ (例: proxy_100.avi) に置き換えられます。後で別のプロキシ レンダー サイズを選択した場合。たとえば 25% の場合、補助プロキシ (proxy_25.avi) が作成され、2 つのプロキシ ファイル (図 1-f を参照) が存在し、そのうちの 2 番目 (25%) がプレビューに使用されます。

   .. There are 6 Proxy Renders Sizes: No display, Scene size, 25%, 50%, 75%, 100%. Remember that these View settings are intended to set the resolution of the Preview window. For example, if the strip has a resolution of 1080p (1920 x 1080), then setting the Proxy Render Size to 25% means that the Preview window will have a resolution of 480 x  270. Displaying the strip in this low-resolution window will speed up the rendering a little. The setting No display, will set the resolution at zero (=no display!). The setting Scene size will set the resolution the same as the project (see figure 1-h), which can be different from the resolution of the strip.
   [Proxy Render Size] には、表示なし、シーン サイズ、25%、50%、75%、100% の 6 つがあります。これらのビュー設定は、Preview ウィンドウの解像度を設定することを目的としていることに注意してください。たとえば、ストリップの解像度が 1080p (1920 x 1080) の場合、プロキシ レンダー サイズを 25% に設定すると、Preview ウィンドウの解像度は 480 x 270 になります。この低解像度ウィンドウにストリップを表示すると、レンダリングを少し高速化します。 [No display] を設定すると、解像度がゼロに設定されます (= 表示なし!)。シーン サイズ設定は、プロジェクトと同じに解像度に設定されます (図 1-h を参照)。これはストリップの解像度とは異なる場合があります。

   .. note::
      .. You can easily see the effect of the Proxy Render Size in the following example. Create a new Video Editing project. The project resolution is probably 1080p (1920 x 1080). Add a text strip with size 30. Set the zoom to View > Fractional Zoom 1:1. Change the Proxy Render Size and watch the degradation of the image quality.
      次の例で、[Proxy Render Size] の効果を簡単に確認できます。新しいビデオ編集プロジェクトを作成します。プロジェクトの解像度はおそらく 1080p (1920 x 1080) です。サイズ 30 のテキスト ストリップを追加します。ズームを [View] > [Fractional Zoom 1:1] に設定します。プロキシ レンダリング サイズを変更し、画質の低下を確認します。

   .. figure:: /images/vse_setup_environment_proxies-render-size.svg
      :alt: Example of proxy Render Sizes

      図2: プロキシ レンダー サイズ 100%、50%、25% の品質への影響

   .. Reducing the display resolution will certainly reduce the time necessary to draw the display. On the other hand, the source file has a different resolution; so some additional scaling must be done. Perhaps, it confuses you that there exists a 100% proxy size. What's the use of this? If the display resolution is not changed, how will this help performance? Well, then comes the following default setting into action.
   ディスプレイの解像度を下げると、ディスプレイの描画に必要な時間が確実に短縮されます。一方、ソース ファイルの解像度は異なります。したがって、追加のスケーリングを行う必要があります。おそらく、100% のプロキシ サイズが存在することに混乱しているかもしれません。これは何の役に立つのですか？ディスプレイ解像度を変更しない場合、パフォーマンスはどのように向上しますか?さて、次のデフォルト設定が機能します。

.. 3. The checkbox ``Use proxies`` is enabled by default (see figure 1-b). It's a global setting, meaning that all strips in the project will use proxies. You can reverse this setting per strip (see later). So, if you select the Proxy Render Size of 25% in the View Settings, then the file proxy_25.avi is set as the strip source.
3. この ``Use proxies`` チェックボックスはデフォルトで有効になっています (図 1-b を参照)。これはグローバル設定であり、プロジェクト内のすべてのストリップがプロキシを使用することを意味します。この設定はストリップごとに反転できます (後述)。したがって、ビュー設定でプロキシ レンダー サイズ 25% を選択すると、ファイル proxy_25.avi がストリップ ソースとして設定されます。

.. A proxy file can differ in two ways from the source file.
プロキシ ファイルは、2つの点でソース ファイルと異なります。

.. * The resolution; e.g. 25% of the original resolution.
.. * The encoding; e.g. only intra-frame compression instead of intra- and inter-frame compression.
* 解像度: たとえば、元の解像度の 25%
* エンコーディング: たとえば、フレーム内およびフレーム間圧縮の代わりにフレーム内圧縮のみを実行します。


.. Some raw footage is heavily compressed to keep the storage requirements (e.g. smartphone) within reasonable limits. One compression technique that is used by the popular H2.64 codec is inter-frame compression. On an average video, content does not change abruptly from frame to frame. So, in stead of storing each frame fully, we can store only the changes from the previous frame. So, there are a few frames which contain the full image (i-frames) in a file, but most frames are delta-frames. This results in a huge reduction in storage but ... There is also a downside. In a typical editing task, you scrub and jump between frames. If most frames are delta-frames however, the software has to regenerate each time that frame by searching for the corresponding i-frame and adding all the subsequent changes. That takes time.
一部の生の映像は、ストレージ要件 (スマートフォンなど) を妥当な制限内に保つために大幅に圧縮されています。一般的な H2.64 コーデックで使用される圧縮技術の 1 つはフレーム間圧縮です。平均的なビデオでは、コンテンツがフレームごとに突然変化することはありません。したがって、各フレームを完全に保存する代わりに、前のフレームからの変更のみを保存できます。したがって、ファイル内には完全なイメージ (i フレーム) を含むフレームがいくつかありますが、ほとんどのフレームはデルタ フレームです。これにより、ストレージが大幅に削減されますが、欠点もあります。一般的な編集タスクでは、フレーム間をスクラブしたりジャンプしたりします。ただし、ほとんどのフレームがデルタ フレームの場合、ソフトウェアは、対応する i フレームを検索し、その後のすべての変更を追加することによって、フレームを再生成する必要があります。それには時間がかかります。

.. A proxy is a transcoded file in which no interframe compression is applied. So, scrubbing will be smoother; each frame has all information it needs to display and does not depend on others. So even if the resolution is the same as the source file (100%), the proxy will still be faster than the original. However, proxy files are on average much larger than the (inter-frame compressed) source files. In figure 1-d you can see that the original 4K source file is 525 Kib and the proxy_100.avi/proxy_25.avi are respectively 9.2 and 1.5 MiB. So, even the 25% proxy is approximately 3x larger than the original.
プロキシは、フレーム間圧縮が適用されないトランスコードされたファイルです。そのため、スクラブがよりスムーズになります。各フレームには表示する必要のあるすべての情報が含まれており、他のフレームには依存しません。したがって、解像度がソース ファイルと同じ (100%) であっても、プロキシの方が元のファイルよりも高速になります。ただし、プロキシ ファイルは平均して (フレーム間圧縮された) ソース ファイルよりもはるかに大きくなります。図 1-d では、元の 4K ソース ファイルが 525 Kib、proxy_100.avi/proxy_25.avi がそれぞれ 9.2 MiB と 1.5 MiB であることがわかります。したがって、25% のプロキシでも、元のプロキシよりも約 3 倍大きくなります。

.. Of course, much depends on the format of the source files. If your source files have already an optimized codec for editing (e.g. Apple’s ProRes, Avid’s DNxHD/HR and GoPro’s Cineform), creating proxy files isn't much of help.
もちろん、多くはソース ファイルの形式に依存します。ソース ファイルに編集用に最適化されたコーデック (Apple の ProRes、Avid の DNxHD/HR、GoPro の Cineform など) がすでにある場合、プロキシ ファイルの作成はあまり役に立ちません。

.. todo::
   .. Better explanation of inner working of proxies; link to external website/tutorial?
   プロキシの内部動作のより良い説明。外部の Web サイト/チュートリアルへのリンクはありますか?

.. 4. The above settings can be tweaked for individual strips with the Proxy Settings panel in the sidebar. To show the panel, select the strip in the Sequencer and press N or select the menu View > Sidebar.
4. 上記の設定は、 Sidebar > Proxy タブ > [Proxy Settings]パネルを使用して個々のストリップに対して微調整できます。パネルを表示するには、シーケンサーでストリップを選択して N を押すか、メニューの [View] > [Sidebar] を選択します。

   .. A. You have to decide if the proxies should be generated Per Strip or globally for the project. If you choose Per Strip, then the Proxy folder (BL_proxy) will be created at the location of the selected strip.  You can override this directory location and name in the panel below with the Custom Proxy Directory checkbox. Or, you can choose Project. The proxy folder BL_proxy will then be created in the directory from the field below. This setting influences also the Automatic setup. The chosen directory will be used for the automatic creation of the BL_proxy directory.

   A. プロキシをストリップごとに生成するか、プロジェクト全体に生成するかを決定する必要があります。 [Per Strip] を選択すると、選択したストリップの場所にプロキシ フォルダー (BL_proxy) が作成されます。このディレクトリの場所と名前は、下のパネルで [Custom Proxy Directory] チェックボックスを使用して上書きできます。または、プロジェクトを選択することもできます。プロキシ フォルダー BL_proxy が、以下のフィールドのディレクトリに作成されます。この設定は自動セットアップにも影響します。選択したディレクトリは、BL_proxy ディレクトリの自動作成に使用されます。

   .. note::
      .. In general, it is easier to manage, if you have a separate directory for all of your proxies of the same project. It's also advisable to have that folder on a different disk than the Blender program or source files (to minimize the disk access time).
      一般に、同じプロジェクトのすべてのプロキシに対して個別のディレクトリを作成すると、管理が容易になります。また、そのフォルダーを Blender プログラムやソース ファイルとは別のディスクに置くことをお勧めします (ディスク アクセス時間を最小限に抑えるため)。


   .. B. If you have opted for a Manual Proxy setup, you have to build the proxy files yourself. Select the strips (it can be more than one!) for which you want to create proxies. With the button ``Set Selected Strip Proxies`` you can enable multiple proxy render sizes (25%, 50%, 75%, 100%). With the Overwrite checkbox, you give permission to overwrite existing proxy-files. You'll use this button to enable these settings for *multiple* selected clips.

   B. 手動プロキシ設定を選択した場合は、プロキシ ファイルを自分で構築する必要があります。プロキシを作成するストリップを選択します (複数にすることもできます)。 ``Set Selected Strip Proxies`` ボタンを使用すると、複数のプロキシ レンダリング サイズ (25%、50%、75%、100%) を有効にすることができます。 [Overwrite] チェックボックスを使用すると、既存のプロキシ ファイルを上書きする許可を与えます。このボタンを使用して、選択した複数のクリップに対してこれらの設定を有効にします。

   .. C. The result of pushing the ``Set Selected Strip Proxies`` is that the checkbox next to ``Strip Proxy & Timecode`` is enabled and that the proxy sizes are filled in for all the selected strips. Eventually, you can deviate for the storage directory and filename of an individual strip here.
   C. ``Set Selected Strip Proxies`` を押した結果、 ``Strip Proxy & Timecode`` の隣のチェックボックスが有効になり、選択したすべてのストリップにプロキシ サイズが入力されます。最終的には、ここで個々のストリップの保存ディレクトリとファイル名を変更することができます。


   .. D. The proxy files however are not yet created. To generate them, you have to click the ``Rebuild Proxy and Timecode Indices``. By this time, you probably will appreciate the ease of the Automatic mode. The Build indicator (see figure 1-c) appears and the folders and files are created in the background. Unchecking the box ``Strip Proxy & Timecode`` will remove the advantage of smooth previewing but will not delete the proxy file on the hard disk.
   D. ただし、プロキシ ファイルはまだ作成されていません。それらを生成するには、 ``Rebuild Proxy and Timecode Indices`` をクリックする必要があります。この時点までに、おそらく自動モードの簡単さが分かるでしょう。ビルド インジケーター (図 1-c を参照) が表示され、フォルダーとファイルがバックグラウンドで作成されます。 ``Strip Proxy & Timecode`` チェックボックスをオフにすると、スムーズなプレビューの利点が失われますが、ハード ディスク上のプロキシ ファイルは削除されません。

   .. E. The Build JPEG Quality setting 0-100 corresponds to "Lowest Quality" to "Perceptually Lossless" in Blender's H.264 encoding presets.
   E. Build JPEG Quality 設定 0 ～ 100 は、Blender の H.264 エンコード プリセットの「Lowest Quality」から「Perceptually Lossless」に対応します。

   .. todo::
      .. Better explanation of Quality & Time Code; see `Timecode index <https://docs.blender.org/manual/en/dev/video_editing/sequencer/sidebar/proxy.html>`_ .
      品質とタイムコードの説明が改善されました。`Timecode index <https://docs.blender.org/manual/en/latest/editors/video_sequencer/sequencer/sidebar/proxy.html#strip-proxy-timecode>`_ を参照してください。

.. _proxies_cache:

Cache
-----
.. In order for this property to be visible, enable :ref:`Developer Extras <prefs-interface-dev-extras>`.
このプロパティを表示するには、`Developer Extras <https://docs.blender.org/manual/en/latest/editors/preferences/interface.html#prefs-interface-dev-extras>`_ を有効にします。

.. The biggest impact on playback performance is to allow the Video Sequencer to cache the playback. Because, it is so important, the cache system is designed to work silently in the background without much user interference. In fact, the Cache tab in the sidebar (see figure 3) will only be visible if the Developer Extras are switched on in the Edit > Preferences menu (Interface tab). In every case, the cache system will run silently for your benefit in the background.

再生パフォーマンスに最も大きな影響を与えるのは、ビデオ シーケンサーが再生をキャッシュできるようにすることです。これは非常に重要であるため、キャッシュ システムはユーザーの介入をあまり受けずにバックグラウンドで静かに動作するように設計されています。実際、 Sidebar > [Cache] タブ (図3) は、[Edit]メニュー > [Preferences] > [Interface] タブ で [Developer Extras] がオンになっている場合にのみ表示されます。どのような場合でも、キャッシュ システムはユーザーの利益のためにバックグラウンドでサイレントに実行されます。

.. There are two panels:
パネルは 2 つあります。

.. * Cache Settings: these settings apply to **all** strips in the Project
.. * Strip Cache: if enabled, these settings apply only to the **selected strip**; thus overriding the global settings.
* Cache Settings: これらの設定はプロジェクト内の **すべて** のストリップに適用されます
* Strip Cache: 有効にした場合、これらの設定は **選択したストリップ** にのみ適用されます。したがって、グローバル設定が上書きされます。


.. With the menu View > Show you can visualize the cache. They appear as small colored bars beneath the strips.
[View]メニュー > [Show Cache] を使用すると、キャッシュを視覚化できます。これらはストリップの下に小さな色のバーとして表示されます。

.. figure:: /images/vse_setup_environment_cache.svg
   :alt: Cache settings & bars

   図3: キャッシュ設定とキャッシュバー

.. todo::
   .. What do the following options really mean? Any supplemental info?
   次のオプションは実際には何を意味するのでしょうか?補足情報はありますか？
   (参照 `Cache — Blender Manual <https://docs.blender.org/manual/en/latest/editors/video_sequencer/sequencer/sidebar/cache.html>`_)

.. * Raw: Cache raw images read from drive, for faster tweaking of strip parameters at the cost of memory usage.
.. * Pre-processed: Cache preprocessed images, for faster tweaking of effects at the cost of memory usage.
.. * Composite: Cache intermediate composited images, for faster tweaking of stacked strips at the cost of memory usage.
.. * Final: Cache final image for each frame.

* Raw: ドライブから読み取られた RAW イメージをキャッシュし、メモリ使用量を犠牲にしてストリップ パラメータをより速く調整します。
* Pre-processed: 前処理された画像をキャッシュし、メモリ使用量を犠牲にして効果をより速く調整します。
* Composite: 中間の合成イメージをキャッシュし、メモリ使用量を犠牲にしてスタックされたストリップをより高速に調整します。
* Final: 各フレームの最終画像をキャッシュします。

.. There are two levels of cache, the first is a RAM cache, this is enabled by default but can be increased based on the amount of RAM available. The next level of cache is a disk cache which stores cached strips on disk. A disk cache can generally cache more than a RAM cache, but it can be slower. Both of these cache options can be configured in the Edit > Preferences menu under the System tab.(see figure 1-a).

キャッシュには 2 つのレベルがあり、1 つ目は RAM キャッシュです。これはデフォルトで有効になっていますが、利用可能な RAM の量に基づいて増やすことができます。キャッシュの次のレベルは、キャッシュされたストリップをディスクに保存するディスク キャッシュです。ディスク キャッシュは通常、RAM キャッシュよりも多くのキャッシュをキャッシュできますが、速度が低下する可能性があります。これらのキャッシュ オプションはどちらも、[Edit]メニュー > [Preferences] > [System]タブで設定できます (図 1-a)。


.. todo::
   .. Summarizing difference between cache, e.g. disk cache and proxies
   ディスクキャッシュとプロキシなどのキャッシュの違いの概要

.. * Proxies only work with movie strips; cache supports all strip types.
.. * Proxies store result on hard disk; cache store result in RAM (except diskcache)
.. * Proxies cache only the RAW datafile; cache can store intermediate results
.. * Proxies are persistent, cache becomes eventually invalidated
* プロキシはムービー ストリップでのみ機能します。キャッシュはすべてのストリップ タイプをサポートします。
* プロキシは結果をハードディスクに保存します。キャッシュは結果を RAM に保存 (ディスクキャッシュを除く)
* プロキシは RAW データファイルのみをキャッシュします。キャッシュは中間結果を保存できます
* プロキシは永続的で、キャッシュは最終的に無効になります


.. toctree::

   proxies_technical
