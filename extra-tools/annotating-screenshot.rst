.. Annotating screenshots
スクリーンショットに注釈を付ける
**********************

.. Adding annotated figures to the Blender documentation can be a labor intensive process; especially if the figure content changes a lot, due to Blender internal development. The following text describes an optimized workflow for creating these frequently changing figures in the Blender docs. Most of the time, these figures are based upon a screenshot of some part of the Blender interface; where upon some annotation (coloring, text, arrows, labels, ...) is added.

注釈付きの図を Blender ドキュメントに追加するのは、多大な労力を要するプロセスになる場合があります。特に、Blender の内部開発により Figure の内容が大幅に変更される場合はそうです。次のテキストでは、Blender ドキュメントでこれらの頻繁に変更される図を作成するための最適化されたワークフローについて説明します。ほとんどの場合、これらの図は Blender インターフェイスの一部のスクリーンショットに基づいています。ここで、何らかの注釈 (色、テキスト、矢印、ラベルなど) が追加されます。

.. Embedding the screenshot in SVG
スクリーンショットをSVGに埋め込む
===============================

..
  1. Create a blend-file with the same name as the figure; e.g. video_editing_setup_workspace.blend. If you have a high resolution monitor, it is perhaps better to set the Edit > Preferences > Interface > Resolution Scale to a higher value (e.g. 1.5) to enhance the readability of the text.
  2. Prepare the Blender environment for the screenshot (e.g. choose workspace, resize, expand or collapse panels, ...).  With the menu Edit > Toggle Full Screen, you can hide hide the title bar where the file location of the Blend-file is displayed. Be sure that your Blender window is maximized (or remember the actual window dimensions).
  3. Take a screenshot. You can use Blender (menu Window > Save Screenshot or Save Screenshot (Editor). The second option will allow you to point to the specific editor, you want a screenshot from. You can also use a dedicated screen-grabber. Be sure that you can recreate this screenshot easily (in case you missed or the Blender UI changes and you need a new screenshot.
  4. Open your SVG paint program; e.g. Inkscape. Paste the screenshot from the clipboard as an embedded image. The overhead of this embedding is reasonable. For example, a PNG file of 105 Kb results in a SVG file of 143 Kb.
  5. Annotate the image. Because SVG is a vector format, these annotations can always be changed without having to recreate everything.
..

1. 図と同じ名前の blendファイルを作成します。例: video_editing_setup_workspace.blend。高解像度のモニターを使用している場合は、テキストの読みやすさを高めるために、[Edit] > [Preference] > [Interface] > [Resolution Scale] をより高い値 (1.5 など) に設定することをお勧めします。
2. スクリーンショット用に Blender 環境を準備します (ワークスペースの選択、パネルのサイズ変更、展開または折りたたみなど)。メニューの [Edit] > [Toggle Full Screen] を使用すると、blend ファイルのファイルの場所が表示されるタイトル バーを非表示にできます。Blender ウィンドウが最大化されていることを確認してください (または、実際のウィンドウの寸法を覚えておいてください)。
3. スクリーンショットを撮ります。Blender を使用できます ([Window]メニュー > [Save Screenshot] または [Save Screenshot (Editor)] を選択します。2 番目のオプションを使用すると、スクリーンショットを取得する特定のエディターを指定できます。専用のスクリーン グラバーを使用することもできます。このスクリーンショットは簡単に再作成できます (見逃したり、Blender UI が変更されて新しいスクリーンショットが必要になった場合に備えて)。
4. SVG ペイント プログラムを開きます。たとえば、Inkscape。クリップボードからスクリーンショットを埋め込み画像として貼り付けます。この埋め込みのオーバーヘッドは妥当です。たとえば、105 KB の PNG ファイルは、143 KB の SVG ファイルになります。
5. 画像に注釈を付けます。SVG はベクター形式であるため、これらの注釈は、すべてを再作成することなくいつでも変更できます。

.. Blender-only solution
Blender のみのソリューション
=====================

.. The basic idea of this workflow is to keep all info into one blend-file (and do all the work in Blender) in stead of dispersing the work and data into several third party programs (blender, screen grabber, graphic editor).

このワークフローの基本的な考え方は、作業とデータを複数のサードパーティ プログラム (ブレンダー、スクリーン グラバー、グラフィック エディター) に分散させるのではなく、すべての情報を 1 つのブレンド ファイルに保存する (そしてすべての作業を Blender で行う) ことです。

..
   1. Create a blend-file with the same name as the figure; e.g. video_editing_setup_workspace.blend. If you have a high resolution monitor, it is perhaps better to set the Edit > Preferences > Interface > Resolution Scale to a higher value (e.g. 1.5) to enhance the readability of the text. Set the project resolution to the size of your monitor (e.g. 1920 x 1080 or 3840 x 2160 for a 4K monitor). Otherwise, Blender will scale your screenshot, resulting in a blurry output. *Is this correct?*
   2. Prepare the Blender environment for the screenshot (e.g. choose workspace, resize, expand or collapse panels, ...).  With the menu Edit > Toggle Full Screen, you can hide hide the title bar where the file location of the Blend-file is displayed. Be sure that your Blender window is maximized (or remember the actual window dimensions).
   3. Take a screenshot with the menu Window > Save Screenshot or Save Screenshot (Editor). The second option will allow you to point to the specific editor, you want a screenshot from. Save this screenshot in a subfolder; e.g. screenshots-original. Later on, you can crop the image. You don't need a third-party screen grabber; except if you want to capture the mouse cursor or for example expanded menu-items. The problem with an external screen grabber however is that it is difficult to recreate the exact same size a second time. It is important that after the screen grab, the UI of Blender is not changed any longer (for example zoom level). *Question: is it possible to freeze the UI?*
   4. Create a new scene (for example scene-output) with the Copy Settings option (so, that the resolution is automatically set correctly).  Activate 3D view (Layout workspace) and change to the Top level view. In this scene you create the annotated figure.
   5. Add an Image as Plane (addon) with the aforementioned screenshot as source. Choose for an Emit Material Setting and a Camera Relative > Fill Plane Dimension. *Note: not sure this is the best option!*
   6. Switch to Orthographic Camera view and and adjust the Orthographic scale until the complete screenshot fits into the camera view. With the View > Layout Properties, you can enable Render Region and Crop to Render Region. With these options you can crop the image to the desired size (if you are in Camera view).
   7. Start annotating. There exists a preset Blend-file (grease-pencil-shapes.blend) that contains some sample texts and shapes, together with the appropriate materials and colors. Append this blend-file to your project and choose the needed text or shape objects (in the Objects folder).
   8. Adding text. Append a preset text-object. Press Tab and change the content. Duplicate the object, if you need more text. You can add text yourself with the 3D Text object. Remember that you are in Top view, so you have to rotate the text 90° on the X-axis. *Question: should we propose a specific font and color?*
   *Question: is there an easy way to add text within Grease Pencil? Advantage: animation is much more easy in GP*
   1.  Adding shapes. Append the desired preset shape object (rectangle, arrow-single, arrow-double, arrow-single-curved, ...). You can scale and rotate these shapes as needed. You can create your own shapes with the Grease Pencil object.

       * Add a Blanc Grease Pencil object. Switch to Draw mode and create the desired shape. If you want some artistic annotation, you can draw the strokes. Or you can use one of the preset tools (line, polyline, arc, curve, ... ). If you use one of the preset tools, don't forget to switch on the Curve Editing in Edit mode.
       * For the dashed line drawings, you need two modifiers: Simplify > Sample to generate equally distributed points in the shape and the dash-dot modifier to create the dashed line. See the predefined shapes in grease-pencil-shapes.blend for some inspiration. *Perhaps, there should be some kind of tutorial to create these shapes in GP.*
   2.  Create the final figure. Render the scene (don't forget Crop to Render Region if you only need a part of the screenshot). Save the rendered image as a .png file. Save the Blend-file.
..
1. 図と同じ名前の blend ファイルを作成します。例: video_editing_setup_workspace.blend。高解像度のモニターを使用している場合は、テキストの読みやすさを高めるために、[Editor] > [Preferences] > [Interface] > [Resolution Scale] をより高い値 (1.5 など) に設定することをお勧めします。プロジェクトの解像度をモニターのサイズに設定します (たとえば、4K モニターの場合は 1920 x 1080 または 3840 x 2160)。そうしないと、Blender がスクリーンショットを拡大縮小してしまい、出力がぼやけてしまいます。これは正しいです？
2. スクリーンショット用に Blender 環境を準備します (ワークスペースの選択、パネルのサイズ変更、展開または折りたたみなど)。メニューの [Edit] > [Toggle Full Screen] を使用すると、blend ファイルのファイルの場所が表示されるタイトル バーを非表示にできます。Blender ウィンドウが最大化されていることを確認してください (または、実際のウィンドウの寸法を覚えておいてください)。
3. メニューの [Window] > [Save Screenshot] または [Save Screenshot (Editor)] を使用してスクリーンショットを撮ります。2 番目のオプションでは、スクリーンショットを取得する特定のエディターを指定できます。このスクリーンショットをサブフォルダーに保存します。例: オリジナルのスクリーンショット。後で画像をトリミングできます。サードパーティのスクリーングラバーは必要ありません。ただし、マウス カーソルや展開されたメニュー項目などをキャプチャする場合は除きます。ただし、外部スクリーン グラバーの問題は、まったく同じサイズを 2 度目に再作成するのが難しいことです。画面を取得した後は、Blender の UI (ズーム レベルなど) が変更されないことが重要です。質問: UI をフリーズすることは可能ですか?
4. [Copy Settings] オプションを使用して新しいシーン (シーン出力など) を作成します (これにより、解像度が自動的に正しく設定されます)。3D ビュー (レイアウト ワークスペース) をアクティブにし、トップ レベル ビューに変更します。このシーンでは、注釈付きの 図 を作成します。
5. 前述のスクリーンショットをソースとして、Image as Plane (アドオン) を追加します。[Emit Material Setting] と [Camera Relative] > [Fill Plane Dimension] を選択します。注: これが最適なオプションかどうかはわかりません。
6. 正投影カメラ ビューに切り替え、完全なスクリーンショットがカメラ ビューに収まるまで正投影スケールを調整します。[View] > [Layout] プロパティ を使用すると、レンダリング領域とレンダリング領域へのトリミングを有効にすることができます。これらのオプションを使用すると、画像を希望のサイズにトリミングできます (カメラ ビューの場合)。
7. 注釈を付け始めます。いくつかのサンプル テキストと形状、および適切なマテリアルと色を含むプリセット ブレンド ファイル (grease-pencil-shapes.blend) が存在します。このブレンド ファイルをプロジェクトに追加し、必要なテキスト オブジェクトまたはシェイプ オブジェクト (Objects フォルダー内) を選択します。
8. テキストを追加します。プリセットのテキストオブジェクトを追加します。Tab キーを押して内容を変更します。さらにテキストが必要な場合は、オブジェクトを複製します。3D Text オブジェクトを使用してテキストを自分で追加できます。現在はトップ ビューなので、テキストを X 軸上で 90 度回転する必要があることに注意してください。質問: 特定のフォントと色を提案する必要がありますか? 質問: グリース ペンシル内にテキストを追加する簡単な方法はありますか? 利点: GP ではアニメーションがはるかに簡単です。
9. シェイプを追加します。目的のプリセット形状オブジェクト (長方形、単一矢印、二重矢印、単一曲線など) を追加します。必要に応じて、これらの形状を拡大縮小したり回転したりできます。グリース ペンシル オブジェクトを使用して独自の形状を作成できます。
  * Blanc Grease Pencil オブジェクトを追加します。描画モードに切り替えて、目的の形状を作成します。芸術的な注釈が必要な場合は、ストロークを描画できます。または、プリセット ツール (線分、ポリライン、円弧、曲線など) のいずれかを使用することもできます。プリセット ツールのいずれかを使用する場合は、編集モードでカーブ編集をオンにすることを忘れないでください。
  * 破線の描画には、2 つのモディファイアが必要です。形状内に均等に分布した点を生成するための [Simplify] > [Sample]と、破線を作成するための一点鎖線モディファイアです。インスピレーションを得るためには、grease-pencil-shapes.blend の事前定義された形状を参照してください。おそらく、GP でこれらの形状を作成するための何らかのチュートリアルがあるはずです。

10. 最終的な図を作成します。シーンをレンダリングします(スクリーンショットの一部のみが必要な場合は、「レンダリング領域にクロップ」を忘れないでください)。レンダリングされたイメージを .png ファイルとして保存します。Blend ファイルを保存します。

.. If you need to update this figure: open the blend-file (eventually into a new version of Blender). Re-prepare the Blender environment (step 2). Try of course, to change as little as possible. Take the screenshot (step 3). Switch to the second scene and refresh the image datablock of the image-as-plane object (underneath the Material property).

この図を更新する必要がある場合は、blend ファイルを開きます (最終的には新しいバージョンの Blender で開きます)。Blender 環境を再準備します (ステップ 2)。もちろん、できるだけ変更しないようにしてください。スクリーンショットを撮ります (ステップ 3)。2 番目のシーンに切り替えて、image-as-plane オブジェクトのイメージ データブロック (マテリアル プロパティの下) を更新します。

.. note::
   .. Some of the above steps could be done with a Python script. The problem of huge png-files from HD monitors is not solved. Can they be scaled down within Sphinx? I've tried to put Blender into a 1920 x 1080 window on a 4K monitor but that is not very practical.

   上記の手順の一部は、Python スクリプトを使用して実行できます。HD モニターからの巨大な PNG ファイルの問題は解決されていません。Sphinx 内でスケールダウンできますか? 4K モニター上の 1920 x 1080 ウィンドウに Blender を入れようとしましたが、それはあまり実用的ではありません。
