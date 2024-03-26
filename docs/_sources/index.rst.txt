+++++++++++++++++++++++++++
.. Blender VSE Unofficial Docs

Blender VSE 非公式文書 [#f1]_
+++++++++++++++++++++++++++


.. toctree::
   :caption: Table of Contents
   :hidden:
   :numbered:


   video_sequencer/index
   video_editing/index
   extra-tools/index

.. This documentation about editing video in Blender is structured in three sections. It's written in a more workflow-oriented approach than the official Blender Reference documentation.

このBlenderによる動画編集の文書は、3つのセクションで構成されます。
この文書は、公式のBlenderリファレンス文書よりも、よりワークフロー思考のアプローチでをで記載されています。 [#f2]_

.. figure:: ./images/vse_icon_sequencer.svg
   :alt: Sequencer icon
   :align: left
   :target: ./video_sequencer/index.html

**Video Sequence Editor**
#########################

.. This section describes the Video Sequence Editor; sometimes also called the *Sequencer*. It is Blender's dedicated *tool* or *editor* to handle video footage.  This is the software corner where you'll spend most of your time as a video editor. So, it is absolutely necessary that you can work fluently and fast in this editor. We describe the major components and their working.

このセクションは、ビデオシーケンスエディターについて説明します。ビデオシーケンスエディターは *シーケンサー* とも呼ばれます。
ビデオ映像を操作するためのBlender専用の *ツール* もしくは *エディター* です。
これは、あなたが動画編集者として一番利用するソフトウェアです。このエディターを使って、よどみなく迅速に作業できることが、絶対に必要です。
その主要なコンポーネントとその働きについて説明します。


.. figure:: ./images/vse_icon_video-editing.svg
   :alt: Sequencer icon
   :align: left
   :target: ./video_editing/index.html

**Video Editing**
#################

.. The Video Editing section is split into 3 chapters, representing a typical workflow of a video editing project: *Setup*, *Edit* and *Render*. You can think of these phases as : pre-editing, editing and post-editing. The editing subsection is of course the most comprehensive with info on montage, effects, color grading and sound editing.

このセクションは、3つの章に分かれており、*セットアップ*、*編集*、*レンダリング* というビデオ編集プロジェクトの一般的なワークフローを表しています。
これらのフェーズは、プリエディティング、エディティング、ポストエディティングと考えることができます。
エディティングサブセクションは、もちろん、モンタージュ、エフェクト、カラーグレーディング、サウンド編集に関する情報が最も充実しています。

.. figure:: ./images/vse_icon_tools.svg
   :alt: Extra tools icon
   :align: left
   :target: ./extra-tools/index.html

**Extra tools**
###############

.. Although Blender's VSE is more than a capable video editor, you will need sometimes some extra-tools to accomplish things such as changing the Exif-data of your source-files, converting media formats, automating some operations. We give a short introduction to the following open-source tools such as Python, ffmpeg, MediaInfo, and ExifTools.

BlenderのVSEは、単なるビデオエディターではありませんが、素材ファイルのExifデータの変更、メディアフォーマットの変換、操作の自動化などを行うには、追加のツールが必要になる場合があります。
Python、ffmpeg、MediaInfoやExifToolsなどのオープンソースツールについて簡単に紹介します。
---

.. rubric:: 脚注

.. [#f1] (訳注) VSEは *Video Sequence Editor* の略です。
.. [#f2] (訳注) 公式のBlenderリファレンス文書は、エディターの各機能を網羅的に説明しているため、動画編集のワークフローと機能の関連がわかりにくくなっています。
