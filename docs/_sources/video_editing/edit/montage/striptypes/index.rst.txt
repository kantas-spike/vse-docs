.. _striptypes:

.. Strip Types
ストリップの種類
...........

.. figure:: /images/vse_setup_project_striptypes_strip-types.svg
   :alt: Available strip types

   図 1: 利用可能なストリップ タイプとカラー コードおよびプロパティ

..
  A strip is a sequence of images displayed as a colored horizontal bar.
  Each image occupies one frame in the timeline.
  In figure 1 the basic strip types are added with the menu :menuselection:`Add` or :kbd:`Shift-A`.
  They run from frame 1 up to frame 300.
..

ストリップは、色付きの水平バーとして表示される一連の画像です。
各画像はタイムライン内の 1 フレームを占めます。
図 1 では、基本的なストリップ タイプが [Add]メニュー または :kbd:`Shift-A`  で追加されています。
フレーム 1 からフレーム 300 まで伸びています。

.. The strip types are classified into 4 groups:
ストリップのタイプは 4 つのグループに分類されます。

   ..
    1. *Scene, Clip, Mask*: the input source is created in another Blender module
    2. *Movie, Sound, Image/Sequence*: the input source is an external file
    3. *Color, Text*: the input is created within the Sequence Editor
    4. *Adjustment Layer, Effect Strip, Transition, Fade*: the input source is another strip.
   ..
   1. *Scene, Clip, Mask*:
       入力ソースは別の Blender モジュールで作成されます
   2. *Movie, Sound, Image/Sequence*:
       入力ソースは外部ファイルです
   3. *Color, Text*:
       入力はシーケンス エディター内で作成されます。
   4. *Adjustment Layer, Effect Strip, Transition, Fade*:
       入力ソースは別のストリップです。


..
  Each strip type is uniquely color-coded.
  In figure 1, from top to bottom: Scene strip :scene:`███`,
  Clip strip :clip:`███`, Mask strip :mask:`███`, Movie strip :movie:`███`,
  Sound strip :sound:`███`, Image/Sequence strip :image:`███`,
  Color :color:`███` + selected color), and Text :text:`███`.
..

各ストリップ タイプは独自に色分けされています。
図 1 では、上から下に:
 - シーン ストリップ :scene:`███`
 - クリップ ストリップ :clip:`███`
 - マスク ストリップ :mask:`███`
 - ムービー ストリップ :movie:`███`
 - サウンド ストリップ :sound:`███`
 - 画像/シーケンス ストリップ :image:`███`
 - カラー ストリップ :color:`███` + 選択した色
 - テキスト ストリップ :text:`███`


.. _default-color:

..
  These colors are defined in the User Preferences and can be changed with the menu
  :menuselection:`Edit --> Preferences --> Themes --> Video Sequencer`.
..
これらの色はユーザー設定で定義されており、メニューの :menuselection:`Edit --> Preferences --> Themes --> Video Sequencer` で変更できます。

..
  The Group 4 strip types are *not* shown in figure 1 and will be discussed in a separate section.
  They presume the existence of one or more of the above basic strips.
..

4番目のグループ のストリップ タイプは、図 1 には示されていないため、別のセクションで説明します。
これらは、上記の基本的なストリップが 1 つ以上存在することを前提としています。

..
  Each strip has multiple Properties. Figure 1 shows the Properties of a Movie strip at the right hand side.
  This sidebar can be displayed with :menuselection:`View --> Sidebar` or shortcut key :kbd:`N`.
  All properties are organized in panels, e.g. Compositing, Transform, Crop, ect...
  Navigating these panels is explained in `Tabs & panels <https://docs.blender.org/manual/en/dev/interface/window_system/tabs_panels.html>`_.
  The top of the sidebar contains the always visible header with the icon of the strip type,
  the name of the strip, and a Mute checkbox. You can name or rename your strips here.
  If the Mute button is checked the strip will still be visible in the Sequencer but will not produce any output.
..

各ストリップには複数のプロパティがあります。

図 1 は、右側にムービー ストリップのプロパティを示しています。
この Sidebar は、 :menuselection:`View --> Sidebar`  またはショートカットキー :kbd:`N` で表示できます。

すべてのプロパティは、[Compositing], [Transform], [Crop] などのパネルにまとめられています。
これらのパネルの操作については、 `Tabs & panels <https://docs.blender.org/manual/en/dev/interface/window_system/tabs_panels.html>`_ で説明されています。

Sidebarの上部には、ストリップ タイプのアイコン、ストリップの名前、および [Mute] チェックボックスを備えた、常に表示されるヘッダーが含まれています。
ここでストリップに名前を付けたり、名前を変更したりできます。[Mute]がチェックされている場合、ストリップは Sequencer に表示されたままになりますが、出力は生成されません。

.. toctree::
   :hidden:
   :maxdepth: 2

   movie
   sound
   image
   clip
   scene
   color
   mask
   text
