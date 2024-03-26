Workspace
=========

.. Upon opening Blender, the `splash screen <https://docs.blender.org/manual/en/dev/interface/window_system/splash.html>`_ gives you the possibility to create a Video Editing project. Choosing this option takes you immediately into the Video Editing workspace. This workspace is a smart combination of five editors: File Browser (top left), Video Sequencer: Preview (top middle), Properties (top right), Video Sequencer: Sequencer (near bottom) and Timeline (bottom). Together they provide you with all the necessary tools to edit your videos.

Blender を開くと、`splash screen <https://docs.blender.org/manual/en/dev/interface/window_system/splash.html>`_ でビデオ編集プロジェクトを作成できるようになります。このオプションを選択すると、すぐに Video Editing workspace に移動します。このワークスペースは、ファイル ブラウザ (左上)、Video Sequence Editor(VSE): Preview (中央上)、プロパティ (右上)、Video Sequence Editor(VSE): Sequencer (下あたり)、およびタイムライン (下) の 5 つのエディターをスマートに組み合わせたものです。これらを組み合わせると、ビデオの編集に必要なすべてのツールが提供されます。



.. figure:: /images/video_editing_setup_workspace.png
   :alt: The Video Editing Workspace

   図1: video editing workspace のスクリーンショット

.. As a result of your preparation for this video editing project, all of your assets (clips, images, sounds, ...) are organized in folder structure that is appropriate for your project. For example, they are organized on daily basis, per topic, per character, ... You can use the File Browser for displaying this structure and for easily adding assets to your timeline by dragging and dropping files. If you select multiple files, they will added one after the other to the timeline. You can customize (sorting, filtering, ...) the file browser, so that you have an optimal overview of your assets.

このビデオ編集プロジェクトの準備の結果、すべてのアセット (クリップ、画像、サウンドなど) がプロジェクトに適したフォルダー構造で整理されます。
たとえば、日次、トピックごと、キャラクターごとなどに整理されています。 ファイル ブラウザを使用すると、この構造を表示したり、ファイルをDrag and Dropすることでタイムラインにアセットを簡単に追加したりできます。複数のファイルを選択すると、タイムラインに順番に追加されます。ファイル ブラウザをカスタマイズ (並べ替え、フィルタリングなど) できるため、アセットの最適な概要が得られます。

.. The Sequence Editor has three view types: *Sequencer*, *Preview*, and *Sequencer & Preview* (see :doc:`Video Sequence Editor <../../../video_sequencer/index>` for more information.

Video Sequence Editor には、 *Sequencer* 、*Preview* 、および *Sequencer/Preview* の3つのビュー タイプがあります(詳細については、:doc:`Video Sequence Editor <../../../video_sequencer/index>` を参照してください)。

.. It is possible to create multiple instances of any view type in single workspace; so, the Video Sequencer occupy two areas in the workspace. You can switch easily between the Sequencer and the Preview with the :kbd:`CtrL Tab`.

1つのワークスペースで任意のビュータイプの複数のインスタンスを作成できます。したがって、 Video Sequence Editor はワークスペース内の 2 つの Area を占有します。を使用すると、:kbd:`CtrL Tab` Sequencer と Preview を簡単に切り替えることができます。

.. The Properties panel allows editing of many active data. They are organized into several categories, which can be chosen via tabs (the icons column to its left). Not all categories are relevant in the Video Sequencer. By default only the following are shown: Active Tool, Render Properties, View Layer Properties, Scene Properties, World Properties, and Texture Properties. Most of the time, you will use only the Render Properties.

[Properties] パネルでは、多くのアクティブなデータを編集できます。これらはいくつかのカテゴリに分類されており、タブ (左側のアイコン列) から選択できます。すべてのカテゴリが Video Sequence Editor に関連するわけではありません。デフォルトでは、Active Tool, Render Properties, View Layer Properties, Scene Properties, World Properties, と Texture Properties のみが表示されます。ほとんどの場合、使用するのは Render Properties のみです。

.. The built-in Video Editing workspace is very handy and it can be customized easily. Each editor area can be sized, moved, replaced or removed from the workspace. As example, an alternative workspace with auto-installed add-ons can be download from `tin2tin's github <https://github.com/tin2tin/Sequence_Editing>`_. A screenshot is provided below.

Blender標準の Video Editing Workspace は非常に便利で、簡単にカスタマイズできます。各エディタ領域は、サイズ変更、移動、置換、またはワークスペースからの削除が可能です。たとえば、アドオンが自動インストールされる代替ワークスペースは、`tin2tin's github <https://github.com/tin2tin/Sequence_Editing>`_ からダウンロードできます [#f1]_ 。スクリーンショットを以下に示します。

.. figure:: https://raw.githubusercontent.com/tin2tin/Sequence_Editing/main/Sequence_Editing.png
   :alt: A customized Video Editing Workspace

   図2: Video Editing Workspaceのカスタマイズ

.. Please, note that the Timeline editor is removed and that the Playback controls are placed in the header of the Sequencer. Several add-ons are automatically installed (e.g. Transform tools), together with some new operators (e.g. Remove Gap after ...). Last but not least, the Properties editor is also removed and the project settings are placed in the Preview sidebar, where they can easily toggled on/off with the N-key.

Timeline Editor が削除され、再生コントロールがシーケンサーのヘッダーに配置されることに注意してください。いくつかのアドオン (例: Transform ツール) が、いくつかの新しいオペレーター (例: Remove Gap after …) とともに自動的にインストールされます。最後になりましたが、Properties Editor も削除され、プロジェクト設定はプレビュー サイドバーに配置され、N キーで簡単にオン/オフを切り替えることができます。

.. rubric:: 脚注

.. [#f1] 紹介されているリポジトリ(tin2tin/Sequence_Editing)は、4年前を最後にメンテナンスされていないようです。そのため、利用しないほうが良さそうです。
