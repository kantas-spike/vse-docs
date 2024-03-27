Directory structure
===================

.. A video project is most likely a combination of several different assets.
.. You can separate them into three broad categories.
ビデオ プロジェクトは、多くの場合、複数の異なるアセットを組み合わせたものです。それらは 3 つの大きなカテゴリに分類できます。

.. - Video files: video clips (or movies in Blender-talk), photos, graphic files (charts, logos, ...), and Visual Effects (VFX) such as masks, lens flares, animation.
.. - Audio files: recorded dialog, voice-over, music, and Sound Effects (SFX) such as environmental sounds, swooshes, ...
.. - Project files: the blend files and backups, (partial) render results, documentation such as scripts and storyboards.
- ビデオ ファイル
   ビデオ クリップ (または Blender-talk のムービー)、写真、グラフィック ファイル (チャート、ロゴなど)、およびマスク、レンズ フレア、アニメーションなどの視覚効果 (VFX)。
- オーディオ ファイル
   録音されたダイアログ、ナレーション、音楽、および環境音、シューッという音などの効果音 (SFX)
- プロジェクト ファイル
    blendファイルとバックアップ、(部分的な) レンダリング結果、スクリプトやストーリーボードなどのドキュメント。

.. Together they can form rapidly an intangible heap of files. It's good practice to collect all those assets in *one* project directory with appropriate subdirectories.
これらを組み合わせると、つかみどころないファイルの山が急速に形成されます。

これらすべてのアセットを、適切なサブディレクトリを含む 1つのプロジェクト ディレクトリに収集することをお勧めします。

.. Why? It will lower the probability that you accidentally delete a file (which will result in a 'file not found' error) or that you forget to include a necessary file when transferring the project ('file is missing' error). And most of all, an appropriate directory structure, will help you to keep a clear overview of your assets.

なぜ？ 誤ってファイルを削除したり (「ファイルが見つかりません」エラーが発生する)、またはプロジェクトを転送するときに必要なファイルを含めるのを忘れた (「ファイルが見つかりません」エラーが発生する) 可能性が低くするためです。そして何よりも、適切なディレクトリ構造は、アセットの概要を明確に保つのに役立ちます。

.. seealso::

    .. Blender can incorporate some files within the Blend file
    .. (see `Packed Data <https://docs.blender.org/manual/en/latest/files/blend/packed_data.html>`_).
    .. However, this doesn't work with video files, which can have very huge file sizes. So, it's better to assure that your project directory contains all necessary files.
    Blender は、blend ファイル内にいくつかのファイルを組み込むことができます。
    (参照 `Packed Data <https://docs.blender.org/manual/en/latest/files/blend/packed_data.html>`_)
    ただし、ファイル サイズが非常に大きくなる可能性があるビデオ ファイルではこれは機能しません。したがって、プロジェクト ディレクトリに必要なファイルをすべて含めることをお勧めします。

.. It's also good practice to use some kind of naming convention and add metadata.
.. Figure 1 shows a possible example, based on our categorization of the assets above.
.. The directories are numbered so that they mimic a normal workflow.
何らかの命名規則を使用してメタデータを追加することもお勧めします。
図 1 は、上記の資産の分類に基づいた考えられる例を示しています。
ディレクトリには、通常のワークフローを模倣するように番号が付けられています。

.. figure:: /images/vse_setup_project_dir-structure-example.svg
   :scale: 50 %
   :alt: Organizing your project

   Figure 1: プロジェクトの構成

.. Blender haven't yet implemented the concept of Bins (virtual directories that only exist within the project). Nor does it have a full-blown asset manager for its video assets. For the moment, you're stuck with the `File Browser <https://docs.blender.org/manual/en/dev/editors/file_browser.html>`_.

Blender はまだ Bins (プロジェクト内にのみ存在する仮想ディレクトリ) の概念を実装していません。また、ビデオアセット用の本格的なアセットマネージャーもありません。現時点では、 `File Browser <https://docs.blender.org/manual/en/latest/editors/file_browser.html>`_ を使用することになります。
