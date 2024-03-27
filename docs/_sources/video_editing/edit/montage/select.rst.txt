Select
------

.. Before you can do *anything* with strips, you have to select them (see below for the different methods of selecting). There is a difference between a *selected* strip and the *active* strip (see figure 1). Selected strips have an outline. A selected but not active strip has an orange outline. The active and selected strip has a white outline, and white text if available. There is always one and only one strip active. The properties shown in the sidebar belong to this active strip.

ストリップで何かを行う前に、ストリップを選択する必要があります (さまざまな選択方法については以下を参照してください)。
選択したストリップとアクティブなストリップには違いがあります(図 1 を参照)。選択したストリップにはアウトラインが付きます。選択されているがアクティブではないストリップには、オレンジ色の輪郭が表示されます。アクティブで選択されたストリップには白い輪郭が表示され、使用可能な場合は白いテキストが表示されます。アクティブなストリップは常に 1 つだけです。サイドバーに表示されるプロパティは、このアクティブなストリップに属します。

.. _video_editing_edit_timeline_select:

.. figure:: /images/video_editing_edit_montage_select_active-vs-selected.svg
   :alt: Active vs selected View

   図1 アクティブなストリップと選択されたストリップ

.. Even if *no* strip is selected, there is an Active strip. For example, in figure 1-a, the second strip is the Active strip. If there is no Text overlay or selection, the only way to know is by looking at the sidebar. In figure 1-b, it is obvious that Strip 2 is active (white text) and that *only* strip 1 and 3 are selected (orange outline). In figure 1-c, all three strips are selected (orange and white outline) and strip 3 is the active one (white text).

ストリップが選択されていない場合でも、アクティブなストリップが存在します。たとえば、図 1-a では、2 番目のストリップがアクティブ ストリップです。テキスト オーバーレイまたは選択範囲がない場合、それを知る唯一の方法は Sidebar を見ることです。図 1-b では、ストリップ 2 がアクティブ (白色のテキスト) であり、ストリップ 1 と 3のみが選択されている (オレンジ色の輪郭)ことが明らかです。図 1-c では、3 つのストリップがすべて選択されており (オレンジと白の輪郭)、ストリップ 3 がアクティブなストリップ (白のテキスト) です。

.. Some actions such as Delete will apply only to the selected strips. Pressing Delete in figure 1-b will only delete strip 1 and strip 3. Other actions will only have an effect on the active strip such as scaling or rotating.

削除などの一部のアクションは、選択したストリップにのみ適用されます。図 1-b で [削除] を押すと、ストリップ 1 とストリップ 3 のみが削除されます。拡大縮小や回転など、他のアクションはアクティブなストリップにのみ影響します。

.. Note::
    .. Changing a value in the sidebar will normally only change the property of the active strip, even if more strips are selected. It is possible to apply an effect to all selected strips instead of only on the active one by pressing the :kbd:`Alt` key. You have to enter the value numerically and then pressing :kbd:`Alt` + :kbd:`Enter` will apply the value to all selected strips. If you change the value by dragging the slider, you have to press :kbd:`Alt` + :kbd:`Enter` twice  to apply the effect to all selected strips. You can also Right Click on any value and choose "Copy to Selected".

    Sidebar の値を変更すると、さらに多くのストリップが選択されている場合でも、通常はアクティブなストリップのプロパティのみが変更されます。 :kbd:`Alt` キーを押すと、アクティブなストリップのみではなく、選択したすべてのストリップにエフェクトを適用することができます。
    値を数値で入力し、 :kbd:`Alt` + :kbd:`Enter` を押すと、選択したすべてのストリップに値が適用されます。
    スライダーをドラッグして値を変更する場合、選択したすべてのストリップに効果を適用するには :kbd:`Alt` + :kbd:`Enter` を2 回押す必要があります。任意の値を右クリックして「選択項目にコピー」を選択することもできます。

Select one strip
................

.. As can be seen in figure 1, a strip bar has a 'body' and a left and right handle; the small darker colored bars at the left and right of the strip. You can select the strip in its entirety (body + handles) by clicking :kbd:`LMB` somewhere in the middle of the strip bar. Dragging with the mouse will then *move* the strip to another position.

図 1 からわかるように、ストリップ バーには 'ボディー' と左右のハンドル があります。ストリップの左右にある小さな暗い色のバー がハンドルです。ストリップ バーの中央のどこかを :kbd:`LMB` クリックすると、ストリップ全体 (ボディ + ハンドル) を選択できます。マウスでドラッグすると、ストリップが別の位置に移動します。

.. However, you can also click (nearby) the handles. This will select the handle. The darker colored small bar will become white and dragging will *extend* or *shorten* the clip (see section about :ref:`Offsets <time-panel>` to understand what is happening. Note that also the Start and/or End date is displayed; even if The Show Overlay button is disabled.

ただし、ハンドル (近く) をクリックすることもできます。これでハンドルが選択されます。濃い色の小さなバーが白になり、ドラッグするとクリップが延長または短縮されます (何が起こっているかを理解するには、 :ref:`Offsets <time-panel>` に関するセクションを参照してください。[Show Overlay] ボタンが無効になっている場合でも、Start および/または End date?? が表示されることに注意してください。

.. If you have :doc:`zoomed out </video_sequencer/sequencer/zoom>` the strip bars could become pretty small and it's a known annoyance to select the handles instead of the entire strip. Once the handles are selected, you have to deselect (clicking in the middle part again won't help) and select the strip a second time to have access to the entire strip.

:doc:`zoomed out </video_sequencer/sequencer/zoom>` した場合、ストリップ バーがかなり小さくなる可能性があり、ストリップ全体ではなくハンドルを選択するのが煩わしいことが知られています。
また、ハンドルを選択したら、ストリップ全体にアクセスするには、選択を解除し (中央部分をもう一度クリックしても役に立ちません)、もう一度ストリップを選択する必要があります [#f1]_。

.. Select multiple strips
複数のストリップを選択する
......................

.. Select specific strips
特定のストリップを選択する
    .. You can :kbd:`Shift` + click consecutively on strips to select them all. The strip that is last clicked will become the active one. If you want another strip to be active, click that strip again (without releasing :kbd:`Shift`). To remove a strip from the collection, make it active and :kbd:`Shift` + click again.

    ストリップを連続して :kbd:`Shift` + click して、クリックしたストリップを選択できます。最後にクリックしたストリップがアクティブになります。
    別のストリップをアクティブにしたい場合は、そのストリップをもう一度クリックします (:kbd:`Shift` を放さずに)。
    コレクションからストリップを削除するには、ストリップをアクティブにして、もう一度 :kbd:`Shift` + click します。

.. figure:: /images/video_editing_edit_montage_select_select-menu.svg
   :alt: Active vs selected View
   :align: right

   図2 メニューの選択

すべてのストリップを選択
   .. The shortcut key :kbd:`A` selects all the strips in the timeline (visible and invisible). The strip which was the last active strip becomes active again. The menu equivalent is Select > All (see figure 2).
   ショートカット :kbd:`A` キーは、タイムライン内のすべてのストリップ (表示および非表示) を選択します。最後にアクティブだったストリップが再びアクティブになります。同等のメニューは、[Select] > [All] です (図 2)。

すべてのストリップの選択を解除
   .. You can either choose :kbd:`Alt-A` or fast tap twice :kbd:`A` to deselect all the strips in the timeline. Or, and this is probably the most used technique: just click somewhere outside the strips in the sequencer. The menu equivalent is Select > None (see figure 2).
   :kbd:`Alt-A` を押す か :kbd:`A` を素早く2回押す と タイムライン内のすべてのストリップを選択を解除できます。
   または、おそらく最もよく使用されるテクニックは、シーケンサーのストリップの外側のどこかを、ただクリックすることです。
   同等のメニューは、[Select] > [None] です (図 2)

選択範囲を反転
   .. Press :kbd:`Ctrl-I` to invert the current selection of strips. The menu equivalent is Select > Invert (see figure 2).
   :kbd:`Ctrl-I` を押すと、現在選択されているストリップが反転します。同等のメニューは、[Select] > [Invert] です (図 2)。

ストリップのボックス選択
   .. Pressing the :kbd:`B` key will produce a crosshair cursor. You can draw a rectangle selection around a region of strips in your Sequencer window.  All strips that intersect this rectangle (they should not be enclosed) will be selected. The menu equivalent is Select > Box Select (see figure 2).
   :kbd:`B` キーを押すと十字カーソルが表示されます。Sequencer ウィンドウでストリップの領域の周囲に四角形の選択範囲を描画できます。
   この長方形と交差するすべてのストリップ (囲む必要はない) が選択されます。同等のメニューは、[Select] > [Box Select] です (図 2)。

   .. The same result could be obtained by just :kbd:`LMB` clicking and dragging the selection over some strips.
   :kbd:`LMB` で ただクリックして、いくつかのストリップ上に 選択範囲をドラッグするだけでも、同じ結果が得られます。

.. Extend/shrink selection
選択範囲の拡大/縮小 ??


.. Location based selection
場所に基づいた選択
.........................

.. figure:: /images/video_editing_edit_montage_select_select-menu-location-based.svg
   :alt: Select Location Based

   図3 位置ベースの選択

.. With these commands you can select strips, based on their position on the timeline in relation to the playhead or the active strip (see figure 2).
これらのコマンドを使用すると、再生ヘッドまたはアクティブなストリップに対するタイムライン上の位置に基づいてストリップを選択できます (図3)。

.. Select all strips based on position of playhead
Playhead位置に基づいてすべてのストリップを選択
   .. Pressing :kbd:`[` key will select all strips that *start after* the playhead in all channels. Pressing :kbd:`]` will select all strips that *start before* the playhead. Please note, that strips running over the playhead will not be selected. If you want those strips in the selection, you first have to select the opposite side and then invert that selection (see above).

   :kbd:`[` キーを押すと、すべてのチャンネルで Playhead の *左側* の すべてのストリップが選択されます。
   :kbd:`]` を押すと、Playhead の *右側* のすべてのストリップが選択されます。
   ただし、Playheadの上を走るストリップは選択されないことに注意してください。これらのストリップを選択範囲に含めたい場合は、まず反対側を選択してから、その選択範囲を反転する必要があります (上記を参照)。

   .. Users of a non-QWERTY keyboard probably need different keys. For example, on an AZERTY keyboard, you should use the ellipsis ) for the Select left command. You can change the key assignment rather easily in the User Preferences: menu Edit > Preferences > Keymap. Search for "Select Side of frame" and assign a new key.

   QWERTY 以外のキーボードを使用している場合は、おそらく別のキーが必要になります。たとえば、AZERTY キーボードでは、[Select left] コマンドに :kbd:`)` を使用する必要があります。キーの割り当ては、ユーザー設定で簡単に変更できます: [Edit]メニュー > [Preferences] > [Keymap]。 "Select Side of frame" を検索し、新しいキーを割り当てます。

   .. You can also use :kbd:`Ctrl + LMB` at the *left* of the playhead to select all strips before the playhead or :kbd:`Ctrl + LMB` at the *right* of the playhead to select all strips after the playhead.

   Playheadの左側を :kbd:`Ctrl+LMB-Click` して Playheadの前のすべてのストリップを選択するか、Playheadの右側を :kbd:`Ctrl+LMB-Click` して Playheadの後のすべてのストリップを選択することもできます。

   .. To select all strips located at the position of the playhead, choose the submenu  *Current Frame*. There is no shortcut key associated by default.
   再生ヘッドの位置にあるすべてのストリップを選択するには、 [Current Frame]サブメニュー を選択します。デフォルトでは関連付けられたショートカット キーはありません。

   .. The menu equivalent is Select > Side of Frame (see figure 2), with options: Left, Right or Current Frame.
   メニューは [Select] > [Side of Frame] (図) で、オプションは [Lef]、[Right]、または [Current Frame] です。

チャンネル内のストリップを選択
   .. Select strips in the same channel laying left and/or right of the selected strips.
   選択されているストリップと同じチャンネルで左右に並んでいるストリップを選択します。

   .. The menu equivalent is Select > Channel (see figure 2), with options: Left, Right or Both Sides. The difference with the previous command is that the selection is taken as reference; not the playhead.
   メニューは [Select] > [Channel] (図 2) で、オプションは [Left]、[Right]、または [Both Sides] です。前のコマンドとの違いは、選択されたストリップが基準となることです。Playheadではありません。

   .. Use this command to select all strips in the channel of the active strip by choosing the both sides option.
   このコマンドを使用して、[Both Sides]オプションを選択してアクティブなストリップのチャンネル内のすべてのストリップを選択します。

リンクされたストリップを選択
   .. :kbd:`Ctrl + L` will select all the strips in the same channel that are connected with the Active Strip, meaning there are no gaps between them.
   :kbd:`Ctrl + L` は、アクティブ ストリップに接続されている同じチャンネル内のすべてのストリップを選択します。
   つまり、それらの間にギャップがないことを意味します

   .. The menu equivalent is: Select > Linked > All.
   メニューは [Select] > [Linked] > [All] です。

   .. Todo::
      .. The menu Select > Linked > Less and More seem to be doing nothing.
      [Select] > [Link] > [Less and More] メニューは何も実行していないようです。

リンクされたストリップを垂直方向に選択
   .. The shortcut key :kbd:`Ctrl+LMB` + Click on a strip will select all above and below it, if the have exactly the same Start and End time. The clicked strip becomes selected and active. This shortcut is not exposed in the menu.
   ストリップを :kbd:`Ctrl+LMB` クリックすると、開始時刻と終了時刻がまったく同じであれば、その上下のすべてが選択されます。クリックしたストリップが選択され、アクティブになります。このショートカットはメニューには表示されません。



属性ベースの選択
.........................

.. figure:: /images/video_editing_edit_montage_select_select-menu-attribute-based.svg
   :alt: Select Attribute Based

   図4 属性ベースの選択


.. With these commands you can select strips according to their relation with other strips and their strip type. First select a strip and press  :kbd:`Shift-G` or use the menu Select > Grouped (see figure 3).
これらのコマンドを使用すると、他のストリップとの関係およびストリップのタイプに従ってストリップを選択できます。まずストリップを選択し、 :kbd:`Shift-G` を押す か、 [Select] メニュー > [Grouped] を使用します (図 3)。

Type
   .. Selects all strips of the same type as the active strip within a category. For example, if you have a speed control strip selected, this command will select all other speed control strips but not the Transform or Cross Transition strips.
   カテゴリ内のアクティブなストリップと同じタイプのストリップをすべて選択します。たとえば、スピード コントロール ストリップを選択している場合、このコマンドは他のすべてのスピード コントロール ストリップを選択しますが、トランスフォーム ストリップやクロス トランジション ストリップは選択しません。

Global Type
   .. With this command you can differentiate between Audio strips and the rest (Movie, Image, Effect, ...). To select all audio strips, make sure that the Active Strip is an audio strip and issue this command.
   このコマンドを使用すると、オーディオ ストリップと残りの部分 (ムービー、画像、エフェクトなど) を区別できます。すべてのオーディオ ストリップを選択するには、アクティブ ストリップがオーディオ ストリップであることを確認して、このコマンドを発行します。

Effect Type
   .. Selects *all* effect strips. Please note that Text and Color strips are also considered as Effect strips.
   すべてのエフェクト ストリップを選択します。テキストおよびカラー ストリップも効果ストリップとして考慮されることに注意してください。

Data
   .. Selects strips that share the same data, for example, two image strips sharing the same image file. This could be handy if you have used the same file on different places; e.g. a logo image.
   同じデータを共有するストリップ、たとえば、同じ画像ファイルを共有する 2 つの画像ストリップを選択します。これは、同じファイルを別の場所で使用した場合に便利です。たとえば、ロゴ画像など。

Effect
   .. Selects all strips that have the same effect applied as the Active Strip. For example, if the Active Strip has a Blur effect, this command will select all other strips with a Blur effect.
   アクティブ ストリップと同じエフェクトが適用されているすべてのストリップを選択します。たとえば、アクティブ ストリップにブラー エフェクトがある場合、このコマンドはブラー エフェクトを持つ他のすべてのストリップを選択します。


Effect/Linked
   .. Selects other strips affected by the active one (sharing some time and below or effect-assigned.
   アクティブなストリップの影響を受ける他のストリップを選択します（一定時間以下またはエフェクトが割り当てられているものを共有します）。

   .. Select all strips within time range and with lower channel of initial selection. Then select effect chains of these strips.
   時間範囲内で、初期選択ストリップの下位チャンネルを持つすべてのストリップを選択します。次に、これらのストリップのエフェクト チェーンを選択します。

   .. Todo::
      .. Explain in more detail.
      もっと詳しく説明してください。

Overlap
   .. Selects any strips that occur on the same frame as the current. Note that the current frame is always in reference to the Start frame of the active strip. It does not correspondent with the playhead position.
   現在と同じフレーム上にあるストリップを選択します。現在のフレームは常にアクティブなストリップの開始フレームを参照していることに注意してください。再生ヘッドの位置とは対応しません。

ストリップハンドルを選択
....................

.. figure:: /images/video_editing_edit_montage_select_select-menu-handles.svg
   :alt: Select Handles

   図4 ハンドルの選択

.. The strip handles are the small darker colored bars at the left and right of the strip. You can use them to create :ref:`Offsets <time-panel>` for the strip. You can select the handles-only with several commands (see figure 4).

ストリップ ハンドルは、ストリップの左右にある小さな暗い色のバーです。それらを使用して、ストリップの :ref:`Offsets <time-panel>` を作成できます。いくつかのコマンドを使用してハンドルのみを選択できます (図4)。

.. Note::
   .. The visualization of the strip handles have been `discussed <https://developer.blender.org/D7401>`_ and reworked already a few times but they still do not look as polished as in some other editors. On HDPI monitors they are quite small and do not scale in relation with the zoom level. The cursor also don't give any clue if it is above the handle or the strip body.
   ストリップ ハンドルの視覚化についてはすでに `discussed <https://developer.blender.org/D7401>`_ され、作り直されていますが、まだ他のエディタほど洗練されていません。 HDPI モニターでは非常に小さく、ズーム レベルに応じて拡大縮小されません。また、カーソルがハンドルの上にあるのか、ストリップ本体の上にあるのかはわかりません。

:kbd:`LMB` + Click
   .. Just like selecting a strip, clicking with the :kbd:`LMB` in the 'neighborhood' of a handle will select this handle. The handle becomes white. Holding down :kbd:`Shift` will select multiple handles.
   ストリップを選択するのと同じように、ハンドルの「付近」を :kbd:`LMB` クリックすると、このハンドルが選択されます。ハンドル部分が白くなります。:kbd:`Shift` 押しながら:kbd:`LMB` クリックすると、複数のハンドルが選択されます。

   .. If just one handle is selected, moving the strip after selecting will change the strip's length. If both handles (left and right) are selected the strip will move and behave as if the entire strip was selected with the regular Box Select.

   ハンドルが 1 つだけ選択されている場合、選択後にストリップを移動すると、ストリップの長さが変更されます。両方のハンドル (左と右) が選択されている場合、ストリップは移動し、通常のボックス選択でストリップ全体が選択されているかのように動作します。

:kbd:`Alt` - :kbd:`LMB`
   .. Using the Alt-key in combination with left click above a strip will select the strip handles of the strip *and* its neighbors. This is handy shortcut to trim the neighbor strips.

   Alt キーとストリップの上の左クリックを組み合わせて使用​​すると、ストリップとその隣接するストリップのストリップ ハンドルが選択されます。これは、隣接するストリップをトリミングするための便利なショートカットです。

Box Select (Include Handles) :kbd:`Ctrl-B`
   .. Works the same as *Box Select* (see above) but it selects only the strip's handles that fall within the region.
   ボックス選択(上記参照)と同じように機能しますが、領域内にあるストリップのハンドルのみを選択します。

   .. But, with this Box select, it is also possible to select the right handle of a strip and the left handle of its successor. Moving this selection (with :kbd:`G` or :kbd:`LMB`) will trim the left strip, if moving left or the right strip, if moving right. We cover these techniques in more detail in section: Edit > Assembling > Cutting.

   ただし、このボックス選択を使用すると、ストリップの右ハンドルと後続のストリップの左ハンドルを選択することもできます。この選択範囲を (:kbd:`G` または  :kbd:`LMB` を使用してLMB) 移動すると、左に移動した場合は左のストリップがトリミングされ、右に移動した場合は右のストリップがトリミングされます。これらのテクニックについては、Edit > Assembling > Cutting のセクションで詳しく説明します。

Handle
   .. This command operates on the Active strip. You could choose between Both, Left or Right. This will select the appropriate handles of the active strip itself. Or you can choose Both, Left or Right Neighbor. This will select the handles of the active strip and the appropriate handles of the neighbor strip.

   このコマンドはアクティブ ストリップ上で動作します。[Both]、[Left]、または[Right]から選択できます。これにより、アクティブなストリップ自体の適切なハンドルが選択されます。または、[Both Neighbor]、[Left Neighbor]または[Right Neighbor]を選択することもできます。これにより、アクティブなストリップのハンドルと隣接するストリップの適切なハンドルが選択されます。

   .. These operators are useful to change the timing of a cut by moving the handles after selecting them.
   これらのオペレータは、選択後にハンドルを移動してカットのタイミングを変更するのに便利です。

.. rubric:: 訳注

.. [#f1] Blender4.0では、ハンドルを選択後にストリップバーの中央を選択するとクリックすると、ストリップのボディーが選択されるようです。
