#############
Video Editing
#############

.. toctree::
   :hidden:

   setup/index
   edit/index
   render/index

.. _video-editing:

.. The Video Editing documentation is split into 3 chapters, representing a typical workflow in a video editing project: :red:`(1)` Setup, :red:`(2)` Edit and :red:`(3)` Render. You can think of these phases also as : pre-editing, editing and post-editing.

この ビデオ編集ドキュメントは 3つの章に分かれており、ビデオ編集プロジェクトの一般的なワークフローを表しています:

- :red:`(1)` セットアップ
- :red:`(2)` 編集
- :red:`(3)` レンダリング

これらのフェーズは、pre-editing、editing そして post-editing と考えることもできます。

.. Before even starting to edit a single video, you need to :red:`(1)` setup your :blue:`(1.1)` Work Environment and your specific :blue:`(1.2)` Project. Setting up your work environment includes: :green:`(1.1.1)` Customize the Video Editing Workspace, :green:`(1.1.2)` Install some Add-ons, :green:`(1.1.3)` Manage your User Preferences, and :green:`(1.1.4)` Tweak the Proxies & Cache system.

:red:`(1)` セットアップ
  単一のビデオの編集を開始する前に、 以下のセットアップが必要です。

  -  :blue:`(1.1)` 作業環境
  -  :blue:`(1.2)` 特定のプロジェクト

  :blue:`(1.1)` 作業環境
    作業環境のセットアップには次のものが含まれます:

    - :green:`(1.1.1)` ビデオ編集ワークスペースのカスタマイズ
    - :green:`(1.1.2)` いくつかのアドオンのインストール
    - :green:`(1.1.3)` ユーザー設定の管理
    - :green:`(1.1.4)` プロキシとキャッシュシステムの調整。

  .. A typical :blue:`(1.2)` project contains hundreds of files. Setting up a logical and comprehensible :green:`(1.2.1)` directory structure and appropriate :green:`(1.2.2)` Project Settings will improve your workflow. Then you can :green:`(1.2.3)` Import your footage.

  :blue:`(1.2)` 特定のプロジェクト
    一般的なプロジェクトには数百のファイルが含まれています。

    - :green:`(1.2.1)` 論理的でわかりやすいディレクトリ構造
    - :green:`(1.2.2)` 適切なプロジェクト設定のセットアップ (これにより、ワークフローが改善されます。)
    - :green:`(1.2.3)` 映像のインポート

  .. The :red:`(2)` Editing phase start with the :blue:`(2.1)` montage of the final video, e.g. :green:`(2.1.1)` adding, :green:`(2.1.2)` selecting, :green:`(2.1.3)` splitting, :green:`(2.1.4)` moving, :green:`(2.1.5 )` trimming, :green:`(2.1.6)` grouping, and :green:`(2.1.7)` deleting strips. An extensive description of all available strip types is included in :green:`(2.1.1)`. When the rough montage is done, you can add some :blue:`(2.2)` effects such as transition and fade but also more advanced animation effects, including speeding and masking. This will give you a semi-final timeline. Then, you start :blue:`(2.3)` color grading and :blue:`(2.4)` editing the sound, although some authors start with the sound much earlier (for example when editing a music video).

:red:`(2)` 編集
  編集フェーズは、以下から構成されます。

  - :blue:`(2.1)` ビデオのモンタージュ

      - :green:`(2.1.1)` 追加
      - :green:`(2.1.2)` 選択
      - :green:`(2.1.3)` 分割
      - :green:`(2.1.4)` 移動
      - :green:`(2.1.5)` トリミング
      - :green:`(2.1.6)` グループ化
      - :green:`(2.1.7)` ストリップの削除

  利用可能なすべてのストリップ タイプの詳細な説明は :doc:`ストリップの種類 </video_editing/edit/montage/striptypes/index>` に含まれています。

  ラフなモンタージュが完了したら、以下を開始します。

  - :blue:`(2.2)` エフェクトの追加
     トランジションやフェードなどのいくつかの。スピードやマスキングなどのより高度なアニメーション エフェクトも追加できます。これにより、完成直前のタイムラインが表示されます。
  - :blue:`(2.3)` カラー グレーディング(Color grading)
     (訳注) 映像の色彩を補正や、作品のトーンやルックを設定する作業 (参照: `Color grading - Wikipedia <https://en.wikipedia.org/wiki/Color_grading>`_)
  - :blue:`(2.4)` サウンドの編集
      ただし、作成者によっては、もっと早くサウンドから始める場合もあります。 例 ミュージック ビデオの編集時など。

  .. When the editing is complete, you can start :red:`(3)` rendering the project. First, you have to :blue:`(3.1)` choose your codec and probably do some :blue:`(3.2)` post-processing in the compositor or FFMPEG. Sometimes you need subtitles.

:red:`(3)` レンダリング
  編集が完了したら、プロジェクトのレンダリングを開始できます。

    - :blue:`(3.1)` コーデックの選択
    - :blue:`(3.2)` コンポジターまたは FFMPEG を使った post-processing (字幕が必要な場合もあります。)

.. Please note that there is also a separate chapter about the :doc:`Video Sequence Editor </video_sequencer/index>` . There, you can find detailed info about basic timeline operations such as moving, zooming, and navigating the timeline. Also, in a separate chapter are some :doc:`Extra Tools </extra-tools/index>`. You may need them while editing: some useful Python or FFMPEG scripts, and info about ExifTools and MediaInfo.

:doc:`Video Sequence Editor </video_sequencer/index>` に関する別の章もあることに注意してください。そこでは、タイムラインの移動、ズーム、ナビゲーションなどの基本的なタイムライン操作に関する詳細情報を見つけることができます。また、別の章では、いくつかの :doc:`Extra Tools </extra-tools/index>` について説明します。編集中に必要になるかもしれない、いくつかの便利な Python または FFMPEG スクリプト、ExifTools および MediaInfo に関する情報です。
