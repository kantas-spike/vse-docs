###########
追加ツール
###########

.. Blender's VSE is a great video editor but of course it's not a Swiss knife. In addition, the main focus of Blender is not on video editing but on 3D modeling. Some areas such as sound are less important in that perspective. So,  some functionality is not available or up-to-date. You'll need some extra-tools for this.

Blender の VSE は優れたビデオエディタですが、もちろんスイスナイフではありません。また、Blender の主な焦点はビデオ編集ではなく 3D モデリングです。サウンドなどの一部の領域は、その観点からはそれほど重要ではありません。そのため、一部の機能が利用できないか、最新ではありません。これには追加のツールが必要になります。

.. In this section, we describe some extra tools; mainly open source that you might need when editing.

このセクションでは、いくつかの追加ツールについて説明します。主にオープンソースであり、編集時に必要になる場合があります。

**Python**
  .. Blender uses the Python programming language for its scripting API (Application Programming Interface). Many internal data structures and operators can be accessed through a Python script. The `official docs <https://docs.blender.org/api/current/>`_ are well-written. In this text we provide some :doc:`usefull scripts <python-useful-scripts>` and an in-depth description of  the :doc:`Scripting Workspace <python-scripting-workspace>`.
  Blender は、スクリプト API (アプリケーション プログラミング インターフェイス) に Python プログラミング言語を使用します。多くの内部データ構造と演算子には、Python スクリプトを通じてアクセスできます。 `official docs <https://docs.blender.org/api/current/>`_ はよく書かれています。このテキストでは、いくつかの :doc:`usefull scripts <python-useful-scripts>` と、 :doc:`Scripting Workspace <python-scripting-workspace>` の詳細な説明を提供します。

FFmpeg
  .. FFmpeg is a open-source framework to work with video and audio. Blender's VSE  uses it heavily through its libraries libavcodec, libavutil, ...
  FFmpeg は、ビデオとオーディオを操作するためのオープンソース フレームワークです。Blender の VSE は、ライブラリ libavcodec、libavutil などを通じてこれを頻繁に使用します。

  .. As an end-use, you probably will use the command line tool `ffmpeg <https://ffmpeg.org/ffmpeg.html>`_, the `mediaplayer ffplay <https://ffmpeg.org/ffplay.html>`_, or the multimedia ` stream analyzer ffprobe <https://ffmpeg.org/ffprobe.html>`_.
  最終用途としては、コマンド ライン ツール `ffmpeg <https://ffmpeg.org/ffmpeg.html>`_ 、 `mediaplayer ffplay <https://ffmpeg.org/ffplay.html>`_ 、またはマルチメディア `stream analyzer ffprobe <https://ffmpeg.org/ffprobe.html>`_ を使用することになるでしょう。

  .. We provide some :doc:`useful scripts <ffmpeg>` that you probably will need in your job as a video editor.
  ビデオ編集者としての仕事でおそらく必要となるいくつかの :doc:`useful scripts <ffmpeg>` を提供します。

ExifTool
  .. ExifTool is a platform-independent library and a `command-line application <https://exiftool.org/>`_  command-line application for reading, writing and editing meta information in a wide variety of files (including most graphic file formats).
  ExifTool は、プラットフォームに依存しないライブラリであり、 さまざまなファイル (ほとんどのグラフィック ファイル形式を含む) のメタ情報の読み取り、書き込み、編集を行うための `command-line application <https://exiftool.org/>`_ です。

  .. :doc:`Some usefull scripts <exiftool>` are provided.
  :doc:`Some usefull scripts <exiftool>` が提供されています。

.. toctree::


   Python <python-useful-scripts.rst>
   ffmpeg <ffmpeg>
   Script Editor <python-scripting-workspace.rst>
   exiftool
   creating-test-files
   annotating-screenshot



