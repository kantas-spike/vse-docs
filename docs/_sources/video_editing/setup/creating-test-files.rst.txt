
.. Creating test files
テストファイルの作成
-------------------

.. Sometimes you need a test video or test image with a specific resolution, duration or framerate and specific content, e.g. gradient color, TV test image, counter or time code. Here are some useful commands and programs to create test videos and images.

場合によっては、特定の解像度、期間、またはフレームレート、および特定のコンテンツを持つ、テストビデオまたはテスト画像が必要な時があります。

例えば、グラデーション カラー、TV テスト画像、カウンターまたはタイムコードなど

ここでは、テストビデオや画像を作成するための便利なコマンドとプログラムをいくつか紹介します。


.. **A. Generate test video with ffmpeg**
**A. ffmpeg でテストビデオを生成する**

..
 FFMPEG is a command line tool for handling (decode, encode, convert, ...) video and audio files.
 It is used by many commercial and free software products, including Blender.
 The core is the FFMPEG program, together with a video & audio player
 (FFPLAY) and a stream analyzer (FFPROBE).
..

FFMPEG は、ビデオ ファイルとオーディオ ファイルを処理 (デコード、エンコード、変換など) するためのコマンド ライン ツールです。
これは、Blender を含む多くの商用および無料ソフトウェア製品で使用されています。
ツールのコアは FFMPEG プログラムと、ビデオ & オーディオ プレーヤー (FFPLAY) およびストリーム アナライザー (FFPROBE) です。

..
  You can create a test video with the virtual input device *lavfi*.
  Because it's a virtual device, you need to specify the force (-f) option.
..

仮想入力デバイス *lavfi* を使用してテスト ビデオを作成できます。仮想デバイスであるため、強制 (-f) オプションを指定する必要があります。

..
  The video source can be chosen from a variety of options;
  see `ffmpeg documentation <http://ffmpeg.org/ffmpeg-filters.html#Video-Sources>`_ under section 14.9:
  *allrgb, allyuv, color, haldclutsrc, nullsrc, pal75bars, pal100bars, rgbtestsrc, smptebars,
  smptehdbars, testsrc, testsrc2, yuvtestsrc*.
..

ビデオ ソースはさまざまなオプションから選択できます。
`ffmpeg documentation <http://ffmpeg.org/ffmpeg-filters.html#Video-Sources>`_ のセクション 14.9 以降を参照してください:
*allrgb、allyuv、color、haldclutsrc、nullsrc、pal75bars、pal100bars、rgbtestsrc、smptebars、smptehdbars、testsrc、testsrc2、yuvtestsrc*


..
  With *testsrc* for example you can generate a test video pattern,
  showing a color pattern, a scrolling gradient and a timestamp.
..
たとえば、 *testsrc* を使用すると、カラー パターン、スクロール グラデーション、タイムスタンプを表示するテスト ビデオ パターンを生成できます。

.. You can first try out the command with *ffplay* to preview the output.

まずは、 *ffplay* でコマンドを試して、出力をプレビューできます。

.. code-block::

   ffplay -f lavfi -i testsrc=duration=10:size=1280x720:rate=30

.. raw:: html

    <video width="640" height="480" src="https://www.bogotobogo.com/FFMpeg/images/test_patterns/testsrc.mp4" controls></video>

図1: FFMPEG コマンドからの出力 (上記を参照)

..
  If you are satisfied with the result,
  replace the *ffplay* command with *ffmpeg* and add the output file; eg test.mp4
..
結果に満足したら、ffplayコマンドを *ffmpeg* に置き換えて出力ファイルを追加します。例: test.mp4

.. code-block::

   ffmpeg -f lavfi -i testsrc=duration=10:size=1280x720:rate=30 test.mp4

..
  More commands and test formats can be found at
  `bogotobogo <https://www.bogotobogo.com/FFMpeg/ffmpeg_video_test_patterns_src.php>`_.
..
その他のコマンドとテスト形式については、 `bogotobogo <https://www.bogotobogo.com/FFMpeg/ffmpeg_video_test_patterns_src.php>`_ を参照してください。

.. **B. Generate a timecode overlay with FFMPEG**
**B. FFMPEG を使用してタイムコード オーバーレイを生成する**

.. Did you ever needed a video with the timecode embedded?

タイムコードが埋め込まれたビデオが必要になったことはありますか?

.. code-block::

    ffplay -i test.mp4 -vf "drawtext=text='timestamp: %{pts \: hms}': x=500: y=500: fontsize=32:fontcolor=yellow@0.9: box=1: boxcolor=black@0.6"

..
  This command will invoke the ffmpeg video player (ffplay).
  The input video is test.mp4. With the drawtext video filter,
  the timestamp is overlaid on the input video. The time format is specified with the pts parameter.
..

このコマンドは、ffmpeg ビデオ プレーヤー (ffplay) を呼び出します。入力ビデオは test.mp4 です。drawtext ビデオ フィルターを使用すると、タイムスタンプが入力ビデオにオーバーレイされます。時刻形式は pts パラメータで指定します。

.. Replace the *ffplay*command with *ffmpeg* and add a output file to create a new video.

*ffplay* コマンドを *ffmpeg* に置き換え、出力ファイルを追加して新しいビデオを作成します。

..
  A more extensive introduction to the `drawtext` filter and the above mentioned ffmpeg command is given by
  `Krishna Rao <https://ottverse.com/ffmpeg-drawtext-filter-dynamic-overlays-timecode-scrolling-text-credits/>`_.
..

`drawtext` フィルタと上記の ffmpeg コマンド のより広範な紹介は、 `Krishna Rao <https://ottverse.com/ffmpeg-drawtext-filter-dynamic-overlays-timecode-scrolling-text-credits/>`_ によって提供されています。

.. **C. Generate a timecode overlay with Blender Python**
**C. Blender Python を使用してタイムコード オーバーレイを生成する**

..
  The ffmpeg command above does the job but is not very flexible.
  With the following `Python script of Tin2Tin <https://gist.github.com/tin2tin/1eabb233bce24e78d2edf35cb5a435c8>`_,
  you can generate a timecode overlay very easily in Blender.
..

上記の ffmpeg コマンドは機能しますが、柔軟性はあまりありません。
次の `Python script of Tin2Tin <https://gist.github.com/tin2tin/1eabb233bce24e78d2edf35cb5a435c8>`_ を使用すると、Blender でタイムコード オーバーレイを非常に簡単に生成できます。

.. figure:: /images/vse_setup_project_test-files.png
   :align: center
   :alt: Test file from Python scriptExample of a complex timeline

   図2: Python スクリプトから生成されたテストファイル

.. To create the time code overlay, follow the next steps.
タイムコード オーバーレイを作成するには、次の手順に従います。

.. 1. Open Blender, set the render parameters (resolution, frame rate, start and frame).
   The length of the created time code overlay is determined by the Start and End field in the Render panel.
.. 2. Switch to the scripting workspace, create a new text file and copy the downloaded code into the script editor.
.. 3. Run the code with the menu Text > Run Script or Alt + P.
.. 4. If you need this overlay for an existing video, you'll have to render it out.
1. Blender を開き、Render パラメーター (resolution, frame rate, start and frame) を設定します。作成されるタイムコード オーバーレイの長さは、[Render]パネルの[Start]フィールドと[End]フィールドによって決まります。
2. Scripting Workspace に切り替え、新しいテキスト ファイルを作成し、ダウンロードしたコードをスクリプト エディターにコピーします。
3. [Text]メニュー > [Run Script] または :kbd:`Alt+P` を使用してコードを実行します。
4. 既存のビデオにこのオーバーレイが必要な場合は、それをレンダリングする必要があります。

.. If you want to customize the script, the time code text is assembled at line 53:
スクリプトをカスタマイズする場合は、タイムコード テキストが 53 行目で組み立てられます。

.. code-block::

    text_strip.text = str(bpy.utils.smpte_from_frame(i))

..
  The variable *i* stands for the frame number (*Start <= i <= End*).
  This value is converted to a time code with the `smpte_from_frame` function.
  This function creates a text from the frame number with the format of HH:MM:SS:FF
  and follows hereby the standard of the Society of Motion Picture and Television Engineers (SMPTE).
  The text is positioned at 0.8 on the Y-axis (near the top of the window).
..

変数 *i* はフレーム番号を表します (*Start <= i <= End*)。この値は `smpte_from_frame` 関数でタイムコードに変換されます。
この関数は、HH:MM:SS:FF の形式でフレーム番号からテキストを作成し、Society of Motion Picture and Television Engineers (SMPTE) の標準に従います。
テキストは Y 軸の 0.8 の位置 (ウィンドウの上部近く) に配置されます。

..
  The magic of the script occurs between lines 37 - 60,
  which is essentially a loop of the variable *i* between *Start* and *End* of the project.
  For each value of *i*, a text strip is created (44-49) of exactly one frame; from *i* to *i+1* (38-42).
  The text property of that strip is then filled in and the strip is added to a list `added_strips` (31 and 60).
  At the end of this loop, all created text strips are grouped together into one meta strip (62-66).
  You can see the individual text strips if you tab into the meta strip.
..

このスクリプトの魔法は 37 行目から 60 行目の間で発生します。
これは基本的に、プロジェクトの *開始* と *終了* の間の変数 *i* のループです。
*i* の各値に対して、正確に 1 フレームのテキスト ストリップが作成されます (44 ～ 49)。
*i* から *i+1* (38-42)まで。次に、そのストリップの text プロパティが入力され、そのストリップがリスト `added_strips` (31 および 60) に追加されます。
このループの最後で、作成されたすべてのテキスト ストリップが 1 つのメタ ストリップにグループ化されます (62 ～ 66)。
タブでメタ ストリップに移動すると、個々のテキスト ストリップが表示されます。

..
  This script gives you a lot of flexibility to customize the overlay. A few examples:
  The overlay text should also contain the frame number.
..
このスクリプトを使用すると、オーバーレイを非常に柔軟にカスタマイズできます。
いくつかの例: オーバーレイ テキストにはフレーム番号も含める必要があります。

.. code-block::

    text_strip.text = "Frame: " + str(i) + " - Time: " + str(bpy.utils.smpte_from_frame(i))

.. The overlay text should be in the middle of the preview window
オーバーレイ テキストはプレビュー ウィンドウの中央にある必要があります。

.. code-block::

    text_strip.location[1] = 0.5

.. A timecode should only be generated every 10 frames. (Use the modulo-operator (%) for this).
タイムコードは 10 フレームごとにのみ生成される必要があります。 (これにはモジュロ演算子 (%) を使用します)。

.. code-block::

   if (i % 10)  != 0:
       text_strip.text = ""
   else:
       text_strip.text = str(bpy.utils.smpte_from_frame(i))

.. And, of course, the blender VSE could also be used, for example by adding a color strip for the background color.
そしてもちろん、たとえば背景色のカラー ストリップを追加するなどして、ブレンダー VSE を使用することもできます。

..
  Another approach, suggested by
  `Garrett <https://blender.stackexchange.com/questions/7904/how-can-i-make-dynamic-text-in-an-animation>`_,
  is to create a 3D-text object and animate the content, based on the current frame.
..
`Garrett <https://blender.stackexchange.com/questions/7904/how-can-i-make-dynamic-text-in-an-animation>`_ が提案した別のアプローチは 、3D テキスト オブジェクトを作成し、現在のフレームに基づいてコンテンツをアニメーション化することです。

.. code-block::

    import bpy

    scene = bpy.context.scene
    obj = scene.objects['Text']

    def recalculate_text(scene):
        time_code = str(bpy.utils.smpte_from_frame(scene.frame_current))
        obj.data.body = 'Current time: ' + str(time_code)

    bpy.app.handlers.frame_change_pre.append(recalculate_text)


.. 1. Switch to the Layout workspace and add a text object.
   Customize the text object in terms of font, size, position, ... to your liking.
.. 2. Give your text object a name. The code above assumes the standard name "Text".
.. 3. Switch to the scripting workspace, create a new text file
   and copy the code from above into the script editor.
.. 4. Run the code with the menu Text > Run Script or Alt + P.
.. 5. Switch back to the Layout workspace and move the play head.
   You will see that the text content is changed to something as
   "Current time: 00:00:00:12" depending on the position of the play head.
.. 6. Make a test render. Change the camera position if needed.
.. 7. If you need this clip in the Video Sequence Editor (VSE): create a new scene.
   Switch to the new scene and add a scene strip (Shift + A > Scene).
1. Layout workspaceに切り替えて、テキスト オブジェクトを追加します。フォント、サイズ、位置などの点でテキスト オブジェクトを好みに合わせてカスタマイズします。
2. テキストオブジェクトに名前を付けます。上記のコードは標準名「Text」を想定しています。
3. Scripting workspace に切り替え、新しいテキスト ファイルを作成し、上記のコードをスクリプト エディターにコピーします。
4. [Text]メニュー > [Run Scrpt] または :kbd:`Alt+P` を使用してコードを実行します。
5. レイアウト ワークスペースに戻り、再生ヘッドを移動します。再生ヘッドの位置に応じて、テキストの内容が「現在時刻: 00:00:00:12」のように変化することがわかります。
6. テストレンダリングを行います。必要に応じてカメラの位置を変更します。
7. Video Sequence Editor (VSE) でこのクリップが必要な場合は、新しいシーンを作成します。新しいシーンに切り替えて、シーンストリップを追加します (:kbd:`Shift+A` > Scene)。

..
  Attention: this scene strip will always start at time 0, no matter where you position the strip in the VSE.
  This could be handy, if for example, you want to show the time code relative to a specific strip.
..
注意: このシーン ストリップは、VSE 内のどこにストリップを配置しても、常に時刻 0 から開始されます。これは、たとえば特定のストリップに関連するタイムコードを表示したい場合に便利です。

.. **D. Placeholder image generators**
**D. プレースホルダー画像ジェネレーター**

..
  An image placeholder is a dummy image.
  There are several websites that can either provide you with the link to these images
  or give you the possibility to generate these images yourself on your computer.
  Of course, you can always save the online images behind the link.
..

画像プレースホルダーはダミー画像です。これらの画像へのリンクを提供したり、コンピュータ上でこれらの画像を自分で生成したりできる Web サイトがいくつかあります。もちろん、リンクの背後にあるオンライン画像をいつでも保存できます。

..
  For example, the URL http://via.placeholder.com/640x360 or https://placekitten.com/640/360
  will show you a placeholder image of 640x360 pixels in the browser, which you can save to your computer.
..

たとえば、URL http://via.placeholder.com/640x360 または https://placekitten.com/640/360 [#f1]_ を使用すると、ブラウザーに 640x360 ピクセルのプレースホルダー画像が表示され、コンピューターに保存できます。

.. figure:: http://via.placeholder.com/640x360
   :align: center
   :alt: Test file from placeholder.com

   図 3: via.placeholder.com からのテスト ファイル


.. figure:: https://placekitten.com/640/360
    :align: center
    :alt: Test file from placekitten.com

    図 4: placekitten.com からのテスト ファイル

..
  These placeholder images are mostly used in website design to create mockups of webpages
  (together with Lorem Ipsum generators for text).
  Search in Google for "image placeholder" to find other websites or generators.
..
これらのプレースホルダー画像は主に、Web ページのモックアップを作成するために Web サイトのデザインで使用されます
(テキスト用の Lorem Ipsum ジェネレーターとともに)。
他の Web サイトやジェネレーターを見つけるには、Google で「画像プレースホルダー」を検索してください。

**E. Blender Open-Movies**

..
  The WebM-format of the Spring open-movie can be downloaded from
  `Wikimedia Commons <https://commons.wikimedia.org/wiki/File:Spring_-_Blender_Open_Movie.webm>`_.
..
Spring オープン ムービーの WebM 形式は、 `Wikimedia Commons <https://commons.wikimedia.org/wiki/File:Spring_-_Blender_Open_Movie.webm>`_ からダウンロードできます。


.. **F. Useful websites**
**F. 役立つウェブサイト**

.. 1. https://www.demolandia.net/: Demolandia is, essentially, an audiovisual library where you will find a great diversity of images,
   audio and video files (e.g. 4K) related to the cinema.
.. 2. https://file-examples.com/:
   .. This website is a service designed for developers,
   .. designers, testers. Various categories: video, audio, documents, images, ...
1. https://www.demolandia.net/: Demolandia は本質的に、映画に関連する多種多様な画像、オーディオ、ビデオ ファイル (例: 4K) が見つかるオーディオビジュアル ライブラリです。
2. https://file-examples.com/: この Web サイトは、開発者、デザイナー、テスター向けに設計されたサービスです。さまざまなカテゴリ: ビデオ、オーディオ、ドキュメント、画像など

.. rubric:: 脚注

.. [#f1] (訳注) placekitten.com は、翻訳時点(2024-03-22)でダウンしているようです。
