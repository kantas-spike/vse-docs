Sidebar
--------
.. The sidebar of the Preview can be toggled with the menu :menuselection:`View --> Sidebar` or with the shortcut :kbd:`N`. You can select one of three tabs: Tool, View or Metadata. Figure 1 shows the side bar of the Preview, but also the side bar of the sequencer. In the Preview side bar, the View tab is activated and all panels are expanded. The Safe Areas are enabled and an Annotation is added.

Preview の Sidebarは、[View]メニュー > [Sidebar] または ショートカット shortcut :kbd:`N` を使用して切り替えることができます。
[Tool]、[View]、または [Metadata] の 3 つのタブのいずれかを選択できます。図1 は、Preview のSidebarだけでなく、Sequencerの Sidebarも示しています。PreviewのSidebarで、[View] タブがアクティブになり、すべてのパネルが展開されます。Safe領域が有効になっており、Annotaiomも追加されています。

.. figure:: /images/editors_vse_preview_sidebar-overview.svg
   :alt: Sidebar overview


   図1: Video Sequence Editor の Preview と Sequencer用 Sidebar

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       View Settings
   **Context**:    Video Sequence Editor > Preview
   **Location**:   Sidebar > View
   =============   ==========================================================================



.. figure:: /images/editors_vse_preview_sidebar-view-settings.png
   :alt: Side bar View Settings
   :scale: 50%
   :align: right

   図2: Sidebar View Settings

Proxy Render Size
   .. The use of proxies is fully described in section :doc:`Setup </video_editing/setup/proxies>`. Prefetching frames is described in the section about cache.
   プロキシの使用方法については、:doc:`Setup </video_editing/setup/proxies>` セクションで詳しく説明します。フレームのプリフェッチについては、キャッシュに関するセクションで説明します。
Channel
   .. The Sequencer can contain multiple channels. Figure 1 has three channels with strips: a Sound strip at channel 1, a Movie strip at channel 2 and a Scene strip at channel 3. The channel that is shown in the preview, is indicated here. You can get a similar result by Muting strips above the indicated channel. Channel 0 (default setting) is the compositing result of all strips and is shown by default.

   Sequencer には複数のチャンネルを含めることができます。図 1 には、ストリップのある 3 つのチャネルがあります。チャネル 1 にサウンド ストリップ、チャネル 2 にムービー ストリップ、チャネル 3 にシーン ストリップがあります。Preview に表示されるチャネルがここに示されています。指定されたチャンネルの上のストリップをミュートしても同様の結果が得られます。チャンネル 0 (デフォルト設定) はすべてのストリップの合成結果であり、デフォルトで表示されます。

   .. note::
      .. This option should not be interpreted as some kind of "isolation mode". The indicated channel is *not* isolated in the sense that *only* that channel is shown. Each channel is implicitly composited on top of the channel(s) below. A better description could be "show up to channel".
      このオプションは、ある種の「分離モード」として解釈されるべきではありません。指定されたチャネルは、そのチャネルのみが表示されるという意味では分離されていません。各チャネルは、下のチャネルの上に暗黙的に合成されます。より適切な説明は、「チャンネルを見えるようにする」かもしれません。

Show Overexposed
   .. Shows overexposed (bright) areas using a zebra pattern. When is an area overexposed?  You can set the threshold with the slider. The values 0 - 110 should be interpreted as a percentage of decimal value (0 - 1.1). Whenever the RGB value (any component) of a pixel is greater or equal to the specified threshold, it will be marked (zebra-striped) as overexposed. You can check this easily with a color strip. Set the color for example to bright yellow (RGB = 0.9, 0.9, 0). When the threshold is set to 90, everything will be zebra-striped (supposedly overexposed). From threshold value 91 on, the preview shows a bright yellow color again. A threshold of 0 will disable this filter.

   白とび（明るい）部分をゼブラパターンで表示します。領域が露出過度になるのはどのような場合ですか? スライダーで閾値を設定できます。値 0 ～ 110 は、10 進数値 (0 ～ 1.1) のパーセンテージとして解釈されます。ピクセルの RGB値 (任意のコンポーネント) が指定されたしきい値以上である場合、そのピクセルは露出オーバーとしてマーク (ゼブラストライプ) されます。これはカラーストリップで簡単に確認できます。たとえば、色を明るい黄色に設定します (RGB = 0.9、0.9、0)。しきい値を 90 に設定すると、すべてがゼブラストライプになります (おそらく露出オーバーになります)。しきい値 91 以降、プレビューには再び明るい黄色が表示されます。しきい値を 0 にすると、このフィルターが無効になります。

.. note::
   .. The following Overlays (Frame Overlay, Safe Area, Annotations, and Metadata) can be made visible with the Show Overlay button (top right of the Preview window).
   次のOverlay (Frame Overlay, Safe Area, Annotations, および Metadata) は、[Show Overlay] ボタン (Previewウィンドウの右上) を使用して表示できます。

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Frame Overlay
   **Context**:    Video Sequence Editor > Preview
   **Location**:   Sidebar > View
   =============   ==========================================================================

.. figure:: /images/editors_vse_preview_sidebar-frame-overlay.png
   :alt: Side bar Frame Overlay
   :scale: 50%
   :align: right

   図3: Sidebar Frame Overlay


.. By enabling this Frame Overlay setting, you can compare the current frame to a reference frame. This is very handy, for example in color grading. You can have the preview of two shots on the screen so that it is easier to match the colors of two shots. Also in multicam editing where you have shots of the same scene from different cameras, it can come handy to have a preview of both cameras at the same time.

このフレーム オーバーレイ設定を有効にすると、現在のフレームを参照フレームと比較できます。これは、カラーグレーディングなどに非常に便利です。2枚のショットを画面上でプレビュー表示できるので、2枚のショットの色を合わせやすくなります。また、異なるカメラから同じシーンのショットがあるマルチカム編集の場合、両方のカメラを同時にプレビューできると便利です。

.. The User Interface of this option is however a bit rusty.

ただし、このオプションのユーザー インターフェイスは少し時代遅れです。

.. figure:: /images/editors_vse_preview_sidebar-overlay.svg
   :alt: Frame Overlay

   図4: Frame Overlay Type: Reference (left), Current (mid), Rectangle (right)

Set Overlay region
   .. You have to set the Frame Offset (see below) *first*; otherwise you want see much happening. Pressing the Set Overlay Region button lets you draw a box where you want the Overlay to appear in the Preview. The shortcut is :kbd:`O`. In figure 3, an Overlay Region is drawn at the left side of the Preview.
   最初にフレーム オフセット (以下を参照) を設定する必要があります。それ以外の場合は、多くのことが起こっていることを確認したいと思います。[Set Overlay region] ボタンを押すと、Preview内でオーバーレイを表示する場所にボックスを描画できます。ショートカットは :kbd:`O` です。図4 では、オーバーレイ領域が Preview の左側に描画されます。

   .. This Overlay type (Rectangle) is however not that useful. Suppose, you want to see the mid-region of the reference frame. Therefore, you need to draw a box at the mid-region of the current frame, hiding probably some vital info. Drawing it at the top will move it out of the way but will probably show also the less interesting area (top) from the reference frame.

   ただし、このOverlay Type (Rectangle) はあまり役に立ちません。Reference フレームの 中間領域を確認したいとします。その場合、 現在のフレームの中央領域にボックスを描画して、おそらく重要な情報を隠す必要があります。上部に描画すると邪魔にならないように移動しますが、Reference フレームからあまり興味のない領域 (上部) も表示される可能性があります。

Frame Offset
   .. This slider controls the offset of the reference frame relative to current frame. In figure 3, the current frame is at position 7650 and the reference frame at position 6650 (dashed blue line), which is an offset of -1000 frames from the current frame. Changing the Frame Offset will *not* update in real time the Preview window. To see the result of this change, you have to move the playhead.

   このスライダーは、Current のフレームに対する Refrence フレームのオフセットを制御します。図4 では、Current フレームは位置 7650、Referenceフレームは位置 6650 (青い破線) にあり、これは Current フレームから -1000 フレームのオフセットです。[Frame Offset]を変更しても、Previewウィンドウはリアルタイムでは更新されません。この変更の結果を確認するには、Playheadを移動する必要があります。

Overlay Type
   Rectangle
      .. A rectangle area of the reference frame will be displayed on top of current frame at the same position. This is the case used in figure 3 (right handside).
      参照フレームの長方形領域が、現在のフレームの上の同じ位置に表示されます。これは、図4 (右側) で使用されているケースです。
   Reference
      .. Only the reference frame is displayed in the preview region (see figure 3, left handside). Of course, this is exactly the same as moving the current frame and switching off the frame overlay.
      プレビュー領域にはReferenceフレームのみが表示されます (図4 の左側を参照)。もちろん、これは Current フレームを移動し、[Frame Overlay]をオフにすることとまったく同じです。

   Current
         .. Only the current frame is displayed in the preview region (figure 3, mid section). This is, of course, the default behavior of the Preview.
         Current フレームのみがPreview領域に表示されます (図4 中央)。もちろん、これはPreviewのデフォルトの動作です。

   .. tip::
      .. The last two options are only useful when working with two preview windows.It is possible to have several Sequence Editors opened at the same time and they can use different overlay types. So, the middle sequence editor displays the Current frame, while the left editor displays the Reference frame.
      最後の 2 つのオプションは、2 つのPreviewウィンドウを使用する場合にのみ役立ちます。複数のVSE(Video Sequence Editor) を同時に開くことができ、異なる[Overlay Type]を使用できます。したがって、中央のVSEには Current フレームが表示され、左側のVSEには Reference フレームが表示されます。

Overlay Lock
   .. The reference frame is moved in sync with the current frame. With this option, you can (temporary) lock the reference frame to its current position.
   Reference フレームは Current フレームに同期して移動します。このオプションを使用すると、Reference フレームを現在の位置に（一時的に）ロックできます。


.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Safe Areas
   **Context**:    Video Sequence Editor > Preview
   **Location**:   Sidebar > View
   =============   ==========================================================================

.. figure:: /images/editors_vse_preview_sidebar-safe-areas.png
   :alt: Safe Areas
   :scale: 50%
   :align: right

   図5: Safe Areas

.. A safe area is a screen area that is visible on most devices. Especially, older TV's with rounded corners have a much smaller visible area. This safe area is indicated in Blender by dashed lines (see figure 5) and conform to the  `European Broadcasting Union (EBU) <https://tech.ebu.ch/docs/r/r095.pdf>`_ rules. There are two areas:

[Safe Areas]とは、ほとんどのデバイスで表示される画面領域です。特に、角が丸い古いテレビでは、表示される領域が非常に小さくなります。この[Safe Areas]は、Blender では点線で示され (図6 を参照)、 `European Broadcasting Union (EBU) <https://tech.ebu.ch/docs/r/r095.pdf>`_ の規則に準拠しています。次の 2 つの領域があります。

.. figure:: /images/editors_vse_preview_safe-areas.svg
   :alt: Safe areas

   図6: Safe Areas

Title Safe Margins X & Y
   .. According to the EBU document (where this option is called "Graphics Safe Area"), this is set by default to 5% of the project resolution. All text and graphic elements such as subtitles or a logo must be placed within this area.
   EBU ドキュメント (このオプションは「グラフィックス セーフ エリア」と呼ばれています) によると、これはデフォルトでプロジェクト解像度の 5% に設定されています。字幕やロゴなどのすべてのテキストおよびグラフィック要素は、この領域内に配置する必要があります。

Action Safe Margins X & Y
   .. All major action should be viewable within this area. By default, the Action Safe Margins are set to 3.5% of the the project resolution. The Action Safe Margins are smaller than the Title Safe Margins because loosing some text (or logo) is more harmful than cutting some action.
   すべての主要なアクションはこの領域内で表示できる必要があります。デフォルトでは、アクション セーフ マージンはプロジェクト解像度の 3.5% に設定されています。一部のテキスト (またはロゴ) を失うことは、一部のアクションをカットするよりも有害であるため、アクション セーフ マージンはタイトル セーフ マージンよりも小さくなります。
Center-Cut Safe Areas
   .. This ensures that people who still have old 4×3 TVs or monitors won’t have the text cut off on the sides. By default, this is set to 17.5% of the X project resolution and 5% of the Y axis. Of course, these values are for a 16:9 aspect ratio project. If you want to display a 16:9 image in a 4:3 area, there are two possibilities (see figure 6).
   これにより、古い 4×3 テレビやモニターをまだ持っている人でも、側面のテキストが切れることがなくなります。デフォルトでは、これは X プロジェクト解像度の 17.5%、Y 軸の 5% に設定されています。もちろん、これらの値はアスペクト比 16:9 のプロジェクトのものです。16:9 の画像を 4:3 領域に表示する場合、2 つの可能性があります (図7 を参照)。

.. figure:: /images/editors_vse_preview_safe-areas-4x3.svg
   :alt: Safe areas conversion

   図7: How to fit a 16:9 image in a 4:3 area?

.. In the left solution of figure 6, the complete 16:9 image is preserved but two black rectangular areas (called letterboxes) are added to the top and bottom. If you want to completely fill the 4:3 area with footage, you need the solution at the right of figure 6. The original 16:9 image is cropped 12.5%, both left and right. Add another 5% for the Title Safe Area and you'll get the default 17.5%.

図7 の左側のソリューションでは、完全な 16:9 画像が保存されていますが、2 つの黒い長方形の領域 (レターボックスと呼ばれます) が上部と下部に追加されています。4:3 領域をフッテージで完全に埋めたい場合は、図 6 の右側にある解決策が必要です。元の 16:9 画像は左右とも 12.5% トリミングされます。タイトル セーフ エリアにさらに 5% を追加すると、デフォルトの 17.5% になります。

.. note::
   .. Modern TV's and computer monitors have fixed pixel matrix screens and the viewable area is much larger than older CRT (Cathode Ray Tube) screens. So, the safe areas are not that important anymore. However, users are accustomed with the safe area layout. So, following the safe area guides is good practice. Also, from an aesthetic view point it is not advisable to stick text or logos to the very edge of the screen.
   最新のテレビやコンピュータのモニターは固定ピクセル マトリックス画面を備えており、表示可能な領域は古い CRT (陰極線管) 画面よりもはるかに大きくなります。したがって、Safe Areas はもはやそれほど重要ではありません。ただし、ユーザーは Safe Areas のレイアウトに慣れています。したがって、Safe Areasのガイドに従うことをお勧めします。また、美観の観点から、画面の端にテキストやロゴを貼り付けることはお勧めできません。

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Scene Strip Display
   **Context**:    Video Sequence Editor > Preview
   **Location**:   Sidebar > View
   =============   ==========================================================================

.. figure:: /images/editors_vse_preview_sidebar-scene-strip-display.png
   :alt: Scene Strip Display
   :scale: 50%
   :align: right

   図8: Scene Strip Display


.. With this option, you can control how the images of Scene Strips are displayed in the preview. In figure 1, a scene strip was added to display the orange circle at the left of the intro text. This orange circle was created in the 3D view of another scene; you cannot use the same scene of the sequencer. It's a simple mesh with an orange emission material applied to it.

このオプションを使用すると、シーン ストリップの画像が Preview にどのように表示されるかを制御できます。図1 では、シーンストリップが追加され、イントロ テキストの左側にオレンジ色の円が表示されます。このオレンジ色の円は、別のシーンの 3D ビューで作成されました。Sequencerの同じシーンを使用することはできません。この円は、オレンジ色の発光マテリアルを適用したシンプルなメッシュです。

Shading
   .. Shading refers to the way objects are drawn and lit in the Preview. More info can be found at `Viewport Shading <https://docs.blender.org/manual/en/dev/editors/3dview/display/shading.html#wireframe>`_

   シェーディングとは、プレビューでオブジェクトが描画および照明される方法を指します。詳細については、`Viewport Shading <https://docs.blender.org/manual/en/dev/editors/3dview/display/shading.html#wireframe>`_ を参照してください。

   .. * Solid: shows the objects from the scene strip as massive objects but without any materials assigned. The lightning, colors and other options could be set in the Workbench Render Engine (Properties > Render Tab > Render Engine).
   .. * Wireframe: *Does not seem to work!*
   .. * Material Preview: Renders the scene strip with the Eevee render engine, independent of the render engine that was selected in the scene itself.
   .. * Rendered: Render the scene strip with the chosen scene Render Engine (Cycles, Eevee, Workbench). By default the scene lights are used for lighting.
   * Solid: シーン ストリップのオブジェクトをmassiveオブジェクトとして表示しますが、マテリアルは割り当てられていません。稲妻、色、その他のオプションは、ワークベンチ レンダリング エンジン ([Properties] > [Render]タブ > [Render Engine]) で設定できます。
   * Wireframe: *機能しないようです!*
   * Material Preview: シーン自体で選択されたレンダリング エンジンとは関係なく、Eevee レンダリング エンジンを使用してシーン ストリップをレンダリングします。
   * Rendered: 選択したシーン レンダリング エンジン (Cycles、Eevee、Workbench) を使用してシーン ストリップをレンダリングします。デフォルトでは、シーン ライトが照明に使用されます。

   .. figure:: /images/editors_vse_preview_scene-strip.svg
      :alt: Scene Strip Display


      図9: Scene Strip Display (Solid, Material Preview, Rendered); 図1も参照.

   .. Note that the image in the Rendered view is slightly different because it is rendered with the render engine of the source scene, which was set to Cycles.
   レンダリング ビューのイメージは、Cycles に設定されたソース シーンのレンダリング エンジンを使用してレンダリングされるため、若干異なることに注意してください。

Override Scene Settings
   .. This option is only available, if Solid shading is activated. When enabled, it uses the Workbench render settings from the sequencer scene, *not* the Workbench render settings from the source scene. You can find these settings in the Properties > Render tab > Render Engine.
   このオプションは、ソリッド シェーディングがアクティブ化されている場合にのみ使用できます。有効にすると、ソース シーンの Workbench レンダリング設定ではなく、Sequencer のシーンの Workbench レンダリング設定が使用されます。これらの設定は、 [Properties] > [Render]タブ > [Render Engine] にあります。



.. _annotations:

.. admonition:: Reference
   :class: refbox

   =============   ==========================================================================
   **Name**:       Annotations
   **Context**:    Video Sequence Editor > Preview
   **Location**:   Sidebar > View
   =============   ==========================================================================

.. figure:: /images/editors_vse_preview_sidebar-annotations.png
   :alt: Annotations panel
   :scale: 50%
   :align: right

   図10: Annotations panel

Annotations
   .. With this panel, you can change the appearance of the Annotations that were made in the Preview. More info can be found in the `User Interface section <https://docs.blender.org/manual/en/latest/interface/annotate_tool.html>`_. Using the Annotate tool (in the 3D viewport) is explained in detail in the tutorial by `3DGreenhorn <https://www.youtube.com/watch?v=cVr4pduQJQA>`_.
   このパネルを使用すると、プレビューで作成された注釈の外観を変更できます。詳細については、 `User Interface section <https://docs.blender.org/manual/en/latest/interface/annotate_tool.html>`_ セクションを参照してください。注釈ツール (3D ビューポート内) の使用方法は、`3DGreenhorn <https://www.youtube.com/watch?v=cVr4pduQJQA>`_ によるチュートリアルで詳しく説明されています。

   .. To create an Annotation, you have to select the Annotate tool in the :doc:`Toolbar <toolbar>` (shortcut :kbd:`D`) and start drawing. A new data-block is created and made visible in the Annotate panel of the side bar, called "Annotations" in figure 6. You can create multiple data-blocks (e.g. Annotations.001, Annotations.002, ... with the Add New button (see figure 6) or change to another data-block with the drop-down at the left of the header. All newly added annotations in the Preview are stored within the selected data-block. You can *only* display the annotations of *one* data-block at a time. To remove an Annotations data-block, click the Unlink button. That data-block however is not deleted at once (so you can recover it with the drop-down) but is deleted when the Blend-file is saved (unless the Fake User button is enabled).

   注釈を作成するには、:doc:`Toolbar <toolbar>` (ショートカットキー :kbd:`D`) で注釈ツールを選択し、描画を開始する必要があります。新しいデータ ブロックが作成され、サイド バーの [Annotations] パネルに表示されます (図10  "Annotations"と呼ばれます)。 [New] ボタンを使用して、複数のデータ ブロック (例: Annotations.001、Annotations.002 など) を作成できます。 (図10 を参照) またはヘッダーの左側にあるドロップダウンを使用して別のデータ ブロックに変更します。プレビューに新しく追加されたすべての注釈は、選択したデータ ブロック内に保存されます。表示できるのは1 つのデータの注釈のみです。注釈データ ブロックを削除するには、[Unlink] ボタンをクリックします。ただし、そのデータ ブロックは一度に削除されず (ドロップダウンで復元できるため)、Blend ファイルが保存されるときに削除されます。 ([Fake User] ボタンが有効になっていない限り)。

   .. Within a data-block , there can be multiple layers. The default name of a layer is "note". You can create multiple layers (e.g. note.001, ...) with the Add New Annotation Layer button (+); for example if you want to use different colors. To remove a layer, click (-). To make a layer invisible in Preview, click the Hide button (eye). One layer can contain multiple annotations. They can be drawn in the Preview at the same frame or at different frames. The color of the annotations is set per layer with the Color picker (at the left of the Note). Also, the Opacity and Thickness are set per layer.

   データ ブロック 内には複数のレイヤーが存在する場合があります。デフォルトのレイヤー名は「note」です。[Add New Annotation Layer] ボタン (+) を使用して、複数のレイヤー (note.001 など) を作成できます。たとえば、別の色を使用したい場合などです。レイヤーを削除するには、(-) をクリックします。プレビューでレイヤーを非表示にするには、「Hide」ボタン (eyeマーク) をクリックします。1 つのレイヤーに複数の注釈を含めることができます。これらは、Preview で同じフレームまたは異なるフレームで描画できます。注釈の色は、カラーピッカー (Noteの左側) を使用してレイヤーごとに設定します。また、不透明度と太さはレイヤーごとに設定されます。

   .. An annotation, drawn in the Preview, is visible at the frame that it is drawn and stays visible until the next frame *with* an annotation. So, if you have two consecutive annotations (eg. at frame 10 and 11); the first annotation will only be visible for one frame (eg. frame 10), while the second annotation will stay visible (frame 11 to ...). With the Lock Current Frame button, you will freeze the annotations of that specific frame, regardless of previous and later annotations.

   プレビューに描画された注釈は、描画されたフレームで表示され、注釈が含まれる次のフレームまで表示されたままになります。したがって、2 つの連続したアノテーションがある場合 (フレーム 10 と 11 など)。最初の注釈は 1 つのフレーム (フレーム 10 など) でのみ表示されますが、2 番目の注釈は表示されたままになります (フレーム 11 から…)。[Lock Current Frame] ボタンを使用すると、前後の注釈に関係なく、その特定のフレームの注釈をフリーズします。

Onion Skinning
   .. With Onion Skinning, you can make the previous and later annotations of the current frame visible. They appear in the selected colors for a number of frames (Before and After). Setting the Before and After value to zero will show the annotations one frame before and one frame after the current frame. Setting it to a higher number will show them for a longer period before and after. Setting these values to -1 will disable the Onion Skinning in that direction.

   [Onion Skinning] を使用すると、現在のフレームの前後の注釈を表示できます。これらは、いくつかのフレーム (前後) で選択した色で表示されます。Before と After の値をゼロに設定すると、現在のフレームの 1 フレーム前と 1 フレーム後の注釈が表示されます。より大きな数値に設定すると、前後に長い時間表示されます。これらの値を -1 に設定すると、その方向のオニオン スキニングが無効になります。



.. figure:: /images/editors_vse_preview_onion-skinning.svg
   :alt: Onion Skinning


   図11: VSE の Onion Skinning

Metadata
   .. A movie or image strip can contain, in addition to the actual image, some metadata such as the file name, the date created, the camera model, ... Some of this metadata can be made visible in the Preview (see Show Overlay button). The metadata that is shown however is from the strip under the playhead, *not* the active (selected) strip in the sequencer.
   ムービーまたはイメージ ストリップには、実際の画像に加えて、ファイル名、作成日、カメラ モデルなどのメタデータを含めることができます。このメタデータの一部はプレビューに表示できます ([Show Overlay] ボタンを参照)。ただし、表示されるメタデータは、シーケンサー内のアクティブな (選択された) ストリップではなく、Playheadの下のストリップからのものです。

   .. The metadata from a Blender output render is stored in the appropriate fields (camera, time, ...; see `Rendered Output <https://docs.blender.org/manual/en/dev/render/output/properties/metadata.html>`_. Some graphic programs such as Gimp also store some metadata. However, only the text stored in the header field "Comments" is displayed in the Preview and shown in the metadata panel. You cannot edit this value from within Blender. For that, you need an external program such as exiftool.

   Blender 出力レンダリングからのメタデータは、適切なフィールド (カメラ、時間など) に保存されます。  `Rendered Output <https://docs.blender.org/manual/en/dev/render/output/properties/metadata.html>`_ を参照してください。Gimp などの一部のグラフィック プログラムも一部のメタデータを保存します。ただし、ヘッダー フィールド「コメント」に保存されているテキストのみが表示されます。プレビューに表示され、メタデータ パネルに表示されます。この値は Blender 内から編集することはできません。そのためには、exiftool などの外部プログラムが必要です。

   .. The command to change the Comments field is:
   「コメント」フィールドを変更するコマンドは次のとおりです。

   exiftool --comments="My new comment" name-of-file.png

   .. Note::
      .. The metadata will only be displayed for the image, that has not been processed by any effect. For example, adding an effect strip (eg. Glow) will hide the metadata from view. Of course, the metadata isn't removed from the file. Hiding the effect strip will display it again.
      メタデータは、エフェクトによって処理されていない画像に対してのみ表示されます。たとえば、エフェクト ストリップ (グローなど) を追加すると、メタデータが表示されなくなります。もちろん、メタデータはファイルから削除されません。エフェクト ストリップを非表示にすると、再び表示されます。
