***********
用語
***********
.. The terminology about color is sometimes quite intimidating. Let's take a look at some basic concepts with the help of the well-known color picker. Did you know that Blender has five different :ref:`color pickers <blender_manual:ui-color-picker>` No? You can choose between them in the Preferences panel (Edit > Preferences > Interface). They look rather intuitive to use (see Figure 1) but already loaded with some difficult terminology. And even for this simple tool, several questions arise and trying to answer them will get you very fast into deep Blender space!

色に関する専門用語は、時には非常に恐ろしいものです。有名なカラーピッカーを使用して、いくつかの基本的な概念を見てみましょう。 Blender には 5 つの異なる :ref:`color pickers <blender_manual:ui-color-picker>` があることをご存知ですか?
[Preferences] パネル ([Edit] > [Preferences] > [Interface]) でこれらを選択できます。これらは直感的に使用できるように見えますが (図1)、すでにいくつかの難しい用語が登場します。  そして、この単純なツールであっても、いくつかの疑問が生じ、それらに答えようとすると、すぐに深い Blender の世界に入ることができます。

.. _color_picker:

.. figure:: img/color_picker.svg
   :alt: The Color picker

   図1 カラーピッカー。デフォルトのオプションが左側に表示されています。キャプションは Blender のドキュメントから引用

..
  1. Why do we need 5 of them? Is it only a matter of preference? Do they return different colors? Some color panels sure look brighter (1 vs 2 and 3 vs 4) than others. Why? In what aspect are they different?
  2. How many different colors can you select? If the area of the little white dot is one color, then it seems that not many colors can be selected. Why are there two red's in the square panel (one at the left and one at the right) and not in the circle panel? Why are some color bands small (eg. yellow) compared to others (eg. green)?
  3. Two panels use a circle and three a square shape to show all (?) the colors? Why? Also a matter of preference? And how do they relate? The color slider is sometimes placed horizontal and sometimes vertical? Any difference?
  4. When you click on the Hex button, a little warning ('Gamma corrected') appear? What on earth does this mean? Should you be worried? Better not to use Hex? And why is it only shown underneath the Hex mode?
  5. Besides, what is the meaning of all those abbreviations: RGB, HSV, HSL, Hex?  And why is HSL only mentioned once?
  6. Dragging the value sliders (H, S, ...) from left to right reveal that they go from 0 to 1. But, for some of them, you can also enter values beyond 1 but not less than 0. Why?  And what do those values mean? ...
..
1. なぜ 5 つ必要なのでしょうか?それは単なる好みの問題ですか？異なる色が返されますか?一部のカラー パネルは他のパネルよりも明るく見えます (1 対 2 および 3 対 4)。なぜ？それらはどのような点で異なりますか?
2. 何種類の色を選択できますか? 小さな白い点の領域が 1 色の場合、選択できる色はそれほど多くないようです。正方形のパネルには赤が 2 つ (左に 1 つ、右に 1 つ) あり、円パネルにはないのはなぜですか?一部のカラー バンド (例: 黄色) が他のカラー バンド (例: 緑) に比べて小さいのはなぜですか?
3. 2 つのパネルは円を使用し、3 つのパネルは正方形を使用してすべての色(?)を表示します。なぜ？これも好みの問題でしょうか？そしてそれらはどのように関係しているのでしょうか？カラースライダーは水平に配置される場合もあれば、垂直に配置される場合もあります。違いはありますか？
4. Hex ボタンをクリックすると、小さな警告 (「ガンマ補正済み」) が表示されます。これは一体何を意味するのでしょうか？心配する必要がありますか？ Hexは使わない方が良いでしょうか？そして、なぜこれが Hex モードの下にのみ表示されるのでしょうか?
5. さらに、RGB、HSV、HSL、Hex などの略語にはどのような意味があるのでしょうか?そして、なぜ HSL は 1 回しか言及されないのでしょうか?
6. 値スライダー (H、S、…) を左から右にドラッグすると、0 から 1 まで変化することがわかります。ただし、一部の値については、1 を超え、0 未満ではない値を入力することもできます。なぜでしょうか。そしてそれらの値は何を意味するのでしょうか? …

.. A lot of questions! Some look trivial and may be far fetched but searching for the answer will provide you with some profound insight into color management and also a few really ugly things. Let's focus on only one question in this post. How can you recreate these panels in Blender? Then, it will be apparent how they differ. That shouldn't be too difficult: a plane or circle with an appropriate material. Or so, you think!

質問がたくさん！些細なように見えたり、突飛なものもあるかもしれませんが、答えを探すと、カラー管理についての深い洞察が得られ、また、いくつかの非常に醜い事柄も得られます。この投稿では 1 つの質問だけに焦点を当てましょう。 Blender でこれらのパネルを再作成するにはどうすればよいでしょうか?そうすれば、それらがどのように異なるかが明らかになるでしょう。それはそれほど難しいことではありません。適切なマテリアルを使用して平面または円を作成します。そう思いますか！

.. Start Blender. Delete all objects, set the World Background color to black, switch to top view and add 2 circle and 3 plane meshes of 1 unit each. Position them next to each other; the exact location doesn't matter. To get the colors, you need a five materials. Switch to the Shading workspace and create the materials. You could name them according to the cryptic captions of figure 1.

ブレンダーを起動します。すべてのオブジェクトを削除し、ワールドの背景色を黒に設定し、上面図に切り替えて、それぞれ 1 単位の 2 つの円メッシュと 3 つの平面メッシュを追加します。それらを隣り合わせて配置します。正確な場所は関係ありません。色を得るには5つの素材が必要です。シェーディング ワークスペースに切り替えて、マテリアルを作成します。図 1 の不可解なキャプションに従って、それらに名前を付けることができます。

.. note::
   .. You could download a `blend-file <files/terminology.blend>`_ with these materials already set-up.
   これらのマテリアルがすでにセットアップされている `blend-file <files/terminology.blend>`_ をダウンロードできます。

.. Let's begin with the first square panel (square HV+S). The cryptic name suggests that the parameters H (Hue) and V (Value) are used to create the color panel and that the third parameter S (Saturation) is set by the separate horizontal slider. In the HSV-color model, you need all three values to define a unique color. From the sliders at the bottom you know that these parameters could vary between 0 and 1. Because your plane also has a width and height of 1 unit, the X and Y coordinates of each point in this plane will also vary between 0 and 1, but only if (0,0) is at the bottom-left of the square. Is there a shading node that can give you these coordinates?

最初の正方形のパネル (正方形 HV+S) から始めましょう。この不可解な名前は、パラメータ H (色相) と V (値) がカラー パネルの作成に使用され、3 番目のパラメータ S (彩度) が別の水平スライダによって設定されることを示唆しています。 HSV カラー モデルでは、一意の色を定義するには 3 つの値すべてが必要です。下部のスライダーから、これらのパラメーターが 0 と 1 の間で変化することがわかります。平面の幅と高さも 1 単位であるため、この平面内の各点の X 座標と Y 座標も 0 と 1 の間で変化します。ただし、(0,0) が正方形の左下にある場合に限ります。これらの座標を提供できるシェーディング ノードはありますか?

.. Probably you should search in the Input group nodes (because this node should give you some input). It turns out that there are a quite a few nodes that could provide you with this info: the `Geometry node <https://docs.blender.org/manual/en/latest/render/shader_nodes/input/geometry.html>`_) and the `Texture Coordinate node <https://docs.blender.org/manual/en/dev/render/shader_nodes/input/texture_coordinate.html>`_. The geometry node has (in this case) the disadvantage that it outputs world space coordinates. Moving the object in 3D-space will thus this change these coordinates, which is undesirable. You need something in the range (0 - 1), no matter where the object is located in 3D space. The Texture Coordinate node is what you're looking for. This node outputs for each shading point (this is a point on a surface of our object that could be hit by a light ray) an output vector with the X, Y and Z coordinates of that shading point, e.g. (0.4, 0.3, 0). Moreover, if you choose for the generated texture coordinate, these coordinates have an origin of (0,0,0) at the left-bottom of the shape; again, exactly what you want.  With the `Separate XYZ node <https://docs.blender.org/manual/en/latest/render/shader_nodes/converter/combine_separate.html>`_ you can split this vector into the individual X, Y and Z coordinates.

おそらく、Input グループ ノードを検索する必要があります (このノードから何らかの入力が得られるはずです)。この情報を提供できるノードは、 `Geometry node <https://docs.blender.org/manual/en/latest/render/shader_nodes/input/geometry.html>`_ と `Texture Coordinate node <https://docs.blender.org/manual/en/dev/render/shader_nodes/input/texture_coordinate.html>`_ がかなりの数あることがわかりました。ジオメトリ ノードには (この場合) ワールド空間座標を出力するという欠点があります。したがって、3D 空間内でオブジェクトを移動すると、これらの座標が変更されるため、望ましくないことになります。オブジェクトが 3D 空間のどこにあるかに関係なく、範囲 (0 ～ 1) 内の値が必要です。探しているのはテクスチャ座標ノードです。このノードは、各シェーディング ポイント (これは、光線が当たる可能性のあるオブジェクトの表面上の点) に対して、そのシェーディング ポイントの X、Y、Z 座標を含む出力ベクトル (0.4、0.3、0 など) を出力します。さらに、生成されたテクスチャ座標を選択した場合、これらの座標の原点は形状の左下に (0,0,0) になります。繰り返しますが、まさにあなたが望むものです。 `Separate XYZ node <https://docs.blender.org/manual/en/latest/render/shader_nodes/converter/combine_separate.html>`_ ノードを使用すると、このベクトルを個別の X、Y、Z 座標に分割できます。

.. Then, how do you make colors out of these numbers? Your first guess could be to use the Combine RGB node. This node accepts values for the 3 color channels and creates a mixed color from it. Unfortunately, you need three values for the full spectrum and our Z-coordinate is always zero because we paint the colors on a 2D- plane. This Combine RGB node could well work with a cube, which has three dimensions. Besides, the color panel isn't simply a kind of gradient of one color going from 0 to 1. The red color, for example, occurs both at the left and right side of the square. Upon closer look, the color panel resembles the Hue color card examples; see for example `Wikipedia <https://en.wikipedia.org/wiki/Hue>`_. Maybe you could use the `Hue/Saturation node <https://docs.blender.org/manual/en/dev/render/shader_nodes/color/hue_saturation.html>`_. Normally this node is used to change the hue, saturation or value of a color or image.

では、これらの数字からどのように色を作るのでしょうか?最初に考えられるのは、Combine RGB ノードを使用することです。このノードは 3 つのカラー チャネルの値を受け入れ、そこから混合カラーを作成します。残念ながら、スペクトル全体に 3 つの値が必要ですが、色を 2D 平面上にペイントするため、Z 座標は常に 0 になります。この Combine RGB ノードは、3 次元の立方体でもうまく機能します。さらに、カラー パネルは、1 つの色の単純な 0 から 1 へのグラデーションではありません。たとえば、赤色は正方形の左側と右側の両方に現れます。よく見ると、カラー パネルは Hue カラー カードの例に似ています。たとえば、 `Wikipedia <https://en.wikipedia.org/wiki/Hue>`_ を参照してください。 `Hue/Saturation node <https://docs.blender.org/manual/en/dev/render/shader_nodes/color/hue_saturation.html>`_ を使用できるかもしれません。通常、このノードは、色または画像の色相、彩度、または値を変更するために使用されます。

.. figure:: img/color_picker.png
   :alt: Shading nodes for recreating the color picker

   図2 カラー ピッカーの (正方形 HV+S) カラー パネルを再作成するためのシェーディング ノード

.. Note that we use the color cyan as input color. According to the documentation, the Hue parameter specifies the hue *rotation* of the image. 360° are mapped to (0 to 1). The hue shifts of 0 (-180°) and 1 (+180°) have the same result. So, the Cyan color which is at about 180° will be shifted -180° and therefore becomes zero or red at the texture coordinate 0 and again to red (cyan + 180° = 360°) at texture coordinate 1.

シアン色を入力色として使用することに注意してください。ドキュメントによると、Hue パラメータは画像の色相回転を指定します。 360°は (0 ～ 1) にマッピングされます。色相シフト 0 (-180°) と 1 (+180°) は同じ結果になります。したがって、約 180° にあるシアン色は -180° シフトされるため、テクスチャ座標 0 ではゼロまたは赤になり、テクスチャ座標 1 では再び赤 (シアン + 180° = 360°) になります。

.. The panel is a combination of Hue and Value, with the Saturation parameter in a separate slider (Square HV + S). The Value parameter is represented by the Y axis, which runs from 1 (top) to 0 (bottom). So, you can use the Y socket to plug into the Value parameter of the Hue-Saturation-Value node.

このパネルは色相と値の組み合わせであり、彩度パラメータは別のスライダー (Square HV + S) にあります。 Value パラメーターは Y 軸で表され、1 (上) から 0 (下) まで続きます。したがって、Y ソケットを使用して、Hue-Saturation-Value ノードの Value パラメーターに接続できます。

.. Why do you need the Gamma node? Human vision is not linear. Doubling the light intensity will not necessarily double the perceived light intensity. We are much more sensitive in the dark regions than in the light regions. Slight increments of the light energy in the shadow regions will be much more noticeable than in the lighter regions. The Gamma node takes as input a color and applies a power function; eg. x^power to it. The exponent is called gamma.

ガンマ ノードが必要な理由は何ですか? 人間の視覚は直線的ではありません。光の強度を 2 倍にしても、知覚される光の強度が必ずしも 2 倍になるわけではありません。私たちは明るい領域よりも暗い領域の方がはるかに敏感です。影の領域の光エネルギーのわずかな増加は、明るい領域よりもはるかに目立ちます。
Gamma ノードは入力として色を受け取り、べき乗関数を適用します。(例: x^power) 指数はガンマと呼ばれます。


.. figure:: img/color_picker_gamma_correction.svg
   :alt: color picker

   .. Figure 3: The original color picker (left), from node tree (above) with Gamma correction (center) and without Gamma correction (right).
   図3 ガンマ補正あり (中央) とガンマ補正なし (右) のノード ツリー (上) の元のカラー ピッカー (左)。

.. The panel in the middle of figure 3 is with gamma encoding. The 'gamma' exponent is set to 2.2, which is defined in the sRGB color model. So, an input intensity of 0.25 is transformed to a output intensity of 0.25\ :sup:`2.2` = 0.047. The result is thus darker (closer to zero); which is very obvious if you compare the two right-most panels of figure 3. But the darkening occurs predominantly in the shadows and midtones.

図3 の中央のパネルはガンマ エンコーディングを使用しています。 「ガンマ」指数は 2.2 に設定されており、これは sRGB カラー モデルで定義されています。したがって、0.25 の入力強度は 0.25 2.2 = 0.047の出力強度に変換されます。したがって、結果はより暗くなります (ゼロに近づきます)。これは、図 3 の右端の 2 つのパネルを比較すると非常に明白です。しかし、暗くなるのは主にシャドウと中間調で発生します。

.. csv-table:: 表1: ガンマ関数
   :header: "x", "x\ :sup:`2.2`"
   :widths: 20, 20
   :align: center

   0.000, 	0.000
   0.250, 	0.047
   0.500, 	0.218
   0.750, 	0.531
   1.000, 	1.000


.. The material for the Square (HS + V) and the Square (SV + H) color picker is very similar as the one from fig. 2. You have to connect the X and Y coordinates from the plane with the HS or the SV parameters of the Hue Saturation Value node. In figure 1, a blueish color is selected. Search for the little white dot in the different color panels. It is known by the name "Iceberg blue" and has the following specifications, according to the `list of colors at Wikipedia <https://en.wikipedia.org/wiki/Lists_of_colors>`_. Note that we have selected this color also in the Hue-Saturation-Value node. See also Table 2.

スクエア (HS + V) およびスクエア (SV + H) カラー ピッカーのマテリアルは、図2と非常によく似ています。 平面の X 座標と Y 座標を、Hue Saturation Value ノードの HS または SV パラメータに接続する必要があります。図1 では、青みがかった色が選択されています。さまざまな色のパネルで小さな白い点を探してください。 「アイスバーグブルー」という名前で知られており、 `list of colors at Wikipedia <https://en.wikipedia.org/wiki/Lists_of_colors>`_ によると以下の仕様となっています。この色は Hue-Saturation-Value ノードでも選択していることに注意してください。表 2 も参照してください。

.. csv-table:: 表 2: Iceberg Blue の色の 16 進数、RGB、HSV、および HSL の仕様
   :header: "Hex", "Red", "Green", "Blue", "Hue (HSV/HSL)", "Saturation (HSL)", "Lightness (HSL)", "Saturation (HSV)", "Value (HSV)"
   :widths: 20, 20, 20, 20, 20, 20, 20, 20, 20
   :align: center

   "#71A6D2", "44%", "65%", "82%", "207°", "52%", "63%", "46%", "82%"

**Additive color mix**
  .. You've certainly heard that colors are additive in the RGB color space. What does this mean? You can experience it yourself by recreating the additive color mix diagram in Blender.
  RGB 色空間では色が加法であることを聞いたことがあるでしょう。これはどういう意味ですか？ Blender で加法混色図を再作成することで、実際に体験することができます。

  .. The easiest solution is to create three spot lights. So, start Blender, delete the default cube and the light. Switch to top view; add three lights of type spotlight and a plane.
  最も簡単な解決策は、3 つのスポット ライトを作成することです。そこで、Blender を起動し、デフォルトの立方体とライトを削除します。平面図に切り替えます。スポットライト タイプのライト 3 つと平面を追加します。

  ..
     1. Switch to top view. This is not really essential but it makes your life much easier to get a spot light projection as a perfect circle.
     2. Add three lights of type spot. Position them at location: Red (0, -0.25, 1), Green (-0.5, 0.5,1) and blue (0.5, 0.5, 1). Select the appropriate color   and eventually Power (1000 W) and Spot Shape Size (75°).
     3. Switch to render preview. Are the colored circles visible? NO, because there is no surface to 'shine' on.
     4. Add a plane at location (0,0,0) with the appropriate size. The colored circles become visible.
     5. You need also to position the camera at location (0,0, 10) and change the view to camera view (Alt+Ctrl+0). Then you can render the image.
  ..
  1. 平面図に切り替えます。これは実際には必須ではありませんが、スポット ライトを完全な円として投影するのがはるかに簡単になります。
  2. スポット タイプのライトを 3 つ追加します。それらを次の場所に配置します: 赤 (0、-0.25、1)、緑 (-0.5、0.5、1)、青 (0.5、0.5、1)。適切な色を選択し、最終的に出力 (1000 W) とスポット形状サイズ (75°) を選択します。
  3. レンダリング プレビューに切り替えます。色付きの円が表示されますか?いいえ、「輝く」表面がないからです。
  4. 位置 (0,0,0) に適切なサイズの平面を追加します。色付きの円が表示されます。
  5. また、カメラを位置 (0,0, 10) に配置し、ビューをカメラ ビューに変更する (Alt+Ctrl+0) 必要もあります。その後、画像をレンダリングできます。


.. figure:: img/additive_color_mix_3_spots_render.png
   :alt: Additive color mix

   図3 3 つのスポットライトの加法混色の Evee レンダリング。

.. Figure 3 shows a nice additive color mix diagram. Note, however the status bar with extra info concerning the red color (obtained by Right-clicking on the red circle in the render preview).
図 3 は、優れた加法混色図を示しています。ただし、ステータス バーには赤色に関する追加情報が含まれていることに注意してください (レンダリング プレビューで赤い円を右クリックすると表示されます)。
