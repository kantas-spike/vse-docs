******
FFMPEG
******

.. Here you'll find a few useful commands for FFMPEG to work with video and audio. FFMPEG is a command line tool for handling (decode, encode, convert, ...) video and audio files. It is used by many commercial and free software products, including Blender.  The core is the FFMPEG program, together with a video & audio player (FFPLAY) and a stream analyzer (FFPROBE).

ここでは、FFMPEG がビデオとオーディオを操作するための便利なコマンドをいくつか紹介します。 FFMPEG は、ビデオ ファイルとオーディオ ファイルを処理 (デコード、エンコード、変換など) するためのコマンド ライン ツールです。これは、Blender を含む多くの商用および無料ソフトウェア製品で使用されています。コアは FFMPEG プログラムと、ビデオ & オーディオ プレーヤー (FFPLAY) およびストリーム アナライザー (FFPROBE) です。

.. ## 1. Generate testfiles
テストファイルを生成する
----------------

.. Sometimes you need a test video or test image with a specific resolution, duration or framerate. You can first try with ffplay to view the test video. Replace afterwards the ffplay command with ffmpeg and add the outputfile parameter.

場合によっては、特定の解像度、期間、またはフレームレートのテスト ビデオまたはテスト画像が必要になることがあります。まず ffplay を試してテストビデオを表示してください。その後、ffplay コマンドを ffmpeg に置き換え、outputfile パラメーターを追加します。

.. code-block::

   ffplay -f lavfi -i testsrc=duration=10:size=1280x720:rate=30

   ffmpeg -f lavfi -i testsrc=duration=10:size=1280x720:rate=30 test.mp4

..
This command will show/create a count-up video with a resolution of 1280 x 720 pixels, a framerate of 30 frames per second with a duration of 10 seconds in MP4-format
More commands and test formats can be found at [bogotobogo](https://www.bogotobogo.com/FFMpeg/ffmpeg_video_test_patterns_src.php).
..

このコマンドは、解像度 1280 x 720 ピクセル、フレームレート 30 フレーム/秒、持続時間 10 秒のカウントアップ ビデオを MP4 形式で表示/作成します。
その他のコマンドとテスト形式は、 `bogotobogo <https://www.bogotobogo.com/FFMpeg/ffmpeg_video_test_patterns_src.php>`_ を参照してください。。

.. The following command will show/create a red color background with opacity set to 0.2, with a duration of 10 seconds and a resolution of 640x480 in MP4-format.

次のコマンドは、不透明度が 0.2 に設定された赤色の背景を、持続時間 10 秒、解像度 640x480 の MP4 形式で表示/作成します。

.. code-block::

   ffplay -f lavfi -i color=c=red@0.2:duration=5:s=640x480:r=10

   ffmpeg -f lavfi -i color=c=red@0.2:duration=5:s=640x480:r=10 test.mp4


.. ## 2. Combine several video fragments into one file
複数のビデオ フラグメントを 1 つのファイルに結合
-------------------------------------------------

.. I used to create my videos in separate scenes; e.g. one scene for each month of a yearly review montage. During the year I could render the separate scenes into a video fragment. At the end of the year I need then to combine them into one piece.

以前はビデオを別々のシーンで作成していました。たとえば、年次レビュー モンタージュの各月に 1 つのシーンです。
この 1 年の間に、個別のシーンをビデオ フラグメントにレンダリングすることができました。年末にはそれらを 1 つの作品にまとめる必要があります。

.. code-block::

   concatenate: ffmpeg -safe 0 -f concat -i list.txt -c copy output.mp4


.. The output file is called "output.mp4". The monthly fragments are named in a separate file "list.txt" which contains 12 lines with the name of the fragments, eg. "01-jan.mp4 02-feb.mp4 ... 12-dec.mp4". You have to run the command in the folder where the fragments are located.

出力ファイルは "output.mp4" にします。毎月のフラグメントは、フラグメントの名前を含む 12 行を含む別のファイル「list.txt」で名前が付けられます。 「01-jan.mp4 02-feb.mp4 … 12-dec.mp4」。フラグメントが配置されているフォルダーでコマンドを実行する必要があります。

.. ## 3. Check for variable frame rate
可変フレームレートを確認する
-------

.. The following command will check for VFR. It uses the videofilter vfrdet.
次のコマンドは VFR をチェックします。ビデオフィルター vfrdet を使用します。

.. code-block::

   ffmpeg -i test_input.mp4 -vf vfrdet -f null -

.. The output is directed to the screen. The VFR parameter shows the percentage of variable frame rate. Between brackets are the number of frames with VFR (0 in this example) and with CFR (532 in this example); see below.

出力は画面に送られます。 VFR パラメータは、可変フレーム レートの割合を示します。括弧内は、VFR (この例では 0) と CFR (この例では 532) のフレーム数です。以下を参照してください。 [#f1]_

``[Parsed_vfrdet_0 @ 000001f8b3902e80] VFR:0.000000 (0/532)``

.. rubric:: 脚注

.. [#f1] `VFR(Variable Frame Rate)`: 可変フレームレート、`CFR(Constant Frame Rate)`: 固定フレームレート
