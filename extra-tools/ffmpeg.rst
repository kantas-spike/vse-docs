FFMPEG
******

.. FFMPEG is a command line tool for handling (decode, encode, convert, …) video and audio files. It is used by many commercial and free software products, including Blender. The core is the FFMPEG program, together with a video & audio player (FFPLAY) and a stream analyzer (FFPROBE).

FFMPEG は、ビデオ ファイルとオーディオ ファイルを処理 (デコード、エンコード、変換など) するためのコマンド ライン ツールです。これは、Blender を含む多くの商用および無料ソフトウェア製品で使用されています。コアは FFMPEG プログラムと、ビデオ & オーディオ プレーヤー (FFPLAY) およびストリーム アナライザー (FFPROBE) です。

.. There are lots of tutorials for installing FFMEG and for using the command line (just google "how install ffmpeg"). A nice `3-part tutorial <https://www.youtube.com/watch?v=MPV7JXTWPWI&t=669s>`_ is by NerdFirst.

FFMEG のインストールやコマンド ラインの使用に関するチュートリアルはたくさんあります (Google で「ffmpeg のインストール方法」を検索してください)。素晴らしい `3-part tutorial <https://www.youtube.com/watch?v=MPV7JXTWPWI&t=669s>`_ がNerdFirst によって提供されています。

.. **1. Trim a video lossless**

ビデオをロスレスでトリミングする
----------------------------

.. You have a source file "input.mkv" from which you want to cut a part in the middle. The following command will cut out the section from about 2 min and 2 sec (after the -ss command) to 2 min 43 sec (after the -to command). Both the video (c:v) and the audio (c:a) are copied without recompressing (copy). The result is wirtten to "output.mkv"

ソースファイル "input.mkv" の途中の部分を切り取りたいとします。次のコマンドは、約 2 分 2 秒 (-ss コマンド後) から 2 分 43 秒 (-to コマンド後) のセクションを切り出します。ビデオ (c:v) とオーディオ (c:a) の両方が再圧縮されずにコピーされます (コピー)。結果は "output.mkv" に書き込まれます。

``ffmpeg -i input.mkv -ss 00:02:02 -to 00:02:43 -c:v copy -c:a copy output.mkv``


.. **2. Combine several video fragments into one file**
複数のビデオフラグメントを 1 つのファイルに結合します
-------

.. I used to create my videos in separate scenes; e.g. one scene for each month of a yearly review montage. During the year I could render the separate scenes into a video fragment. At the end of the year I need then to combine them into one piece.

以前はビデオを別々のシーンで作成していました。たとえば、年次レビュー モンタージュの各月に 1 つのシーン。この 1 年の間に、個別のシーンをビデオ フラグメントにレンダリングすることができました。年末にはそれらを 1 つの作品にまとめる必要があります。

``ffmpeg -safe 0 -f concat -i list.txt -c copy output.mp4``

.. The output file is called “output.mp4”. The monthly fragments are named in a separate file “list.txt” which contains 12 lines with the name of the fragments, eg. “01-jan.mp4 02-feb.mp4 … 12-dec.mp4”. You have to run the command in the folder where the fragments are located.

出力ファイルは "output.mp4" と呼ばれます。毎月のフラグメントは、フラグメントの名前を含む 12 行を含む別のファイル "list.txt" で名前が付けられます。 "01-jan.mp4 02-feb.mp4 … 12-dec.mp4"。フラグメントが配置されているフォルダーでコマンドを実行する必要があります。

.. **3. Generate testfiles**
テストファイルを生成する
------

.. Sometimes you need a test video or test image with a specific resolution, duration or framerate. You can first try with ffplay to view the test video. Replace afterwards the ffplay command with ffmpeg and add the outputfile parameter.

場合によっては、特定の解像度、期間、またはフレームレートのテスト ビデオまたはテスト画像が必要になることがあります。まず ffplay を試してテストビデオを表示してください。その後、ffplay コマンドを ffmpeg に置き換え、outputfile パラメーターを追加します。

``ffplay -f lavfi -i testsrc=duration=10:size=1280x720:rate=30``

``ffmpeg -f lavfi -i testsrc=duration=10:size=1280x720:rate=30 test.mp4``

.. This command will show/create a count-up video with a resolution of 1280 x 720 pixels, a framerate of 30 frames per second with a duration of 10 seconds in MP4-format More commands and test formats can be found at `bogotobogo <https://www.bogotobogo.com/FFMpeg/ffmpeg_video_test_patterns_src.php>`_.

このコマンドは、解像度 1280 x 720 ピクセル、フレームレート 30 フレーム/秒、持続時間 10 秒の MP4 形式のカウントアップ ビデオを表示/作成します。その他のコマンドとテスト形式については、 `bogotobogo <https://www.bogotobogo.com/FFMpeg/ffmpeg_video_test_patterns_src.php>`_ を参照してください。

.. The following command will show/create a red color background with opacity set to 0.2, with a duration of 5 seconds and a resolution of 640x480 with 10 a framerate of 10 fps in MP4-format.

次のコマンドは、不透明度が 0.2 に設定され、持続時間が 5 秒、解像度が 640x480、フレームレートが 10 fps の MP4 形式で赤色の背景を表示/作成します。

``ffplay -f lavfi -i color=c=red@0.2:duration=5:s=640x480:r=10``

``ffmpeg -f lavfi -i color=c=red@0.2:duration=5:s=640x480:r=10 test.mp4``

.. **4. Create multiple video channels into one container**
複数のビデオチャンネルを 1 つのコンテナに作成する
-----

.. Some video containers can contain multiple video and audio channels; for example two surveillance camera outputs next to each other. In Blender you can select the channel to preview (not both at the same time) with Strip > Source panel > Stream index. The following command creates a two video channels  into one container.

一部のビデオ コンテナには、複数のビデオおよびオーディオ チャネルを含めることができます。たとえば、2 つの監視カメラ出力が隣り合っている場合などです。Blender では、[Strip] > [Source] パネル > [Stream index] を使用して、プレビューするチャンネルを選択できます (同時に両方を選択することはできません)。次のコマンドは、2 つのビデオ チャネルを 1 つのコンテナに作成します。

``ffmpeg -i input-1.mp4 -i input-2.mp4 -map 0:0 -map 1:0 output.mkv``

.. **4. Fix the "not divisible by 2" error**
「2で割り切れない」エラーを修正
-----

.. Sometimes you need a render resolution, other than the classic 1080p (1920 x 1080). You can then enter your X and Y Resolution in the Dimensions panel of the Output Properties. However, when you try for example 1500 px x 399 px and use the H.264 codec you'll get the "not divisible by 2" error (or worse sometimes, a crash). The reason for this error is that the H.264 encoder uses macroblocks of a fixed size (e.g. 4x4) to compress your movie. Each frame is divided into these small macroblocks and to compress your video, it only encodes the differences between these macroblocks.  However, this adds the requirement that the width and height of your movie must be divisible by 2.  Changing the Y-resolution to 400 will fix the problem.

場合によっては、クラシックな 1080p (1920 x 1080) 以外のレンダリング解像度が必要になることがあります。次に、[Output]プロパティ の [Dimensions] パネルに X および Y 解像度を入力できます。ただし、たとえば 1500 ピクセル x 399 ピクセルで H.264 コーデックを使用しようとすると、「2 で割り切れません」というエラーが発生します (さらに悪いことに、クラッシュが発生する場合もあります)。このエラーの理由は、H.264 エンコーダが固定サイズ (4x4 など) のマクロブロックを使用してムービーを圧縮するためです。各フレームはこれらの小さなマクロブロックに分割され、ビデオを圧縮するために、これらのマクロブロック間の差異のみがエンコードされます。ただし、これにより、ムービーの幅と高さが 2 で割り切れる必要があるという要件が追加されます。Y 解像度を 400 に変更すると、問題が解決します。

.. If, for some reason, you want to stick with the original resolution of 1500 x 399, then you have to render your animation first as a PNG sequence. The PNG format does not has this restriction on width & height. Of course, you don't have a playable movie.

何らかの理由で、元の解像度 1500 x 399 を維持したい場合は、最初にアニメーションを PNG シーケンスとしてレンダリングする必要があります。PNG 形式には、幅と高さに関するこの制限はありません。もちろん、再生可能なムービーはありません。

.. Therefore, you need FFMPEG to create a movie (e.g. MP4) of it. To create a movie out of a sequence of images, you need the following command:
したがって、ムービー (MP4 など) を作成するには FFMPEG が必要です。一連の画像からムービーを作成するには、次のコマンドが必要です。

``ffmpeg -f image2 -r 24 -i %04d.png test.mp4``

- ``-f image2`` specifies the filter to convert from images to movie
- ``-r 24`` sets the framerate to 24 fps
- ``-i %04d.png`` specifies the input as a 4 digit number, followed by .png, e.g. 0001.png, 0002.png, ...
- ``test.mp4`` specifies the output file.


