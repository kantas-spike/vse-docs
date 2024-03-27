Workspace
=========

.. Upon opening Blender, the `splash screen <https://docs.blender.org/manual/en/dev/interface/window_system/splash.html>`_ gives you the possibility to create a Video Editing project. Choosing this option takes you immediately into the Video Editing workspace. This workspace is a smart combination of five editors: File Browser (top left), Video Sequencer: Preview (top middle), Properties (top right), Video Sequencer: Sequencer (near bottom) and Timeline (bottom). Together they provide you with all the necessary tools to edit your videos.

Blender を開くと、`splash screen <https://docs.blender.org/manual/en/dev/interface/window_system/splash.html>`_  [#f2]_ で [Video Editing] を選択すると、ビデオ編集プロジェクトを作成できるようになります。

.. figure:: /images/video_editing_setup_splash_screen.svg
   :alt: Splash Screen
   :align: center
   :scale: 60%

   図1: Splash Screen

また、`splash screen` が表示されない場合は、[File]メニュー > [New] > [Video Editing] からもビデオ編集プロジェクトを作成できます。

.. figure:: /images/video_editing_setup_new_menu.svg
   :alt: File > New
   :align: center
   :scale: 60%

   図2: [File]メニュー > [New] > [Video Editing]

`Video Editing` を選択すると、すぐに Video Editing workspace に移動します。このワークスペースは、以下の5つのエディターをスマートに組み合わせたものです。これらを組み合わせると、ビデオの編集に必要なすべてのツールが提供されます。

- 図3-(1) File Browser
- 図3-(2) Video Sequence Editor: Preview
- 図3-(3) Video Sequence Editor: Sequencer
- 図3-(4) Properties
- 図3-(5) Timeline


.. figure:: /images/video_editing_setup_workspace.png
   :alt: The Video Editing Workspace

   図3: video editing workspace のスクリーンショット

.. As a result of your preparation for this video editing project, all of your assets (clips, images, sounds, ...) are organized in folder structure that is appropriate for your project. For example, they are organized on daily basis, per topic, per character, ... You can use the File Browser for displaying this structure and for easily adding assets to your timeline by dragging and dropping files. If you select multiple files, they will added one after the other to the timeline. You can customize (sorting, filtering, ...) the file browser, so that you have an optimal overview of your assets.

このビデオ編集プロジェクトの準備の結果、すべてのアセット (クリップ、画像、サウンドなど) がプロジェクトに適したフォルダー構造で整理されます。
たとえば、日次、トピックごと、キャラクターごとなどに整理されています (参照 :doc:`Directory structure </video_editing/setup/directory-structure>`)。

File Browser を使用すると、この構造を表示したり、ファイルを ドラッグ&ドロップ することで Sequencer のタイムラインにアセットを簡単に追加したりできます。複数のファイルを選択すると、タイムラインに順番に追加されます。File Browserをカスタマイズ (並べ替え、フィルタリングなど) できるため、アセットの最適な概要が得られます。

.. The Sequence Editor has three view types: *Sequencer*, *Preview*, and *Sequencer & Preview* (see :doc:`Video Sequence Editor <../../../video_sequencer/index>` for more information.

Video Sequence Editor には、 *Sequencer* 、*Preview* 、および *Sequencer/Preview* の3つのビュー タイプがあります(詳細については、:doc:`Video Sequence Editor </video_sequencer/index>` を参照してください)。

.. It is possible to create multiple instances of any view type in single workspace; so, the Video Sequencer occupy two areas in the workspace. You can switch easily between the Sequencer and the Preview with the :kbd:`CtrL Tab`.

1つのワークスペースで任意のビュータイプの複数のインスタンスを作成できます。したがって、 Video Sequence Editor はワークスペース内の 2 つの 領域(Area) を占有します。 :kbd:`CtrL-Tab` を使用すると、 Sequencer と Preview を簡単に切り替えることができます。

.. The Properties panel allows editing of many active data. They are organized into several categories, which can be chosen via tabs (the icons column to its left). Not all categories are relevant in the Video Sequencer. By default only the following are shown: Active Tool, Render Properties, View Layer Properties, Scene Properties, World Properties, and Texture Properties. Most of the time, you will use only the Render Properties.

Properties Editor では、多くのアクティブなデータを編集できます。これらはいくつかのカテゴリに分類されており、タブ (左側のアイコン列) から選択できます。すべてのカテゴリが Video Sequence Editor に関連するわけではありません。デフォルトでは、Active Tool, Render Properties, Output Properties, View Layer Properties, Scene Properties, World Properties, Collection Properties と Texture Properties のみが表示されます。ほとんどの場合、使用するのは Render Properties のみです。

.. The built-in Video Editing workspace is very handy and it can be customized easily. Each editor area can be sized, moved, replaced or removed from the workspace. As example, an alternative workspace with auto-installed add-ons can be download from `tin2tin's github <https://github.com/tin2tin/Sequence_Editing>`_. A screenshot is provided below.


サードパーティ アドオンの代替ワークスペースの例
----

.. warning::
  (訳注) ここで紹介されているアドオン `tin2tin's github <https://github.com/tin2tin/Sequence_Editing>`_ は、4年前を最後にメンテナンスされていないようです。そのため、アドオンは利用はせずに、あくまで参考情報としてください。


Blender標準の Video Editing Workspace は非常に便利で、簡単にカスタマイズできます。各エディタ領域は、サイズ変更、移動、置換、またはワークスペースからの削除が可能です。たとえば、`tin2tin's github <https://github.com/tin2tin/Sequence_Editing>`_ からダウンロードできるアドオンにより自動インストールされる代替ワークスペースのスクリーンショットを以下に示します。

.. figure:: https://raw.githubusercontent.com/tin2tin/Sequence_Editing/main/Sequence_Editing.png
   :alt: A customized Video Editing Workspace

   図4: Video Editing Workspaceのカスタマイズ

.. Please, note that the Timeline editor is removed and that the Playback controls are placed in the header of the Sequencer. Several add-ons are automatically installed (e.g. Transform tools), together with some new operators (e.g. Remove Gap after ...). Last but not least, the Properties editor is also removed and the project settings are placed in the Preview sidebar, where they can easily toggled on/off with the N-key.

Timeline Editor が削除され、再生コントロールがシーケンサーのヘッダーに配置されることに注意してください。いくつかのアドオン (例: Transform ツール) が、いくつかの新しいオペレーター (例: Remove Gap after …) とともに自動的にインストールされます。最後になりましたが、Properties Editor も削除され、プロジェクト設定は Preview の Sidebar に配置され、N キーで簡単にオン/オフを切り替えることができます。

.. rubric:: 訳注

.. [#f2] スプラッシュスクリーンが表示されない場合は、[Edit]メニュー > [Preferences] > [interface] > [Display] の [Splash Screen]チェックボックスを有効にすると表示できます。


