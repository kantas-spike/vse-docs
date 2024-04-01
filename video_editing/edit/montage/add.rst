Add
---

.. After :doc:`setting up your project </video_editing/setup/index>`, you should haven an organized directory with all your footage. The first step in Montage is to *import* this footage and to *add* some supporting strips (text, color, ...).

:doc:`setting up your project </video_editing/setup/index>` した後、すべての映像を含む整理されたディレクトリが作成されるはずです。 *Montage* の最初のステップは、これらの footage (ムービーの場面、一部)を *import* し、サポート ストリップ (テキスト、カラーなど)を *Add* することです。

Import
......

.. note::

   .. Blender is - as all video editors nowadays - a non-linear editing (NLE) system. According to `wikipedia <https://en.wikipedia.org/wiki/Non-linear_editing>`_ non-linear editing is a form of offline editing for audio, video, and image editing, where the *original content is not modified in the course of editing*.

   Blender は、最近のすべてのビデオ編集者と同様に、ノンリニア編集 (NLE) システムです。 `wikipedia <https://en.wikipedia.org/wiki/Non-linear_editing>`_ によると、ノンリニア編集は、編集中に元のコンテンツが変更されない、オーディオ、ビデオ、および画像編集のためのオフライン編集の形式です。

.. There are three methods available to import footage with subtle but sometimes annoying differences between them.
.. `Mikeycal Meyers <https://www.youtube.com/watch?v=zslAZxC29rk>`_ demonstrated them in a short video tutorial.

映像をインポートするには 3 つの方法がありますが、それらの間には微妙ではあるものの、場合によっては煩わしい違いがあります。 `Mikeycal Meyers <https://www.youtube.com/watch?v=zslAZxC29rk>`_ は、短いビデオ チュートリアルでそれらをデモンストレーションしました。

..
  1. Add a strip with the shortcut key (:kbd:`Shift - A` ) or the Add menu to the Sequencer timeline and locate the desired file with a modified Blender File Browser version.
  2. Drag a video, sound, or image/image sequence on the timeline with the `Blender File Browser <https://docs.blender.org/manual/en/dev/editors/file_browser.html>`_. The Blender File Browser is the top-left window in the Video Editing workspace (see figure 1).
  3. Drag and drop the desired video, sound, or image file on the sequencer timeline from the File Browser of the operating system.
..

1. `Blender File Browser <https://docs.blender.org/manual/en/dev/editors/file_browser.html>`_ を使用して、ビデオ、サウンド、または画像/画像シーケンスをタイムライン上にドラッグします。 Blender ファイル ブラウザは、ビデオ編集ワークスペースの左上のウィンドウです (図 1)。
2. ショートカット キー (:kbd:`Shift-A`) または [Add] メニューにより、ストリップを Blender File View を使って Sequencer のタイムラインに追加し、 目的のファイルを配置します。
3. オペレーティング システムのファイル ブラウザから、シーケンサーのタイムライン上に目的のビデオ、サウンド、または画像ファイルをドラッグ アンド ドロップします。

.. figure:: /images/vse_setup_project_methods.gif
   :alt: Import methods

   図 1: 3 つのインポート方法


.. - Only with the Add (2nd) method can you add all of the :doc:`available strip types </video_editing/edit/montage/striptypes/index>`. The other methods only allow adding Movie, Sound, or Image/Image Sequence strips.
.. - Also, only the Add method offers the Import options (Scale To Fit, ...). A discussion of these options is in the next section.
.. - And also, only the Add method can import multiple files. Although you can select multiple files (as well in the Blender File Browser as in the OS File Browser), only one file (the first selected) is dropped on the timeline.   Probably, for the same reason, it is not possible to add an Image Sequence.
- 2番目の Add 方法を使用した場合のみ、利用可能なすべてのストリップ タイプを追加できます。他の方法では、ムービー、サウンド、またはイメージ/イメージ シーケンス ストリップの追加のみが可能です。
- また、Add による方法のみがインポート オプション ([Scale To Fit] など) を提供します。これらのオプションについては、次のセクションで説明します。
- また、複数のファイルをインポートできるのは Add メソッドのみです。複数のファイルを選択できますが (OS ファイル ブラウザと同様に Blender ファイル ブラウザでも)、タイムラインにドロップされるのは 1 つのファイル (最初に選択したファイル) だけです。おそらく同じ理由で、イメージ シーケンスを追加することはできません。

.. Warning::
   .. All three methods are rather limited, compared to some other video editors.
   3 つの方法はすべて、他のビデオエディターと比べるとかなり制限されています。

  .. - Using the Add method with multiple clips will place them one after the other on the timeline, starting at the position of the playhead. If you want them stacked however, you have to add the clips one by one.
  .. - When there are already strips at the position of the playhead, Blender will add the strips at the first free channel. You cannot choose the channel, you want the clips to be added.
  .. - The location where you drop the strip is not important. Blender will insert them at the position of the playhead. If, however, you try to drop the strip upon another strip or between strips (hoping that it will insert the strip), nothing will happen. The strip isn't even added.
  .. - There are  128 channels available for inserting strips, although you can scroll to higher-numbered channels. So, in principle, you cannot add more than 128 strips at the same time position. You can however work around this limitation by using meta strips. Select a few strips and right click. Choose "Make meta strip". Shortcut :kbd:`Ctrl G`. The selected strips collapse into one channel and count also as 1 channel.
  .. - It is not possible to import strips before or between other strips. You can do that however within the sequencer.
  .. - For the File Browser Drag method, you need to drag the icon of the file. Trying to drag the name will only invoke a select operation.
  - 複数のクリップで Add メソッドを使用すると、再生ヘッドの位置から開始してタイムライン上にクリップが順番に配置されます。ただし、クリップを積み重ねたい場合は、クリップを 1 つずつ追加する必要があります。
  - Playhead の位置にすでにストリップがある場合、Blender は最初の空きチャンネルにストリップを追加します。追加するクリップのチャンネルを選択することはできません。
  - ストリップをドロップする場所は重要ではありません。 Blender はそれらをPlayheadの位置に挿入します。ただし、(ストリップが挿入されることを期待して) 別のストリップの上またはストリップの間にストリップをドロップしようとしても、何も起こりません。ストリップも追加されていません。 [#f1]_
  - ストリップの挿入に使用できるチャンネルは 128 です。 より大きな番号のチャンネルにはスクロールで表示することができあす。したがって、原則として、同時に 128 を超えるストリップを追加することはできません。ただし、メタ ストリップを使用することで、この制限を回避できます。いくつかのストリップを選択して右クリックします。 [Make meta strip] を選択します。ショートカット :kbd:`Ctrl-G` 。選択したストリップは 1 つのチャンネルに折りたたまれ、1 チャンネルとしてカウントされます。
  - 他のストリップの前または間にストリップをインポートすることはできません。ただし、シーケンサー内でそれを行うこともできます。 [#f2]_
  - ファイル ブラウザのドラッグ方法の場合は、ファイルのアイコンをドラッグする必要があります。名前をドラッグしようとすると、選択操作のみが呼び出されます。 [#f3]_

.. Some of these limitations are tackled by addons. For example, the `VSE Quick Functions addon <https://github.com/snuq/VSEQF>`_  has the following import additions:

これらの制限の一部はアドオンによって解決されます。たとえば、`VSE Quick Functions addon <https://github.com/snuq/VSEQF>`_ に は次のインポート機能が追加されています。 [#f4]_

.. - Import At Frame: standard import behavior, places new sequences at the playhead.
.. - Insert At Frame: the following sequence will be moved forward by the length of the imported sequence.
.. - Cut And Insert At Frame: all sequences at the current frame will be cut and all following sequences will be moved forward by the length of the imported sequence.
.. - Import At End: places the imported sequences at the end of the timeline.
- Import At Frame: 標準のインポート動作で、新しいシーケンスを再生ヘッドに配置します。
- Insert At Frame: 次のシーケンスは、インポートされたシーケンスの長さだけ前方に移動されます。
- Cut And Insert At Frame: 現在のフレームのすべてのシーケンスがカットされ、後続のすべてのシーケンスがインポートされたシーケンスの長さだけ前に移動されます。
- Import At End: インポートされたシーケンスをタイムラインの最後に配置します。


.. There is also a working but experimental version of the Three Point Edit method. With this method, you can load a source clip in a separate preview window (e.g. the Movie Clip Editor),
.. scrub in this clip and set the In (Start) and Out (Finish) points and import this part of the source clip into the timeline with various options (import at frame, insert at frame, ..., see above).

3点編集方法の実用的ではあるが実験的なバージョンもあります。この方法を使用すると、
ソースクリップを別のプレビューウィンドウ(例えば Movie Clip Editor)にロードでき、
このクリップ内でスクラブし、イン (開始) ポイントとアウト (終了) ポイントを設定できます。
そして、ソースクリップの一部を、様々なオプション(上述の import at frame, insert at frame, ...)を使って、タイムラインにインポートできます。


Options
,,,,,,,

.. figure:: /images/vse_setup_project_options-moviestrip.png
   :alt: Import options Movie strip
   :scale: 70%
   :align: right

   図2 Movieストリップのインポート オプション

.. There are only import options for :doc:`strip types of group 2 </video_editing/edit/montage/striptypes/index>`:
.. Movie, Sound, and Image/Image Sequence because they have an external source.
インポート オプションは 外部ソース(ムービー、サウンド、イメージ/イメージ シーケンス)を持つ :doc:`strip types of group 2 </video_editing/edit/montage/striptypes/index>` 用です。

Relative Path
    ..
     The location of the video file is stored and available in the :ref:`Source panel <source-panel>`.
     This location can be relative - starting from the location of the Blend-file
     where the asset is imported - or absolute - starting from the root directory of the computer -
     (see `Blender manual <https://docs.blender.org/manual/en/dev/files/blend/open_save.html#relative-paths>`_ ).
     The Blend-file is of course already saved and the external file could not be on a different drive.
    ..
    ビデオ ファイルの場所は保存され、:ref:`Source panel <source-panel>` で利用できます。
    この場所は、アセットがインポートされる blend ファイルの場所から始まる相対的な場所、またはコンピューターのルート ディレクトリから始まる絶対的な場所にすることができます ( `Blender manual <https://docs.blender.org/manual/en/dev/files/blend/open_save.html#relative-paths>`_ を参照)。
    もちろん、blend ファイルはすでに保存されており、外部ファイルを別のドライブに置くことはできません。??


Start Frame
    ..
     As the name implies, the Start frame of the movie.
     This field is automatically filled in with the position of the playhead;
     e.g. with the value zero if the playhead is at position 0, or 15 if the playhead is at position 15.
    ..
    名前が示すように、ムービーの開始フレーム。このフィールドには、再生ヘッドの位置が自動的に入力されます。たとえば、再生ヘッドが位置 0 にある場合は値 0、再生ヘッドが位置 15 にある場合は値 15 です。

Channel
    ..
     The Channel to place the strip. The filled-in channel is always one,
     even if there is already a strip at that position.
     The newly added strip however will be placed at the next lower or higher free channel.
     The maximum number of channels is 32, even though you can see more channels.
    ..
    ストリップを配置するチャンネル。たとえその位置にすでにストリップがあったとしても、塗りつぶされたチャンネルは常に 1 つです。ただし、新しく追加されたストリップは、次に低い、または高い空きチャンネルに配置されます。より多くのチャンネルを表示できる場合でも、チャンネルの最大数は 128 です。

Replace Selection
     .. Replaces the currently selected strips with the new strip.
     現在選択されているストリップを新しいストリップに置き換えます。

.. todo::
     .. The Replace Selection option does not seem to do anything.
     [選択範囲を置換] オプションは何も行わないようです。

Set View Transform
   ..
    When enabled (default), this option sets the View Transform to Standard on the first import of a Movie clip.
    You can find the View Transform property in the Properties Editor > Render Properties > Color Management panel.
    Most video files are encoded in the sRGB (=standard) color space.
    Color values can fluctuate between 0 and 1. In the 3D modeling world,
    however, color values can fluctuate between 0 and infinity, depending on the amount of light you add to a scene.
    Therefore, a different View Transform algorithm (e.g. Filmic) is used.
    For example, if you start your project within the Modeling workspace,
    the View Transform option is set by default to Filmic.
    A mismatch of this View Transform setting can cause huge delays in render time and distortions of colors.
   ..
   このオプションを有効にすると (デフォルト)、ムービー クリップの最初のインポート時に[View Transform]が標準に設定されます。
   [View Transform] プロパティは、 [Properties Editor] > [Rnedering Properties] > [Color Management] パネルあります。
   ほとんどのビデオ ファイルは sRGB (=標準) 色空間でエンコードされます。カラー値は 0 から 1 の間で変動することがあります。ただし、3D モデリングの世界では、シーンに追加する光の量に応じて、カラー値は 0 から無限大まで変動する可能性があります。
   したがって、別の [View Transform] アルゴリズム (Filmic など) が使用されます。
   たとえば、モデリング ワークスペース内でプロジェクトを開始した場合、[View Transform]オプションはデフォルトで Filmic に設定されます。この[View Transfrom]設定が一致しないと、レンダリング時間の大幅な遅延や色の歪みが発生する可能性があります。

Fit Method
  ..
    The dimensions of the scene/project do not always fit the dimensions of the movie or image that you want to import.
    For example; you want to import an image of 500 (w) x 500 (h) into a scene of 640 (w) x 360 (h).
    It's obvious that the height of the image (500) will not fit into the height of the scene (360).
    The Fit method determines how images are scaled to fit inside the render area.
    This is done by changing the Transform Scale X and Y properties of the imported image.
  ..

  シーン/プロジェクトのサイズは、インポートするムービーまたは画像のサイズと必ずしも一致するとは限りません。
  例えば; 500 (w) x 500 (h) のイメージを 640 (w) x 360 (h) のシーンにインポートしたいとします。画像の高さ (500) がシーンの高さ (360) に適合しないことは明らかです。 [Fit Method]は、レンダリング領域内に収まるようにイメージをどのようにスケールするかを決定します。これを行うには、インポートされたイメージの Transform Scale X および Y プロパティを変更します。

    Scale to Fit
        ..
          The visual content of the strip fits exactly within the
          project’s Dimensions while maintaining the original aspect ratio.
          This means that -  from the above example (see also figure 3) - that the height of image (500)
          should be scaled to fit exactly in the height of the scene (360) with a factor of 0.72 (360/500).
          Because this method wants to maintain the original aspect ratio of the image,
          also the width should be scaled by 0.72, creating transparent vertical bands.
        ..
        ストリップのビジュアル コンテンツは、元のアスペクト比を維持しながら、プロジェクトのサイズ内に正確に収まります。
        これは、上記の例 (図 3 も参照) から、画像の高さ (500) がシーンの高さ (360) に正確に収まるように、係数 0.72 (360/500) でスケーリングする必要があることを意味します。この方法では画像の元のアスペクト比を維持する必要があるため、幅も 0.72 で拡大縮小し、透明な垂直バンドを作成する必要があります。

    Scale to Fill
        ..
          The visual content of the strip spans the project’s Dimensions while maintaining the original aspect ratio.
          In our example: the largest dimension of the scene (640) should be filled with the image (500).
          So the image should be enlarged in the X axis with a factor of 1.28 (= 640 /500).

          This may mean that portions of the original image no longer fit the content inside the rendered area.
        ..
        ストリップのビジュアル コンテンツは、元のアスペクト比を維持しながら、プロジェクトのディメンションにまたがります。この例では、シーンの最大寸法 (640) が画像 (500) で満たされる必要があります。したがって、画像は 1.28 (= 640 /500) の係数で X 軸に拡大される必要があります。

        これは、元のイメージの一部がレンダリング領域内のコンテンツに適合しなくなったことを意味する可能性があります。

    Stretch to Fill
        ..
          The visual content of the strip fills the project’s Dimensions.
          Note that, unlike the other two methods, Stretch to Fill does not maintain the original aspect ratio.

          This could result in a distortion of the original image (see figure 3).
        ..
        ストリップのビジュアル コンテンツはプロジェクトのディメンションを埋めます。
        他の 2 つの方法とは異なり、Stretch to Fill は元のアスペクト比を維持しないことに注意してください。

        これにより、元の画像が歪む可能性があります (図 3 を参照)。

    .. figure:: /images/vse_setup_project_scale-methods.svg
       :alt: Import methods

       図3 3 つのフィット方法

Sound
    ..
      If the video file contains an embedded audio channel,
      enabling this option will add a Sound Strip to the that contains the movie’s audio track.
      Disabling the option will only add a movie strip without the audio.
    ..
    ビデオ ファイルに埋め込みオーディオ チャネルが含まれている場合、このオプションを有効にすると、
    ムービーのオーディオ トラックを含むサウンド ストリップが追加されます。このオプションを無効にすると、音声のないムービー ストリップのみが追加されます。

Use Movie Frame Rate
    ..
      This option sets the Scene Frame Rate of the Scene to the frame rate encoded in the added movie file.
      A mismatch of the project and strip frame rate is often the cause of
      :doc:`synchronizing problems </video_editing/edit/montage/striptypes/movie>` with the audio.
      When a new Blend-file is created, the framerate is by default set to 24 fps.
      Unless this option is enabled, adding a movie with a framerate of 30 fps, will result in this kind of problems.
    ..
    このオプションは、シーンのシーン フレーム レートを、追加されたムービー ファイルにエンコードされたフレーム レートに設定します。プロジェクトとストリップのフレーム レートの不一致が、 オーディオとの :doc:`synchronizing problems </video_editing/edit/montage/striptypes/movie>` となることがよくあります。新しい Blend ファイルが作成されると、フレームレートはデフォルトで 24 fps に設定されます。このオプションが有効になっていない場合、フレームレート 30 fps のムービーを追加すると、この種の問題が発生します。

..
  The Image/Image Sequence strip has no ``Sound`` or ``Use Movie Frame Rate`` option
  (because they don't make any sense in this context). The ``Use Placeholders`` option is added.
  The Sound strip has in addition no ``Fit method`` option. The options ``Cache`` and ``Mono`` however are added.
  These options are already described in the properties list of the
  :doc:`Image Sequence strip <striptypes/image>` and :doc:`Sound strip <striptypes/sound>`.
..
Image/Image Sequence ストリップには、[Sound] や [Movie Frame Rate] オプションはありません。 (この文脈では意味をなさないため)。
[Use Placeholders] オプションが追加されます。さらに、サウンド ストリップには [Fit method] オプションがありません。
ただし、[Cache]と[Mono]オプションが追加されます。これらのオプションは、:doc:`Image Sequence strip <striptypes/image>` と :doc:`Sound strip <striptypes/sound>` のプロパティ リストですでに説明されています 。


.. Organize timeline
タイムラインを整理する
,,,,,,,,,,,,,,,,,

..
  Working with a long and complex timeline isn't easy.
  Some kind of organization is needed in order to work as efficiently as possible.
  The adagio "Leave your timeline in a state that someone else could pick it up" certainly applies.
  Although organizing your timeline is probably a highly individual approach,
  the following tips may offer some help.
..

長く複雑なタイムラインを扱うのは簡単ではありません。可能な限り効率的に作業するには、何らかの組織が必要です。
「タイムラインを他の人が拾える状態にしておくこと」というアダージョは確かに当てはまります。タイムラインの整理はおそらく非常に個人的なアプローチですが、次のヒントが役立つかもしれません。

..
  - Blender VSE lets you place whatever strip on whatever channel.
    Many editors however group their channels into functional bands: e.g.
    channel 1-5: audio, 5-10: video, 11-15: effects.
    Within each band there can be sub-bands such as background music, voice-over, ambient sounds, ...
    Take a look at :doc:`Organize your assets </video_editing/setup/directory-structure>` for a possible categorization.
  - Some video editing programs link the video and embedded audio strip.
    The advantage of course is that moving one strip will move the other.
    Synchronization issues will less likely appear. In Blender VSE, the video and audio are not linked.
    A work-around is to use meta strips but this has the disadvantage that you cannot see the Sound wave.
    The VSQEF addon lets you parent strips: see `video tutorial <https://www.youtube.com/watch?v=rJg8xH8PyGc&t=40s>`_.
  - Blender's VSE doesn't use the concept of a "bin": a virtual folder
    that lives only inside the project to hold references to source clips.
    But, it can easily be emulated by using multiple scenes.
    In figure 4, two scenes (Raw footage and Rough cut) are created (slide 1).
    All clips are added to the timeline of the Raw Footage scene.
    The Display Mode of the Outliner (top right window) is set to ``Scenes`` (slide 2).
    You can switch very easily between the timelines of both scenes by just selecting the scene in the Outliner (slide 3).
..
-  Blender VSE では、任意のストリップを任意のチャンネルに配置できます。ただし、多くの編集者は、チャネルを機能バンドにグループ化します。たとえば、以下のようにグループ化します。
  - チャネル 1 ～ 5: オーディオ
  - チャネル 5 ～ 10: ビデオ
  - チャネル 11 ～ 15: エフェクト
  各バンド内には、バックグラウンド ミュージック、ナレーション、アンビエント サウンドのようなサブバンドを含めることができます。可能な分類については、 :doc:`Organize your assets </video_editing/setup/directory-structure>` を参照してください。

-  一部のビデオ編集プログラムは、ビデオと埋め込みオーディオ ストリップをリンクします。もちろん利点は、一方のストリップを移動すると他方のストリップも移動することです。同期の問題が発生する可能性は低くなります。 Blender VSE では、ビデオとオーディオはリンクされていません。回避策はメタ ストリップを使用することですが、これには音波が見えなくなるという欠点があります。 VSQEF アドオンを使用すると、ストリップを親にすることができます。 `video tutorial <https://www.youtube.com/watch?v=rJg8xH8PyGc&t=40s>`_ を参照してください。
-  Blender の VSE は、 "bin" という概念を使用しません。これは、ソース クリップへの参照を保持するためにプロジェクト内にのみ存在する仮想フォルダーです。ただし、複数のシーンを使用することで簡単にエミュレートできます。図 4 では、2 つのシーン (Raw フッテージとラフ カット) が作成されています (スライド 1)。すべてのクリップが Raw Footage シーンのタイムラインに追加されます。アウトライナー (右上のウィンドウ) の表示モードはScenes(スライド 2) に設定されます。アウトライナーでシーンを選択するだけで、両方のシーンのタイムラインを簡単に切り替えることができます (スライド 3)。

.. raw:: html

    <object data="/_static/images/bins.svg" type="image/svg+xml"></object>

図4 "bin"" を作成するには?画像をクリックするか、キーボードの矢印を使用して次のスライドを表示します。

.. When doing fiction, you could organize your footage in:
フィクションを制作する場合、次のように映像を整理できます。

..
   - Sequence: a series of scenes. S. Kubrick always told his stories in 8 sequences.
   - Scene: a situation that plays out in one location in continuity.
   - Shot: a camera set up to cover the entire scene or a part of it.
   - Take: a recorded attempt out of many to get the shot right.
..

- Sequence: 一連のシーン。 S・キューブリックは常に8つのシーケンスで自分の物語を語った。
- Scene: 1 つの場所で継続的に展開される状況。
- Shot: シーン全体またはその一部をカバーするように設定されたカメラ。
- Take: ショットを正しく撮るための多くの試みの中から記録されたもの。

Add
,,,

.. With the shortcut key :kbd:`Shift - A` you can add strips without any external source (text, color, ...); see :doc:`Strip types <striptypes/index>` for an in-depth overview of all available types.

ショートカット キー :kbd:`Shift-A` を使用すると、外部ソースなしでストリップ(テキスト、カラーなど) を追加できます。利用可能なすべてのタイプの詳細な概要については、 :doc:`Strip types <striptypes/index>` を参照してください。

.. The placement of these strips obey the same rules as with importing strips.
これらのストリップの配置は、ストリップのインポートと同じルールに従います。

.. rubric:: 訳注

.. [#f1] Blender4.0では、1つ目の方法では、素材を任意の位置にドラッグ&ドロップできます(snapも利用可能。3つ目の方法でも、任意の位置にドラッグ&ドロップできますが、snapは利用できず、1の方法と比較すると、どの位置に追加できるか判断が難しいです。
.. [#f2] Blender4.0では、可能なようです。
.. [#f3] Blender4.0では、 アイコンおよびファイル名をドラッグ可能です。
.. [#f4] このアドオンも何年もメンテナンスされていません。
