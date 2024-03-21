#####################
Video Sequence Editor
#####################

.. _video-sequence-editor:

.. Blender is a versatile software used for modeling, sculpting, 2D drawing, animation, and video editing. Most of the work is done in so-called editors: tools for viewing and modifying your work through a specific part of Blender.

Blenderは多機能なソフトウェアで、モデリング、スカルプティング、2Dドローイング、アニメーションや動画編集に利用されます。
多くの作業は、いわゆるエディターで行います。エディターとは、Blenderの特定の領域に、あなたの作品を表示・変更するためのツールです。

.. There are a couple of editors that can manage video: the `Compositor <https://docs.blender.org/manual/en/dev/editors/compositor.html>`_, the `Movie Clip Editor <https://docs.blender.org/manual/en/dev/editors/clip/index.html>`_, the `Image Editor <https://docs.blender.org/manual/en/dev/editors/image/index.html>`_ (only for still images) and the Video Sequencer. Every editor has a Editor Type selector in the top-left corner (see figure 1). This chapter describes only the Video Sequence Editor (VSE), sometimes shortened to “Sequencer”.

動画を操作できるエディターがいくつかあります。`Compositor <https://docs.blender.org/manual/en/dev/editors/compositor.html>`_ 、`Movie Clip Editor <https://docs.blender.org/manual/en/dev/editors/clip/index.html>`_, the `Image Editor <https://docs.blender.org/manual/en/dev/editors/image/index.html>`_ (静止画専用)、そして Video Sequencer です。

全てのエディターは、左上のコーナーに、Editor Type Selector を持っています(参照 図2)。
この章では、Video Sequence Editor (VSE) ("Sequencer" とも略される) についてのみ説明します。

.. note::
   .. It is not always obvious whether to describe something in the Video Sequencer section or in the Video Editing section. We try to apply the following rule: Anything that comes down to how to move around the editor(view menu, overlays, display modes, ...) is described in the Editor section. Anything that involves working with the editors data (e.g. strips in case of the VSE) will go into the video editing section. For example, selecting strips is described in the Video Editing section, while zooming in on the timeline is covered in the Editor section.

   Video Sequencerセクションに書くべきか、Video Editingセクションに書くべきか、いつも明らかなわけではありません。以下のルールを適用しようとします。

   - エディター内の操作に関するもの(ビューメニュー、オーバーレイ、ディスプレイモード...)はVideo Sequence Editorセクションで説明します。
   - エディターデータ(例えば、VSEの場合はストリップ)の操作に関わるものは、Vide Editingセクションで説明します。

   例えば、ストリップの選択は、Video Editingセクションに記載し、一方、タイムライン上でのズームはVideo Sequence Editorセクションで扱います。

.. With the View Type selector (see figure 1; top left) you can choose if the Video Sequence Editor contains only the Sequencer or only the Preview or both.

View Type Selector(参照 図1)を使えば、Video Seuqence Editorの構成を、Sequencerのみ、Previewのみ、Sequencer/Previewの両方を選択できます。



.. figure:: /images/editors_vse_view_types.svg
   :alt: View types

   図1: Video Sequence Editorの 3つのビュータイプ



.. Note that any area within the Blender main window can contain any Editor and that the same Editor can occur multiple times within the main window. So, theoretically, you can rebuild the combined Sequencer/Preview, starting from an empty workspace and placing two Video Sequence Editors on top of each other. The bottom editor has View Type Sequencer and the top one has type Preview.

Blender のメインウィンドウ内のどのエリアにもエディターを含めることができ、同じエディターをメインウィンドウ内に複数表示できることに注意してください。したがって、理論的には、空のワークスペースから開始して、2つのVideo Sequence Editorを上下に配置 [#f1]_ することで、View Type の Sequencer/Preview の構成を再構築できます。その場合、下部エディターの View Typeは Sequencer で、上部エディターの View TypeはPreviewになります。

.. The VSE is composed of multiple areas (see figure 2). They are described in more detail in the next sections. Figure 2 shows the combined view *Sequencer/Preview*. You can select this view with the View Type selector. This view can contain the following areas:


VSEは複数のリージョン [#f2]_ から構成されます(参照 図2)。これらのリージョンについては、次のセクションで詳細を説明します。
図2は、*Sequencer*/*Preview* が結合されビューになります。
View Type Selectorでこのビューを選択できます。このビューは以下のリージョンを含みます。


.. figure:: /images/editors_vse_overview.svg
   :alt: Main view of Sequencer

   図2: Sequence Editor メインビュー: Header (赤), Preview (黄), Sequencer (ブルー), Properties (グレー), パネルとタブ (黄色枠線と矢印), Toolbar (パープル)



.. - Sequencer: area for the montage of the strips.
- Sequencer: ストリップのモンタージュ用のエリア [#f4]_
.. - Properties: shows the properties of the active strip. Is divided into panels and tabs. Toggle on or off with :kbd:`N` key.
- Properties: アクティブストリップのプロパティーを表示します。プロパティーはパネルとタブで分割されています。:kbd:`N` キーで表示非表示を切替えます [#f3]_
.. - Toolbar: collection of icons. Clicking the icons will perform an operation on the selected strips in the sequencer. Toggle on or off with :kbd:`T` key.
- Toolbar: アイコンの一覧。 アイコンをクリックすると、Sequencer内の選択したストリップを操作できます。:kbd:`T`キーで表示非表示を切替えます。
.. - Preview: shows the output of the sequencer at the time of the playhead.
- Preview: プレイヘッドが指し示す時刻のSequencerの内容を表示します。 [#f5]_
.. - Header: with the menu and buttons. This header changes slightly depending on the selected view (see below).
- Header: メニューとボタンを持ちます。 ヘッダーは選択されているビューによって若干内容が変わります。 (以降の文書を参照).


.. toctree::
   :hidden:

   sequencer/index
   preview/index
   sequencer&preview/index


.. rubric:: 脚注

.. [#f1] (訳注) Video Editing ワークスペースは、実際に上下2つのエリアにそれぞれVSEをVideo Sequence Editor配置しています。
.. [#f2] (訳注) Vエディター内の名前のつけられた領域は、リージョン(region)と呼ばれます。
.. [#f4] (訳注) 厳密にはメインリージョンの上半分の領域になります。
.. [#f3] (訳注) :kbd:`N` キーで表示される右端のリージョン(region)は、サイドバーと呼ばれます。サイドバーはタブで分類され、各タブにはオブジェクトやエディター自身の設定を行うパネルがあります。
.. [#f5] (訳注) 厳密にはメインリージョンの下半分の領域になります。
