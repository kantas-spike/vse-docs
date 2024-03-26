Proxies technical
=================

.. Videos can have huge file sizes. Taken for example a 4K file (3840 x 2160). One uncompressed frame needs 3840 x 2160 x 24 bits (8 bits for each color R, G and B)or 24 883 200 bytes, ~21 MB.
ビデオのファイルサイズは非常に大きくなることがあります。 4K ファイル (3840 x 2160) を例に挙げます。 1 つの非圧縮フレームには、3840 x 2160 x 24 ビット (R、G、B の各色に 8 ビット)、または 24 883 200 バイト、約 21 MB が必要です。

.. The FFProbe code to select the first 10 frames and to pint the picture type
以下は、最初の 10 フレームを選択し、画像タイプを出力する FFProbe コードです。

ffprobe -v error -hide_banner -of default=noprint_wrappers=0 -print_format flat  -select_streams v:0 -show_entries frame=pict_type -read_intervals "%+#10" dolby-4k.mkv


1920 x 1080 = 2 073 600 x 24 bits = 49 766 400 bits / 8 = 6.220 800 / 0 048 576 = 5.932 MB



.. Blender VSE Easy Proxy Addon for Video Sequence Editor
.. From https://blender.community/c/rightclickselect/0Nfbbc/

Blender VSE の簡単なProxy Addon (より引用 https://blender.community/c/rightclickselect/0Nfbbc/)


Ffmpeg Command:

.. We are using this command for building proxy:
プロキシの構築には次のコマンドを使用します。

ffmpeg -i input.mp4 -vf scale=640:-2 -vcodec libx264 -g 1 -bf 0 -vb 0 -crf 20 -preset veryfast -acodec aac -ab 128k out.avi

    .. This will create intraframes in h264 within an AVI container with a fixed width of 640 preserving aspect ratio.
    Fixed ratio of 640:-2 ("-:2" is needed for x264 to use the scale filter which needs to be divisible by 2) Details: https://ffmpeg.org/ffmpeg-filters.html#scale
    これにより、アスペクト比を維持したまま固定幅 640 の AVI コンテナ内に h264 のイントラフレームが作成されます。
    640:-2 の固定比率 (x264 でスケール フィルターを使用するには、2 で割り切れる必要がある「-:2」が必要です)

    詳細: https://ffmpeg.org/ffmpeg-filters.html#scale


.. Reasons we are using fixed width of 640 preserving aspect ratio are:
アスペクト比を維持しながら固定幅 640 を使用する理由は次のとおりです。

    .. It's straight forward. No need to make decision for variable size for a simple proxy operation.
    それは簡単です。単純なプロキシ操作では、可変サイズを選択する必要はありません。

    .. Mixed media like HD and 4k can be used together with the same quality.
    HD や 4k などの混合メディアを同じ品質で併用できます。

    .. The interface can fit 640 width nicely.
    インターフェイスは幅 640 にぴったりフィットします。

    .. Industry is going for 4k and 4k+. Where 25% proxy creates a huge file size of 960x540 for example.
    業界は 4K および 4K+ に向かっています。たとえば、25% プロキシでは 960x540 という巨大なファイル サイズが作成されます。

    .. Variable scaling also affects the encoding speed and frame blending.
    可変のスケーリングは、エンコード速度とフレーム ブレンディングにも影響します。

    .. We are using CRF for the image quality and file size instead.
    代わりに、画質とファイルサイズを考慮して CRF を使用しています。
