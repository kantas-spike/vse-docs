.. _bpy.types.ImageSequence:

**************************
Image/Image Sequence ストリップ
**************************

.. figure:: /images/vse_setup_project_striptypes_add-strips.png
   :scale: 50%
   :alt: Add stips
   :align: Right

   図1 追加コマンド

..
  Image and Image Strip are two different strip types.
  Nevertheless, you need the same command to add them to the timeline (see figure 1).
  The :ref:`default <default-color>` color of the Image/Image Sequence strip bar is: :image:`███`
..

Imageストリップ と Image Sequence ストリップは、2 つの異なるストリップ タイプです。
ただし、タイムラインに追加するには同じコマンドが必要です (図 1 を参照)。
画像/画像シーケンスのストリップバーのデフォルトの色は :image:`███` です。

..
  The input source of an Image/Image Sequence strip is a graphics file
  or a collection of graphics files with extension
  ``.BMP``, ``.Iris``, ``.PNG``, ``.JPEG``, ``.JPG2000``, ``.targa``,
  ``.cineon & DPX``, ``openEXR``, ``Radiance HDR`` or ``.TIFF``.
  For more in-depth information about these formats,
  see `graphics formats <https://docs.blender.org/manual/en/dev/files/media/image_formats.html>`_.
..

Image/Image Sequence ストリップの入力ソースは、以下の拡張子をもつ 画像ファイルまたは画像ファイルのコレクション です。
またはのこれらの形式の詳細については、`graphics formats <https://docs.blender.org/manual/en/dev/files/media/image_formats.html>`_ を参照してください。

  ``.BMP``, ``.Iris``, ``.PNG``, ``.JPEG``, ``.JPG2000``, ``.targa``,
  ``.cineon & DPX``, ``openEXR``, ``Radiance HDR``, ``.TIFF``.




Image
=====

..
  Although an image file contains normally only one image,
  the resulting Image strip has a length of 25 identical frames or stills.
  As such, these strips are very much like Movie strips.
  The default length of 25 is hard-coded but you can change it easily
  by entering a new Duration or by dragging the strip handles.
..

通常、画像ファイルには 1 つの画像しか含まれていませんが、結果として得られる画像ストリップの長さは 25 個の同一のフレームまたは静止画になります。
そのため、これらのストリップは映画のストリップに非常によく似ています。デフォルトの長さ 25 はハードコーディングされていますが、
新しい Duration を入力するか、ストリップ ハンドルをドラッグすることで簡単に変更できます。

.. note::
  ..
   The exact numerical Offset is stored in two unexposed fields: *still_offset_start*
   and *still_offset_end*. See :doc:`Extra Tools > Python > Useful scripts </extra-tools/python-useful-scripts>`
   to make those timecodes visible in the sidebar and :ref:`Movie strip > Time panel <time-panel>` for an explanation.
  ..

  オフセットの正確な数値は、*still_offset_start* と *Still_offset_end* という2 つの非公開フィールド [#f1]_ に保存されます。
  説明については、 :doc:`Extra Tools > Python > Useful scripts </extra-tools/python-useful-scripts>`
  および :ref:`Movie strip > Time panel <time-panel>` を参照してください。


Image Sequence
==============

..
  The input of an Image Sequence strip is a sequence of graphic files, e.g. *0001.png*, *0002.png*, *0003.png*, etc.
  Most of the time these files are numbered as in the previous example.
  However, this is not necessary because Blender creates the sequence based on the sort order in the File browser.
  You could name them also as *a.png*, *b.png*, and *c.png*.
  If - by coincidence - you sorted the above files in reversed order,
  then the sequence will begin with *0003.png* or *c.png*.
..

Image Sequence ストリップの入力は、一連のグラフィック ファイル (例: 0001.png、0002.png、0003.pngなど) です。
ほとんどの場合、これらのファイルには前の例のように番号が付けられます。
ただし、Blender はファイル ブラウザーの並べ替え順序に基づいてシーケンスを作成するため、これは必要ありません。
それらにa.png、b.png、およびc.pngという名前を付けることもできます。
偶然にも、上記のファイルを逆の順序で並べ替えた場合、順序は0003.pngまたはc.pngで始まります。


..
  When this image sequence is added to the timeline, the resulting strip is treated as one movie.
  In the :ref:`Source panel <image-source-panel>` of the sidebar you can retrieve the individual image names.
..

この Image Sequence がタイムラインに追加されると、結果のストリップが 1 つのムービーとして扱われます。
サイドバーの :ref:`Source panel <image-source-panel>` で個々のイメージ名を取得できます。

..
  Sometimes, you don't have all of the image files available at the time you want to create the Image Sequence.
  You can then enable the Use placeholders checkbox when adding the image strip.
  This will create the image strip with empty -but named- frames for the missing images.
  Suppose 0002.png is missing in the previous example.
  Creating the Image Sequence -- with Use Placeholders checked -- will create a strip of three frames.
  The second frame appears as black but is named 0002.png.
  Later on, you can add this file to the folder with the others.
  This method will only work with correctly numbered sequences.
  Our previous example with *a.png*, *b.png*, *c.png* will not succeed.
..

Image Sequence を作成するときに、利用可能なイメージ ファイルのすべてが存在しない場合があります。
これで、Image ストリップを追加するときに [Use placeholders] チェックボックスを有効にすることができます。
これにより、欠落している画像に対して空の、しかし名前が付けられたフレームを含む画像ストリップが作成されます。
前の例で 0002.png が欠落しているとします。
[Use placeholders] をチェックしてイメージ シーケンスを作成すると、3 つのフレームのストリップが作成されます。
2 番目のフレームは黒で表示されますが、名前は 0002.png です。後で、このファイルを他のファイルと一緒にフォルダーに追加できます。
このメソッドは、正しい番号が付けられたシーケンスでのみ機能します。a.png、b.png、c.pngを使用した前述の例は成功しません。

Options
=======

.. note::
  .. Panels documented elsewhere!
  パネルは他の場所で文書化されています。

  .. The following panels are identical to those from the Movie strip:
  次のパネルは、Movie ストリップのパネルと同じです

  - :ref:`Compositing <compositing-panel>`
  - :ref:`Transform <transform-panel>`
  - :ref:`Crop <crop-panel>`
  - :ref:`Video <video-panel>`
  - :ref:`Color <color-panel>`
  - :ref:`Time <time-panel>`
  - :ref:`Source <source-panel>`
  - :ref:`Custom <custom-panel>`.


.. Only in the Source panel, there are minor changes.
ソースパネルのみに若干の変更があります。

Source
------

.. _image-source-panel:

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Source
   **Context**:    Video Sequence Editor > Sequencer
   **Location**:   Sidebar > Strip
   =============   ==========================================================================

.. figure:: /images/vse_setup_project_striptypes_panel-source-strip-image.png
   :scale: 50%
   :alt: Source Property of Image Strip
   :align: Right

   図2 ソース プロパティ

..
  In contrast to the Movie strip, the Source property of the Image Sequence strip
  is split into a directory and a file component (see figure 2).
..

Moveストリップとは対照的に、Image Sequenceストリップの Source プロパティはディレクトリとファイル コンポーネントに分割されています (図2)。


Directory
   .. The directory that contains the source files.
   .. When the image files have moved this field can be updated instead of having to recreate the strip.
   ソースファイルが含まれるディレクトリ。画像ファイルが移動された場合、ストリップを再作成する代わりに、このフィールドを更新できます。

File
   .. The filename of the image for that particular frame, e.g. *0001.png*.
   .. If you want to replace a particular frame in the Image sequence with another one, you can change the name here.
   その特定のフレームの画像のファイル名 (例: *0001.png* )。画像シーケンス内の特定のフレームを別のフレームに置き換えたい場合は、ここで名前を変更できます。

Color Space
   :ref:`参照 Movie strip <source-panel>`.

Alpha
   .. The options are *Premultiplied* or *Straight*.
   オプションは[Premultiplied]または[Straight]です。


   .. todo::
    ..
      Clarify the following text. Next to the Red, Green & Blue channels,
      most graphic formats at the top of this page support a fourth channel:
      the Alpha channel. One notably exception is JPEG.

      Alpha channels store transparency information in files in one of two ways:
      straight or premultiplied. Although the alpha channels are the same, the color channels differ.

      With straight (or unmatted) channels, transparency information is stored
      only in the alpha channel, not in any of the visible color channels.
      With straight channels, the effects of transparency aren’t visible until
      he image is displayed in an application that supports straight channels.

      With premultiplied (or matted) channels, transparency information is stored
      in the alpha channel and also in the visible RGB channels,
      which are multiplied with a background color.
      The colors of semitransparent areas, such as feathered edges,
      are shifted toward the background color in proportion to their degree of transparency.

      Some software lets you specify the background color with which the channels are premultiplied;
      otherwise, the background color is usually black or white.

      Premultiplied (RGB channels in transparent pixels are multiplied by the alpha channel)
      or Straight (RGB channels in transparent pixels are unaffected by the alpha channel) of the image.
    ..

    次のことを明確にしてください。
    このページの上部にあるほとんどのグラフィック形式は、赤、緑、青チャネルの隣に 4 番目のチャネルであるアルファ チャネルをサポートしています。顕著な例外の 1 つは JPEG です。

    アルファ チャネルは、透明度情報を 2 つの方法 (直接または事前乗算) のいずれかでファイルに保存します。アルファ チャネルは同じですが、カラー チャネルは異なります。

    ストレート (またはマットされていない) チャネルの場合、透明度情報はアルファ チャネルにのみ保存され、表示されるカラー チャネルには保存されません。ストレート チャネルの場合、ストレート チャネルをサポートするアプリケーションで画像が表示されるまで、透明度の効果は見えません。

    事前乗算された (またはマットされた) チャネルでは、透明度情報がアルファ チャネルに保存され、背景色と乗算される可視の RGB チャネルにも保存されます。ぼかしエッジなどの半透明領域の色は、透明度に比例して背景色に向かってシフトされます。

    一部のソフトウェアでは、チャンネルに事前乗算する背景色を指定できます。それ以外の場合、背景色は通常黒または白です。

    イメージの事前乗算 は (透明ピクセルの RGB チャネルがアルファ チャネルで乗算される)。
    ストレート は (透明ピクセルの RGB チャネルがアルファ チャネルの影響を受けない)。

Change Datafile
  ..
   Replaces the complete image sequence with the selected images.
   It is advisable to have the same number of images in the sequence as the original strip.
   The duration of the original strip is indeed not changed; so, if there are fewer images the last one is repeated,
   or if there more images the last ones are cut off.
  ..
  完全な画像シーケンスを選択した画像に置き換えます。シーケンス内に元のストリップと同じ数の画像を含めることをお勧めします。元のストリップの長さは実際には変更されません。したがって、画像の数が少ない場合は最後の画像が繰り返され、画像の数が多い場合は最後の画像が切り取られます。

Resolution
   :ref:`参照 Movie strip <resolution>`.

.. rubric:: 脚注

.. [#f1] Blender3.2以降では、 *frame_still_start* と *frame_still_end* ではなく、 *frame_offset_start* と *frame_offset_end* の負値で表現します。
