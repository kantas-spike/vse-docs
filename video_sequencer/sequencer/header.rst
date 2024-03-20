Header
------
.. The Header of the VSE is by default located at the very top of the editor. You can however flip it to the bottom :kbd:`RMB` on header ; see `Header > Context menu <https://docs.blender.org/manual/en/dev/interface/window_system/regions.html#header>`_ for more info about the available options. There are three areas within the Header.

VSEの Header はデフォルトでは、エディターの最上部に配置されます。ヘッダー上で :kbd:`RMB` をクリックすることで、コンテキストメニューからヘッダーを最下部に配置することもできます。利用可能なオプションの詳細は、 `Header > Context menu <https://docs.blender.org/manual/en/dev/interface/window_system/regions.html#header>`_ を参照してください。

Headerには3つの領域があります。


.. Type Selector buttons
Type Selector ボタン
.....................

.. The left area contains the Editor Type selector and the View Type selector (see figure 1). As the name implies, you can swap the entire editor to another type (e.g. Compositor) with the Editor Type selector. With the View Type selector you can select a specific view: Sequencer, Preview or Sequencer/Preview. Depending on the selected type, you'll get slightly different headers.

左側の領域は Editor Type Selecto と View Type Selector を持ちます(図1)。
名前が示すように、Editor Type Selectorを使用して、エディター全体を、別のタイプのエディター(例えば Compositor)に切替えることができます。
View Type Selectorを使うと、特定のビュー(Sequencer、Preview、Sequencer/Preview)を選択できます。選択されたビューのタイプによって、多少内容が異なるHeaderが表示されます。

.. Menu bar
メニューバー
........

.. The middle area contains the menu bar. Again, the menu can be toggled on or off with the context menu. Figure 1 shows the menu bar with the expanded menu items beneath.

中央の領域はメニューバーを持ちます。この場合も、メニューはコンテキストメニューを使って、表示・非表示を切替えれます。
図1は、メニューの下に、展開されたメニュー項目を合せて表示しています。

.. figure:: /images/editors_vse_header-sequencer.svg
   :alt: Header Sequencer


   図1: パネルが展開されたSequencerビューのHeader


.. The menus Select, Marker, Add and Strip are discussed in following sections or in the Video Editing chapter, when they appear in our typical workflow. The View menu contains many items which are specific for operation within the Sequencer; so, they are discussed here.

[Select], [Marker], [Add] と [Strip] メニューは、一般的な動画編集ワークフローの中で登場する時に、以降のセクションや Video Editingの章で説明します。
[View] メニューは、Sequencerの操作に特有の多くの項目を含むため、ここで説明します。

.. View Menu
View メニュー
,,,,,,,,,

.. See figure 1 (left panel) for an overview of all the submenus of the Sequencer's View menu.

Sequencerの[View]メニューのすべてのサブメニューの概要は、図1(左下のパネル)を参照してください 。

Sidebar :kbd:`N`
   .. Show or hide the sidebar. You can use the shortcut :kbd:`N` or the Sidebar button (see figure 1) to toggle on or off. This sidebar appears at the right of the sequencer and will show all the properties of the active strip. Please, note that the active strip does *not* need to be a selected strip (see :ref:`Selecting <video_editing_edit_timeline_select>`). A detailled description of all the properties of the various strip types can be found in the :ref:`Video Editing <striptypes>` section.

   Sidebarを表示・非表示します。ショートカットキー :kbd:`N` か Sidebarボタン(図１)を使って、表示・非表示を切替えれます。
   Sidebarは Sequenceer の右側に表示され、編集対象(active)のストリップの全てのプロパティーが表示されます。
   編集対象(active)のストリップは選択されたストリップである *必要はない* ことに注意してください (参照 :ref:`Selecting <video_editing_edit_timeline_select>`)。
   様々なストリップのタイプの全プロパティーの詳細については、 :ref:`Video Editing <striptypes>` セクションを参照してください。



Tool Settings
   .. Show or hide the Tool Settings (below the menu bar). These Tool Settings are mostly used in combination with the Toolbar (:kbd:`T`). For example, if you select the Blade tool in the Toolbar, then you can choose between *Soft* and *Hard* in the Tool Settings.

   Tool Settings (メニューバーの下に配置) を表示・非表示します。 Tool Settings は 主にToolbar (:kbd:`T`)と組合せて使用します。
   例えば、ToolbarでBladeツールを選択した場合、Tool Settingsで Bladeツールのカット方式を *Soft* と *Hard* から選択できます。

.. figure:: /images/editors_vse_header_toolbar-generic.png
   :alt: Toolbar
   :scale: 80%
   :align: right

Toolbar :kbd:`T`
   .. Show or hide the toolbar. You can use the shortcut :kbd:`T` or the Toolbar button (see figure 1) to toggle on or off. The toolbar in the Video Sequencer is rather minimalistic and not useful. It contains only a Select and Blade tool.

   Toolbar を表示・非表示します。ショートカットキー :kbd:`T` か Toolbarボタン(図1)を使って、表示・非表示を切替えれます。
   SequncerのToolbarは、かなり簡素で役に立ちません。これには、選択ツールとBladeツールのみ含まれます。

.. warning::
   .. Both generic tools don't seem to work. Some addons, for example the `VSE Transform Tools <https://github.com/zeograd/VSE_Transform_Tools>`_ make better use of this toolbar.

   どちらの汎用ツールも上手く機能しないようです。例えば、`VSE Transform Tools <https://github.com/zeograd/VSE_Transform_Tools>`_ のような一部のアドオンは、Toolbarを有効に活用します。 [#f1]_

Adjust Last Operation
   .. If enabled, this option will display a pop-up panel to alter properties of the last completed operation. For some general background info, see :ref:`bpy.ops.screen.redo_last`.

   有効にした場合、最後に完了した操作のプロパティーを変更するためのポップアップパネルを表示します。
   一般的な背景情報については、:ref:`bpy.ops.screen.redo_last` を参照してください。

   .. For example, after a Duplicate Strip operation, you can still change the horizontal and vertical Offset. Or after a Split operation, you can change the type of split (see figure 2).

   例えば、ストリップの複製オペレーションを実施後に、複製したストリップの水平(開始フレーム)・垂直(チャンネル)オフセットを変更できます。また、ストリップのカットオペレーションを実施後に、カット方式を変更できます(図3)。

   .. figure:: /images/editors_vse_header_adjust_last_operation.svg
      :alt: Adjust Last Operation


      図3: Adjust Last Operationの例

Preview as Backdrop
   .. Displays the current frame in the background of the Sequencer (like in the `Compositor <https://docs.blender.org/manual/en/dev/editors/compositor.html>`_). The backdrop will be updated when the playhead is moved. Of course, when there are a lot of strips in the sequencer, they will occlude most of the backdrop image. When you open the :ref:`Sequencer in Full View <sequencer_full_view>` , this could be an alternative of having the preview window on a separate monitor.

   現在のフレームをSequencerの背景として表示します。(`Compositor <https://docs.blender.org/manual/en/dev/editors/compositor.html>`_ と同じです) この背景プレビューは、プレイヘッドを移動すると更新されます。

   もちろん、大量のストリップがSequencerに配置されている場合、背景画像の大部分は隠されてしまいますが、
   :ref:`Sequencer in Full View <sequencer_full_view>` で表示した場合、背景へのプレビューは、別のモニターに Preview画面を表示する変わりに使用できます。


   .. figure:: /images/editors_vse_header_backdrop.png
      :alt: Backdrop


      図4: Sequencer内のムービーの背景プレビュー

Frame Selected - Frame All - Zoom
   .. These menu items are all about zooming in or out of the Sequencer window. This topic is covered more in depth (with all shortcuts) in section :doc:`Zoom <zoom>`

   これらのメニュー項目は全て、Sequencer画面のズームインまたはズームアウトに関するものです。
   このトピックは(全てのショートカットキーも含め)、 :doc:`Zoom <zoom>` セクションで詳しく説明されています。

.. _bpy.ops.sequencer.refresh_all:

Refresh All
   .. To force Blender to re-read in files, and to force a re-render of a scene strip,
   click the *Refresh All* button. Blender will update and synchronize all cached images and compute the current frame.

   Blenderに強制的にファイルを再読み込みさせたり、強制的にシーンストリップを再描画させる場合は、 *[Refresh All]* ボタンをクリックします。 Blenderはキャッシュされた全ての画像を更新・同期し、現在のフレームを処理します。

   .. Whenever there are unexpected glitches in the playback, there is a chance that the cache is not updated and you need to do a *Refresh All*.

   再生中に予期しない glitch(不具合) が発生した場合は、キャッシュが更新されない場合があるため、 *[Refresh All]* する必要があります。

   .. For example, suppose you have a scene strip (see :ref:`Strip types <striptypes>`) in the Sequencer. Changing something in the source scene (e.g. rotating an object) will not force the Sequencer to update the cache. In the Sequencer you will see the object as if not rotated. Moving with the playhead will refresh the cache but not all at once; so there can be glitches (some frames are updated in the cache, others are not).   Better is to use the Refresh All button, which will invalidate the cache and rebuild it.

   例えば、Sequencerにシーンストリップ(参照 :ref:`Strip types <striptypes>`)があるとします。
   もととなるシーンでなにかを変更しても(例えば、オブジェクトを回転するなど)、Squencerはキャッシュを更新しません。
   Sequencerでは、オブジェクトが回転されることなく表示されます。
   プレイヘッドを動かすとキャッシュは更新されますが、一度に統べてのキャッシュが更新されるわけではありません。

   これにより、glitches(キャッシュ内のいくつかのフレームは更新され、それ以外は更新されない状態)が発生します。
   この場合、[Refresh All] ボタンを使うと良いでしょう。キャッシュが無効になり、キャッシュが再構築されます。

   .. Another use case is when you add an image that is changed later on in an external program. Blender has no real way of knowing this. So, the image should be read in again and the cache should be updated.

   別のユースケースは、追加した画像を後で外部プログラムで変更した場合です。
   Belnderはこのような変更を知ることができません。
   そのため、画像を再読み込みしてキャッシュを更新する必要があります。

   .. Remember that the mouse pointer should be over the correct area: the Sequencer timeline!
   マウスポインタが正しい領域(ここでは、Sequencerタイムライン)上にある必要があることに注意してください。 [#f2]_


Navigation
   .. Navigating your timeline is done by moving the playhead. The Navigation submenus are covered in detail in section :doc:`Navigate <navigate>`

   タイムラインを移動するには、プレイヘッドを移動します。[Navigation] サブメニューは :doc:`Navigate <navigate>` セクションで詳しく説明します。

.. figure:: /images/editors_vse_header_menu-range.png
   :alt: Menu Range
   :align: right
   :scale: 60%

   図5: Range サブメニュー

Range
   .. With the menu Range you can specify which frames are going to be previewed or rendered.
   The first three menu items (see figure 5) will change the *Preview Range* or *Playback Range*. The last three menu items are meant to set the *Render Range*.

   [Range] メニューを使うと、どのフレームをプレビューまたはレンダリングするのかを指定できます [#f3]_。
   最初の3つのメニュー項目(図5)は *Preview Range* や *Playback Range* を変更します。
   最後の3つのメニュー項目は、*Render Range* を設定するためのものです。

   Set Preview Range :kbd:`P`
      .. Interactively define the frame range used for preview or playback. After selecting this menu item, a crosshair cursor appears. With this cursor you can drag a box around the frames that you want to preview. You can drag anywhere within the Sequencer area.
      .. The selected Preview Range will be displayed in the normal black color. The frames outside the Preview Range will be colored brown (see figure 6). The Shortcut :kbd:`P` is, of course, much faster to apply.

      プレビューやプレイバックに使用する範囲を対話的に定義します。このメニューを選択すると、十字カーソルが表示されます。このカーソルを使って、プレビューしたいフレームの範囲を、ドラッグしてボックス選択します。
      Sequencer領域内のどこにでもドラッグして選択できます。
      選択された Preview Range は通常の黒色で表示されます。 Preview Rangeの範囲外のフレームは茶色で表示されます(図6)。

      .. This Preview Range will not affect in any way the Render Range. Both can exist independently.

      この Preview Range は Render Rangeにまったく影響しません。どちらも独立して存在できます。


   Set Preview Range to Strips
      .. Sets the Preview Frame range to the range of the selected strips.

      Preview Rangeを、選択されたストリップの範囲に設定します。

   Clear Preview Range (Shortcut: :kbd:`Alt-P`)
      .. Pressing :kbd:`Alt-P` anywhere within the Sequencer area will clear the preview range. If no Preview Range is defined, then the Render Range willbe used to playback or Preview the movie.

      Sequencer領域内の任意の場所で、:kbd:`Alt-P` を押すと、Preview Rangeがクリアされます。
      Preview Rangeが定義されていない場合は、Render Range がplaybackやpreviewに使用されます。

   .. figure:: /images/editors_vse_header-menu-range.svg
      :alt: Preview & Render Range


      図6: Preview Range と Render Range

   .. The Render Range is normally set during the Setup phase of your project (see :doc:`Project Settings </video_editing/setup/project-settings>`). They also can be set in different editors: `Properties <https://docs.blender.org/manual/en/dev/render/output/properties/dimensions.html>`_ , and `Timeline <https://docs.blender.org/manual/en/dev/editors/timeline.html>`_.

   Render Range は通常、プロジェクトのSetupフェーズ (参照 :doc:`Project Settings </video_editing/setup/project-settings>`) で設定されます。Render Range は、様々エディター(`Properties <https://docs.blender.org/manual/en/dev/render/output/properties/dimensions.html>`_ や `Timeline <https://docs.blender.org/manual/en/dev/editors/timeline.html>`_ )で設定することもできます。

   Set Start Frame :kbd:`Ctrl-Home`
      .. Set Start of Render Range to the current playhead position.
      Render Rangeの開始位置を現在のPlayheadの位置に設定します。
   Set End Frame :kbd:`Ctrl-End`
      .. Set End of Render Range to current playhead position.
      Render Rangeの終了位置を現在のPlayheadの位置に設定します。
   Set Frame Range to Strips
      .. Sets the Render Range to the frame range of the selected strips.
      Render Rangeを選択したストリップの範囲に設定します。

Sync Visible Range
   .. The VSE is a time based editor. But, so is the Dope Sheet, the Graph Editor, and the Timeline. Finetuning animation is often done in the Graph Editor. So, these two editors should work in synchronization.

   VSEは時間ベースのエディターです。そして、Dope Sheet や Graph Editor、Timeline も同様です。アニメーションの微調整には、よくGraph Editorが利用されます。そのため、これら2つのエディターは、同期して動作する必要があります。

   .. The playhead is always synchronized between editors. If the playhead is at frame 15 in the Sequencer, then it will also be at frame 15 in the Graph Editor. The Visible Range, however, is not synchronized by default. So, you could see the frames 15 -150 (= Visible Range) in the Sequencer and a totally different Visible Range in the Graph Editor.

   Playhead は、常にエディター間で同期しています。PlayheadがSequencerの15フレーム目にある場合、Graph Editorでも15フレーム目にあります。
   しかし、表示範囲はデフォルトでは同期しません。そのため、Sequencerで15から150フレームの範囲を表示し、Graph Editerではまったく異なる表示範囲が表示することができます。

   .. Sometimes you could benefit from a synchronized Visible Frame. Zooming in at the Sequencer will also zoom in at the Graph Editor. For that, you need to enable this option.

   場合によっては、表示範囲を同期することで、役に立つことがあります。Sequencerでズームインすると、同様にGraph Editorでもズームインされます。そのためには、このオプションを有効にする必要があります。 [#f4]_


   .. warning::
      .. Currently, if we open the side panels of the animation editors (N or T panels) then the 'Visual Range' shrinks or expands depending on the side panel sizes. This happens even if we have enabled the 'Region Overlap' (Preferences > Interface > Editors > Region Overlap > Enabled) making the option useless.

      現在のところ、エディターのサイドパネル(ショートカット N や Tで開く、SidebarやToolbar)を開くと、サイドパネルのサイズに応じて、表示範囲が縮小または格段します。これは、'Region Overlap' ([Preferences] > [Interface] > [Editors] > [Region Overlap] > [Enabled])を有効にしても発生するため、[Sync Visible Range]オプションは役に立たなくなります。

   .. todo::
      .. Give a meaningful example for this option.
      このオプションの意味のある例を教えてください。 [#f5]_

Show Seconds :kbd:`Ctrl-T`
   .. By default, the timeline units are so-called SMPTE timecodes, e.g. 12+08. This is the time after 12 seconds and 8 frames. Disabling this option will show the timeline in frames (see figure 7).

   デフォルトでは、タイムラインの単位はいわゆる SMTEタイムコードです。例えば、12+08は、12秒と8フレーム後の時刻になります。このオプションを無効にすると、タイムラインはフレーム単位で表示されます(図7)。


   .. figure:: /images/editors_vse_header-menu-show-seconds.svg
      :alt: Menu Show Seconds


      図7: [Show Seconds]オプションの有効/無効

Show Markers
   .. This option is set by default. It shows the markers region (see figure 8). When disabled, the Markers region but also the Markers menu is hidden and the markers operators (adding, deleting, ...) are not available in this editor.

   このオプションはデフォルトで有効に設定されています。このオプションはマーカー領域(図8)を表示します。
   無効の場合は、マーカー領域だけでなく、[Marker]メニューも非表示になります。そして、マーカー関連操作(追加、削除など)がこのエディター内で利用できなくなります。

   マーカーの使用については、:ref:`マーカーの使用 <using_markers>` で詳細を説明する。

   .. figure:: /images/editors_vse_header-menu-show-markers.svg
      :alt: Show Markers


      図8: 3つのマーカーがあるマーカー領域

.. _bpy.types.SequenceEditor.show_cache:

Show Cache, Sequence Render Image, Sequence Render Animation, Export Subtitles
   .. - Cache is described in section Video Editing > Setup > Environment > Proxies & Cache.
   - キャッシュは Video Editing > Setup > Environment > Proxies & Cache セクションで説明します。
   .. - Rendering is described in section Video Editing > Render.
   - Rendering は Video Editing > Render セクションで説明します。
   .. - Subtitles are described in Video Editing > Edit > Sound.
   - Subtitles は Video Editing > Edit > Sound で説明します。

   .. todo::
      .. Add links to those sections
      それらのセクションへのリンクを追加する。

Toggle Sequencer/Preview :kbd:`Ctrl-Tab`
   .. Switch the editor display type between Sequencer and Preview. With the shortcut :kbd:`Ctrl-Tab` you can toggle very fast between these two views. This command is especially useful if you are editing with the Sequencer in full view.

   エディターの表示タイプを Sequencer とPreview の間で切替えます。ショートカットキー :kbd:`Ctrl-Tab` を使うと、これらの2つのビューを素早く切替えることができます。
   このコマンドは、Sequencerをフル表示している編集している場合、特に便利です。

Area
   .. With this menu you can redefine the area that the Sequencer occupies. All options are described in detail in the  `user interface section <https://docs.blender.org/manual/en/dev/interface/window_system/areas.html?highlight=area>`_

   このメニューを使用すると、Sequencerが占める領域を再定義できます。全てのオプションは、`user interface section <https://docs.blender.org/manual/en/dev/interface/window_system/areas.html?highlight=area>`_ で詳しく説明されています。

   https://docs.blender.org/manual/en/dev/interface/window_system/areas.html?highlight=area


Select - Marker - Add - Strip メニュー
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,

.. The menus Select, Marker, Add and Strip are discussed in following sections or in the Video Editing chapter, when they appear in our typical workflow.

[Select]、[Marker]、[Add]、[Strip]メニューは、一般的な動画編集ワークフローの中で登場する時に、以降のセクションや Video Editingの章で説明します。



Overlap ドロップダウン
................
.. When moving a strip in the sequencer, you can drop it onto other strips. With this dropdown, you can specify how to resolve the overlap after transformation. The available options are: Shuffle, Overwrite, and Expand. They are described in more detail in :doc:`video editing > montage > move </video_editing/edit/montage/move>`

Sequencerのストリップを移動する場合、他のストリップの上にドロップできます。Overlapドロップダウンを使うと、移動後のストリップの重なりを解決する方法を指定できます。
使用可能なオプションは、[Shuffle]、[Overwrite]と[Expand]です。:doc:`video editing > montage > move </video_editing/edit/montage/move>` で詳細を説明しています。

Snapping
........
.. If the Snapping option is enabled, moving strips in the sequencer will snap them at the border of other strips (or even the playhead). Thin white lines are displayed when the strip is nearby a border of another strip. With the dropdown, you can eanble some specific options (for example, ignoring sound strips). More detail in :doc:`video editing > montage > move </video_editing/edit/montage/move>`.

Snappingオプションを有効にした場合、Sequencer内のストリップを移動すると、他のストリップ(またはPlayhead)の境界にストリップがスナップ [#f6]_ されます。
移動するストリップが、他のストリップの境界近くにある場合、細い白線が表示されます。Snappingドロップダウンを使うと、いくつかの特別のオプションを有効にできます(例えば、サウンドストリップは無視するなど)。
詳細については、:doc:`video editing > montage > move </video_editing/edit/montage/move>` を参照してください。

Show Overlay ボタン
...................

.. On the extreme right in the header, you find the Show Overlay button (see figure 9). You can enable of disable it completely with :kbd:`LMB - Click` or you can enable/disable one of the options The area at the right contains one or three buttons. By default, Name, Source, Duration, F-curves, and Waveform Display are set.

ヘッダーの右端に、[Show Overlay]ボタンがあります(図9)。
:kbd:`LMB - クリック`で、オーバーレイの表示を、完全に有効するか有効にするかを切替えれます。
また、ドロップダウンを表示し、一部オプションの有効無効を切替えることもできます。

ドロップダウンのパネルには、デフォルトでは、[Name]、[Source]、[Duration]、[Color Tags]、[F-Curves]、[Gird]と[Waveform Display]が設定されているようです。[#f7]_

.. figure:: /images/editors_vse_header_preview-overlays.png
   :alt: Preview Overlays
   :scale: 50%
   :align: right


   図9: Preview Overlays

Name
   .. Enabling this option will show the name of the strip on top of the stripbar; aligned left at the start of the strip. The name of the strip is set in the Properties.
   このオプションを有効にするとストリップバーの上部にストリップの名前が表示されます。ストリップの先頭に左揃えで表示されます。ストリップの名前はストリップのプロパティーで設定されます。

Source
   .. With this option you can show the source filename and path of the strip. The source is set in the :ref:`Source panel <source-panel>`
   このオプションを使うと、ストリップのソースファイル名とパスを表示できます。ソースは、:ref:`Source panel <source-panel>` で設定されます。

Duration
   .. With this option the duration will be displayed. The duration is always set in frames. The Duration can be set in multiple ways. The numeric value is available in the :ref:`Time panel <time-panel>`
   このオプションを使うと、ストリップの長さ(Duration)が表示されます。Durationには常にフレーム数が設定されます。Durationは複数の方法で設定できます。Durationの数値は :ref:`Time panel <time-panel>` で利用できます。

Color Tags
   .. The Color Tags option will switch on the display of the choosen color in the Properties panel of the strip (see figure 10). The default colors are set in the Preferences; see :doc:`Strip types </video_editing/edit/montage/striptypes/index>`
   [Color Tags]オプションを選択すると、ストリップのプロパティーパネル(図10)で選択した色が表示されます。デフォルトカラーはPreferenceで設定されます。参照: :doc:`Strip types </video_editing/edit/montage/striptypes/index>`

   .. figure:: /images/editors_vse_header-sequencer_color_tag.svg
      :alt: Color tags


      図10: Color Tags



Offsets
   .. When creating a Split, the Offset fields get a value. With this option, you will visualize these values with a little blue bar. Only available for the Strip Offset Start and Strip Offset End field. See :doc:`text on splitting </video_editing/edit/montage/transform>`

   分割したストリップを作成するとそのオフセットフィールドの値を取得されます。このオプションを使うと、細い青色のバーでオフセットの値を視覚化します。[#f8]_
   ストリップの開始オフセットと終了オフセットのみ表示できます。参照: :doc:`text on splitting </video_editing/edit/montage/transform>`

F-curves
   .. When animating, for example adding a Fade effect, a F-curve is created. In fact, you are animating the Opacity property of the strip. You can visualize the F-curve with this option.

   アニメーション化する時、例えばフェード効果を追加時、F-curveが作成されます。実際、ストリップのOpacityプロパティーをアニメーション化しています。
   このオプションを使うと、F-curveを視覚化できます。

   .. figure:: /images/editors_vse_header-F-curves.svg
      :alt: F-curves
      :scale: 50%

   図11: F-curves

Thumbnails
   .. For Movie, Image Sequence and Image strips you can display thumbnails. The example in figure 12 has 30 frames; each with a blue background and the frame number in yellow as foreground. To draw thumbnails, this overlay has to be enabled and the strip bars must be tall enough. In order to be recognizable, a thumbnail channel should be at least about 92 pixels (see figure 12; bottom strip).
   .. The width of the thumbnail is calculated in accordance to the aspect ratio of the actual image. In figure 12, the width of the strips at the left side does not vary across zoom level because the strip height isn't changed either. The strip at the top right however has a much larger height, and therefore also a larger width.

   MovieやImage Sequence、Imageストリップについては、サムネイルを表示できます。
   図12の例では、ストリップには30フレームあります。各フレームは青色の背景に黄色のフレーム番号が表示されます。
   サムネイルを表示するためには、[Thumbnails]オプションを有効にし、かつストリップバーの高さが十分である必要があります。
   認識できるようにするには、サムネイルチャンネルは少なくとも約92ピクセルが必要です(図12 一番下のストリップ)。

   サムネイルの幅は実際の画像のアスペクト比に応じて計算されます。図12 では、ストリップの高さも変更されていないため、左側のストリップの幅はズーム レベル全体で変化しません。
   ただし、右上のストリップでは、高さははるかに大きいため、幅も大きくなります。


   .. figure:: /images/editors_vse_sequencer_timeline_sequencer_thumbnails.svg
      :alt: Thumbnails
      :scale: 50%

   図12: 異なるズームレベルのThumbnails

   .. The number of thumbnails depends on the thumbnail size (see above) and the strip length (which depend on the zoom level). The first frame of the strip is always shown as a thumbnail.
   サムネイルの数は、サムネイルのサイズ (上記を参照) とストリップの長さ (ズーム レベルに応じて異なります) によって異なります。ストリップの最初のフレームは常にサムネイルとして表示されます。

   .. The thumbnails are loaded from source file using separate thread and stored in cache. Cache capacity is limited to 5000 thumbnails and performs cleanup of non visible images when limit is reached.
   サムネイルは、別のスレッドを使用してソース ファイルからロードされ、キャッシュに保存されます。キャッシュ容量は 5000 サムネイルに制限されており、制限に達すると表示されない画像のクリーンアップが実行されます。

Grid
   .. If enabled, thin black vertical lines are displayed in the sequencer every *n* frames. The number of frames depend on the zoom levels but starts at every 1000 frames (if zoomed out sufficiently) and decrements while zooming in to 500, 200, 100, 50, 20, 15, 10, 5, and eventually stops at every two frames. This grid is a visual aid to recognizing the location of strips in the timeline.
   有効にすると、 nフレームごとに細い黒色の垂直線がシーケンサーに表示されます。フレーム数はズーム レベルによって異なりますが、(十分にズームアウトした場合) 1000 フレームごとに開始され、500、200、100、50、20、15、10、5 とズームインしながら減少し、最終的には 2 フレームごとに停止します。 このグリッドは、タイムライン内のストリップの位置を認識するための視覚的な補助です。


Waveform Display
   .. In figure 9, this option is already expanded. You can choose to override the Strip Option and display (waveforms On) or not display (Waveforms Off) the waveform of a sound strip in the strip bar. The Strip option is set in the Sound Properties of the :doc:`Sound </video_editing/edit/montage/striptypes/sound>` strip.

   図9 では、このオプションはすでに設定されています。ストリップ オプションをオーバーライドして、ストリップ バーにサウンド ストリップの波形を表示する (波形オン) か表示しない (波形オフ) かを選択できます。ストリップ オプションは、:doc:`Sound </video_editing/edit/montage/striptypes/sound>` のSoundプロパティで設定します。

.. rubric:: 脚注

.. [#f1] (訳注) このアドオンのリポジトリを見ると、最終コミットは3年前なのでメンテナンスされていないため、利用しないほうが良さそうです。 *TODO*: SequencerのToolbarに良いツールを追加できるアドオンを探す

.. [#f2] (訳注) メニューで [Refresh All] する場合は必ずマウスポインタはSequencer内にあるため、ショートカットキーで [Refresh All] する場合の注意だと思われます。

.. [#f3] (訳注) 処理対象とするフレームの範囲を指定できます

.. [#f4] (訳注) Sequencer と Graph Editorを同期させる場合、その両方の[Sync Visible Range]を有効にする必要があるようです。どちらか一方では同期しません。

.. [#f5] (訳注) 厳密な表示範囲の同期ではなく、ざっくりした表示範囲の同期になります。それでも、いくつかのマーカー間で頻繁にPlayheadを動かして、アニメーションを調整する場合は便利かもしれません。

.. [#f6] (訳注) スナップとは吸着するように動作することだそうです。

.. [#f7] (訳注) 本文の内容がBlender4.0とあっていないため、訳者が修正・追記しました。

.. [#f8] (訳注) MovieやSoundストリップなどStrip Offsetを持つストリップのみ対象になるようです。
