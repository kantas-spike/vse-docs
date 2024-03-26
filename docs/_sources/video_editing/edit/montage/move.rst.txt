Move
----

.. Moving strips in the timeline is of course a basic operation in video editing. Figure 1 shows a few possibilities. The yellow strip (1) at the left is dragged upon the left red & green strips. Before releasing, strip (2) with the move Cross is temporarily visible. Depending upon the the selected option (shuffle, overwrite, or expand), strips 3, 4 or 5 are the result.

タイムライン内でストリップを移動することは、もちろんビデオ編集の基本的な操作です。
図 1 は、いくつかの可能性を示しています。左側の黄色のストリップ (1) を、左側の赤と緑のストリップの上にドラッグします。リリースする前に、クロス移動?? を伴うストリップ (2) が一時的に表示されます。選択したオプション (shuffle、overwrite、または expand) に応じて、ストリップ (3)、(4)、または (5) が結果となります。

.. figure:: /images/video_editing_montage_move.svg
   :alt: Moving strips


   図1 シーケンサーでのストリップの移動

LMB - drag
   .. You can select one or more strips and drag them to a new location. Releasing the :kbd:`LMB` will place the strip at the new location. Pressing :kbd:`Escape` or :kbd:`RMB` (while still holding :kbd:`LMB`) will cancel the movement. From the moment, you start dragging a *Grab* operation (see below) is started and new options are available.

   1 つまたは複数のストリップを選択し、新しい場所にドラッグできます。
   :kbd:`LMB` を放すと、ストリップが新しい位置に配置されます。
   :kbd:`Escape` や :kbd:`RMB` (:kbd:`LMB` を押したまま）を押すと、移動がキャンセルされます。
   ドラッグを開始した瞬間から、*Grap* 操作 (以下を参照) が開始され、新しいオプションが使用可能になります。

Grab
   .. In figure 1 the yellow strip is selected and pressing :kbd:`G` key will *grab* the strip. Note that a status bar appears with some options, the header is temporarily replaced by a message (Sequence Slide: 0,0), the cursor shape changes to a move-icon and the Start and End frame appear within the strip. These are all signs that you are in Grab mode.

   図1 では、黄色のストリップが選択されており、 :kbd:`G` キーを押すとストリップが *grap* されます。
   ステータス バーがいくつかのオプションとともに表示され、ヘッダーが一時的にメッセージ (シーケンス スライド: 0,0) に置き換えられ、カーソルの形状が移動アイコンに変わり、開始フレームと終了フレームがストリップ内に表示されることに注意してください。
   これらはすべて、Grap モードであることを示すサインです。

   .. The Grab or G-command is universal in Blender and works the same in most editors. It is also accessible through the menu: Strip > Transform > Move.
   Grab または G コマンドは Blender で共通であり、ほとんどのエディターで同じように機能します。
   メニューからアクセスすることもできます: [Strip] > [Transform] > [Move]。

   .. * Select one or multiple strips. They can be in different channels. See section on `selecting <selecting>`_ for various methods. If you have selected with the mouse, you can release the mouse button.
   .. * Press :kbd:`G`. The location of the mouse pointer is irrelevant but it is good practice to have the mouse on top of the to-be-moved strip. The Move icon will then nicely follow the strip bar.
   .. * Move the mouse horizontally, vertically or both. The strip bar will jump to the next available channel and will be laid on top of existing strips. You can move past the border (although you want see where you will drop the strip).
   .. * Press :kbd:`Escape` or :kbd:`RMB` to cancel the movement or :kbd:`LMB - Click` or :kbd:`Enter` to confirm the operation. The selected strips will then be locked at the new location.
   * 1 つまたは複数のストリップを選択します。それらは異なるチャネルに存在する可能性があります。さまざまな方法については `selecting <selecting>`_ セクション を参照してください。マウスで選択した場合は、マウス ボタンを放しても問題ありません。
   * :kbd:`G` を押します。マウス ポインタの位置は関係ありませんが、移動するストリップの上にマウスを置くことをお勧めします。移動アイコンはストリップ バーにうまく追従します。
   * マウスを水平、垂直、またはその両方に動かします。ストリップ バーは、次に利用可能なチャンネルにジャンプし、既存のストリップの上に配置されます。境界線を越えて移動することもできます (ただし、ストリップをどこにドロップされるかは確認する必要があります)。
   * :kbd:`Escape` または :kbd:`RMB-Click` を押してキャンセルするか、:kbd:`LMB-Click` または :kbd:`Enter` 押して操作を確定します。選択したストリップは新しい位置でロックされます。

Grab - :kbd:`Shift`
   .. Moving a strip with the :kbd:`Shift` button pressed will move in small increments; eventually frame by frame. The increment size depends on the zoom level (larger steps when zoomed out).
   :kbd:`Shift` ボタンを押したままストリップを移動すると、少しずつ移動します。最終的にはフレームごとに。増分サイズはズーム レベルによって異なります (ズームアウトするとステップが大きくなります)。

Grab - :kbd:`Arrow Left/Right`
   .. After :kbd:`MMB - drag` or :kbd:`G`, you can move left or right by one frame with the :kbd:`Arrow - Left` or :kbd:`Arrow - Right`. This method won't work with the Up or Down arrow keys to change channel number.
   :kbd:`LMB-drag` または :kbd:`G` のあと、 :kbd:`Arrow-Left` または :kbd:`Arrow-Right` で左右に 1 フレームずつ移動できます。この方法は、上矢印キーまたは下矢印キーを使用してチャネル番号を変更することはできません。

Grab - number
   .. Pressing :kbd:`G`, followed by a positive number X will move the strip horizontally to the right with X frames. So G 10 will move the strip 10 frames to the right. A negative number will move the strips to the left. As always, finish with Escape to cancel or Enter (Click) to confirm.
   :kbd:`G` を押して、正の数値 X を押すと、ストリップが X フレーム右に水平に移動します。したがって、G 10 はストリップを 10 フレーム右に移動します。負の数を指定すると、ストリップが左に移動します。いつものように、Esc キーでキャンセルするか、Enter (クリック) で確定します。

Grab - X/Y
   .. You can restrain the movement to the horizontal X-axis or to the vertical Y-axis. So, Grab Y will move the selected strips vertically to a new channel, without changing horizontal position.
   水平 X 軸または垂直 Y 軸への移動を制限できます。したがって、Grab Y は、水平位置を変更せずに、選択したストリップを新しいチャンネルに垂直に移動します。

Grab - X/Y - number
   .. Combines the previous two commands. So, G Y 2 will move the strip 2 channels up and G X -10 will move the strip 10 frames to the left.
   前の 2 つのコマンドを結合します。したがって、GY 2 はストリップを 2 チャンネル上に移動し、GX -10 はストリップを 10 フレーム左に移動します。

   .. If you want to specify the movement in *seconds*, you can always enter the necessary calculation. Suppose, that your project has a fps = 24, then moving a strip 5 seconds is done by G X 5**24. You have to tap the multiply symbol twice (**)!
   移動範囲を秒単位で指定したい場合は、いつでも必要な計算を入力できます。プロジェクトの fps = 24 があり、ストリップの 5 秒間の移動は GX 5**24 によって行われるとします。乗算記号 (**) を 2 回タップする必要があります。

Snapping
........

.. figure:: /images/video_editing_montage_move-guides-icon.png
   :alt: Snapping guides
   :scale: 50%
   :align: right

   図 2: スナップ ガイド

.. If there is only one strip in the sequencer, then you can move that strip freely around and there will be no snapping. However, most of the time this is not the case and snapping could occur. The moving strip is suddenly clamped to another strip and the edges are aligned on consecutive frames. This occurs whenever those edges are within a distance of less than 15 pixels.
シーケンサー内にストリップが 1 つしかない場合は、そのストリップを自由に移動でき、スナップは発生しません。
ただし、ほとんどの場合はそうではなく、スナップが発生する可能性があります。
移動するストリップが突然別のストリップにクランプ(固定)され、エッジが連続するフレーム上で位置合わせされます。これは、これらのエッジが 15 ピクセル未満の距離内にある場合に常に発生します。

.. Snapping can also occur with the playhead. The moving strip is then aligned with the playhead, whenever one of the edges is within that distance of 15 pixels.
スナップは Playhead でも発生する可能性があります。次に、エッジの 1 つが 15 ピクセルの距離内にある場合は常に、移動ストリップが Playhead と位置合わせされます。

.. Snapping can be induced by *moving the strip* **or** by *moving the handles* (and thus changing the strip duration). The snapping can be visualized by a thin white line. Click on the magnet-icon in the middle of the header to turn on the snapping guides. You can also use the shortcut key :kbd:`Shift - Tab`  to toggle (see figure 2).

スナップは、 *ストリップを移動する*  か、*ハンドルを移動する* こと（つまり、ストリップの持続時間を変更すること） によって誘発することができます。スナップは細い白い線で視覚化できます。ヘッダーの中央にある磁石のアイコンをクリックして、スナップ ガイドをオンにします。ショートカット キー :kbd:`Shift-Tab` を使用して 切り替えることもできます (図 2)。

.. Holding down the :kbd:`Ctrl` key while moving a strip, will also toggle the *Show Guides* command. So, if *Show Guides* is enabled, you can disable it temporarily while moving the strip by holding down the :kbd:`Ctrl` key.

:kbd:`Ctrl` キーを押したままストリップを移動すると、スナップの有無 も切り替わります。したがって、[Use Snapping] が有効になっている場合は、 :kbd:`Ctrl` キーを押したままにしてストリップを移動している間、スナップを一時的に無効にすることができますCtrl。

.. The snapping guide will appear whenever an edge of the moving strip is close (< 15 pixels) to an edge of another strip (see figure 2). *All* channels are taken into account. So, in a crowded scene, there can be lot of snapping guides (but only those within 15 pixels are shown).

スナップ ガイドは、移動するストリップのエッジが別のストリップのエッジに近い (< 15 ピクセル) 場合に表示されます (図2)。すべてのチャネルが考慮されます。そのため、混雑したシーンでは、多数のスナップ ガイドが存在する可能性があります (ただし、15 ピクセル以内のガイドのみが表示されます)。

.. figure:: /images/video_editing_montage_move-snapping-guides.svg
   :alt: Snapping guides

   図3 スナップ ガイド

.. Figure 3 shows all possible snapping guides with 3 strips. The top-panel represents the original situation (before moving strip-3). Because there are two other strips, there are 8 possibilities to snap. The Start frame of strip-3 can snap to the Start and End frame of strip-2; and so can the End frame (= 4 possibilities; middle row in figure 2). The same reasoning holds for the edges of strip-1 (bottom row of figure 2).

図 3 は、3 本のストリップを備えたすべての可能なスナップ ガイドを示しています。上のパネルは、元の状況 (ストリップ 3 を移動する前) を表します。他に 2 つのストリップがあるため、スナップする可能性は 8 つあります。ストリップ 3 の開始フレームは、ストリップ 2 の開始フレームと終了フレームにスナップできます。終了フレーム (= 4 つの可能性、図 2 の中段) も同様です。同じ理由がストリップ 1 のエッジにも当てはまります (図 2 の下の行)。

.. (a) The Start frame of strip-3 is snapped to End frame of strip-2. Result: Strip-3 is appended to strip-2. This is in fact the original situation. Because there are no strips to the right of strip-2, this is a legal move and the border of strip-3 is colored in white.
(a) ストリップ 3 の開始フレームがストリップ 2 の終了フレームにスナップされます。結果: ストリップ 3 がストリップ 2 に追加されます。実はこれが本来の状況なのです。ストリップ 2 の右側にはストリップがないため、これは正当な動きであり、ストリップ 3 の境界線は白で色付けされます。

.. (b) The End frame of strip-3 is snapped to the End frame of strip-2. This could cause an Overwrite of strip-2; so the border of strip-3 is colored red. Result: because d1 > d2, strip-3 is moved to the next available location: End frame of strip-2.
(b) ストリップ 3 の終了フレームがストリップ 2 の終了フレームにスナップされます。これにより、strip-2 の上書きが発生する可能性があります。したがって、strip-3 の境界線は赤色になります。結果: d1 > d2 のため、ストリップ 3 は次の利用可能な位置、ストリップ 2 の終了フレームに移動します。

.. (c) The Start frame of strip-3 is snapped to Start frame of strip-2. This is again an illegal operation; so the border is red. Because d1 < d2, you should expect that strip-2 should be placed before strip-2. However, there is not enough room> and the result is that strip-3 is put back in its original location.
(c) ストリップ 3 の開始フレームがストリップ 2 の開始フレームにスナップされます。これもまた違法な操作です。したがって境界線は赤になります。d1 < d2 であるため、ストリップ 2 はストリップ 2 の前に配置されるはずです。しかし、十分なスペースがありません> ため、strip-3 は元の場所に戻されます。

.. (d) The End frame of strip-3 is snapped to the Start frame of strip-2. This could be a normal operation if the gap between strip-1 and strip-2 was big enough to hold strip-3. Unfortunately, this is not the case; so the border of strip-3 is colored red and the strip is once again appended to the End of strip-2.
(d) ストリップ 3 の終了フレームがストリップ 2 の開始フレームにスナップされます。ストリップ 1 とストリップ 2 の間のギャップがストリップ 3 を保持できるほど十分に大きい場合、これは正常な動作である可能性があります。残念ながら、そうではありません。したがって、ストリップ 3 の境界線は赤に色付けされ、ストリップは再びストリップ 2 の最後に追加されます。

.. (e) The Start frame of strip-3 is snapped to End frame of strip-1. As in (d), this could be a normal operation but again, the gap is not big enough; so strip-3 is moved again to the End of strip-2 and the border is colored red.
(e) ストリップ 3 の開始フレームがストリップ 1 の終了フレームにスナップされます。(d) と同様、これは通常の動作である可能性がありますが、やはりギャップは十分大きくありません。したがって、ストリップ 3 はストリップ 2 の最後に再び移動され、境界線は赤色になります。

.. (f) The End frame of strip-3 is snapped to the End frame of strip-1. This is an illegal operation because strip-1 could be overwritten. The border is colored red. Because d1 > d2, it should be moved at the end of strip-1. But there is not enough room; so, the other side is tried, which succeeds.
(f) ストリップ 3 の終了フレームがストリップ 1 の終了フレームにスナップされます。ストリップ 1 が上書きされる可能性があるため、これは不正な操作です。境界線は赤く色付けされます。d1 > d2 であるため、strip-1 の最後に移動する必要があります。しかし、十分なスペースがありません。したがって、反対側が試行され、成功します。

.. (g) The Start frame of strip-3 is snapped to Start frame of strip-1. Strip-1 could be overwritten; so the border of strip-3 is red. The result is that strip-3 is moved to the front of strip-1, because d1 < d2.>.
(g) ストリップ 3 の開始フレームがストリップ 1 の開始フレームにスナップされます。Strip-1 は上書きされる可能性があります。したがって、strip-3 の境界線は赤になります。その結果、d1 < d2.> であるため、ストリップ 3 はストリップ 1 の前に移動されます。

.. (h) The End frame of strip-3 is snapped to the Start frame of strip-1. There is plenty of room before strip-1; so this could be a normal operation (white border). Strip-3 is moved in front of strip-1.
(h) ストリップ 3 の終了フレームがストリップ 1 の開始フレームにスナップされます。ストリップ 1 の前には十分なスペースがあります。したがって、これは通常の動作である可能性があります (白い枠線)。ストリップ 3 はストリップ 1 の前に移動されます。

.. It's a little confusing that for example, the snapping guide in figure 3-d and 3-e seems to implicate that the moved strip will be inserted between strip-1 and strip-2. As explained above, this is not the case, *unless* you activate the Expand-mode (see later).
たとえば、図 3-d と 3-e のスナップ ガイドは、移動したストリップがストリップ 1 とストリップ 2 の間に挿入されることを暗示しているように見えるのは、少し混乱します。上で説明したように、拡張モードを有効にしない限り、これは当てはまりません(後述)。

.. The snapping guide tool has 5 options (see figure 2).
スナップ ガイド ツールには 5 つのオプションがあります (図2)。


.. * Current Frame: the playhead (= current frame) is counted as a supplemental edge to snap on. So, the moving strip can either be snapped to an edge of another strip or to the playhead, whichever is closest.
* Current Frame: Playhead (= 現在のフレーム) は、スナップオンする補助エッジとしてカウントされます。したがって、移動するストリップは、別のストリップの端またはPlayheadのいずれか最も近い方にスナップできます。


.. * Hold Offset: Strips can be the result of a Hold Split operation (see :ref:`Hold Split <hold-split-command>`). For example, in figure 4, the Hold Offset Start is at frame 1133 while the first 250 frames are freezed.
* Hold Offset: ストリップはホールド スプリット操作の結果である可能性があります (参照 :ref:`Hold Split <hold-split-command>`)。たとえば、図 4 では、最初の 250 フレームがフリーズされている間、ホールド オフセットの開始はフレーム 1133 にあります。


   .. figure:: /images/video_editing_montage_move-snapping-hold-split.svg
      :alt: Snapping Hold Split

      図 4: Hold Offset Start フィールドへのスナップ

.. * Muted strips/Sound Strips: when you move a strip, most of the time you don't want to snap this strip to Muted (hidden) or Sound strips. These options are *not* ignored by default, but you have switch them on here.
* Muted strips/Sound Strips: ストリップを移動するとき、ほとんどの場合、このストリップをミュート (非表示) またはサウンド ストリップにスナップする必要はありません。これらのオプションはデフォルトでは無視されませんが、ここでオンに切り替えます。

.. * Current Frame: Snap to Strips: *not* the strips are snapped, but the playhead is snapped to the strip edges *while scrubbing*. To see this happen, you need to scrub at a low speed; otherwise you will be past the edge before snapping could take place.
* Current Frame: Snap to Strips: ストリップはスナップされませんが、スクラブ中に Playhead がストリップの端にスナップされます。これが起こるのを確認するには、低速でスクラブする必要があります。そうしないと、スナップが行われる前にエッジを超えてしまいます。


Snap to the playhead
   .. There is also a special command to move and snap strips to the playhead at the same timeline. Select one or multiple clips. They can be spread over multiple channels. Press :kbd:`Shift - S` to snap the selection to the playhead.

   同じタイムラインでストリップをPlayheadに移動してスナップする特別なコマンドもあります。1 つまたは複数のクリップを選択します。複数のチャネルに拡散する可能性があります。 :kbd:`Shift-S` 押すと、選択範囲が Playhead にスナップされます。


   .. Warning::
      .. If multiple strips are selected, all of them will start at the playhead. The relative position to each other will not be preserved and all the strips are spread over different channels (because they will otherwise overlap); even if the snap option Expand or Overwrite is selected. This command is probably only useful for strips that share a common Start frame; eg. Movie strips with their accompanying Sound strips.
      複数のストリップが選択されている場合、それらはすべて Playhead から始まります。互いの相対位置は保持されず、すべてのストリップは異なるチャネルに分散されます (そうしないとオーバーラップしてしまうため)。スナップ オプションの [Expand] または [Overwrite] が選択されている場合でも同様です。このコマンドはおそらく、共通の開始フレームを共有するストリップにのみ役立ちます。例えば。ムービー ストリップとそれに付随するサウンド ストリップ。


Shuffle
.......

.. With the default Shuffle option selected, moving a strip around will always add the dropped strip to the front or back of another strip, never insert it between strips.
デフォルトのシャッフル オプションが選択されている場合、ストリップを移動すると、ドロップされたストリップは常に別のストリップの前面または背面に追加され、ストリップの間に挿入されることはありません。

.. admonition::
   Conflict resolution

   .. When the Shuffle option (default) is enabled, moving a strip, so that it (partially) overlap with another strip, will create a temporary red outline around the moving strip, indicating that the strip can't be moved there (without expending or overwriting) and will be placed further away and clamped to either side of the overlapping strip.
   Shuffle オプション (デフォルト) が有効になっている場合、別のストリップと (部分的に) 重なるようにストリップを移動すると、移動中のストリップの周囲に一時的な赤い輪郭が作成され、ストリップをそこに移動できないことを示します (Extend や Overwrite でないため)、さらに離れて配置され、重なっているストリップの両側に配置されます。

   .. Which side? Two distances are calculated; eg. d1 and d2 in figure 5. Because d2 is smaller than d1, the moving strip-1 will be appended at the end of strip-2 + strip-3 (if there is room). Moving strip-3 between strip-1 and strip-2 is a little more difficult to predict. If d3 < d4, then strip-3 will be placed before strip-1. Otherwise, it will be appended to strip-2.

   どちら側に配置される？ 2 つの距離が計算されます。例えば。図 5 の d1 と d2。d2 は d1 より小さいため、移動するストリップ 1 はストリップ 2 + ストリップ 3 の最後に追加されます (スペースがある場合)。ストリップ 3 をストリップ 1 とストリップ 2 の間で移動することは、予測が少し難しくなります。d3 < d4 の場合、ストリップ 3 はストリップ 1 の前に配置されます。それ以外の場合は、strip-2 に追加されます。

   .. figure:: /images/video_editing_montage_move-guides-snapping-side.svg
      :alt: Snapping side
      :align: center


      図5 シャッフル オプションを使用してストリップを挿入することはできません。

..
  The background of a moving strip is drawn semi-transparent
  if it overlaps with another strip. It's convenient to see what's
  underneath, especially with the Overwrite feature (see below).
..

移動するストリップの背景が別のストリップと重なる場合、その背景は半透明で描画されます。
特にOverwrite機能 (下記を参照) を使用する時に、下にあるものを確認するのに便利です。

Overwrite
.........

..
  The Overwrite option will replace portions of strips. In figure 1, the yellow strip is dropped upon the red and green strips and will replace the overlapping portions of them. There is no warning, but, of course, you can undo the operation.

  Multiple strips can be dropped; each overwriting the portions of strips that they are overlapping.
..
上書きオプションはストリップの一部を置き換えます。図 1 では、黄色のストリップが赤と緑のストリップの上にドロップされ、それらの重なっている部分を置き換えます。警告は表示されませんが、もちろん操作を元に戻すこともできます。

複数のストリップをドロップできます。それぞれが、重なっているストリップの部分を上書きします。

Expand
......

..
  The Expand option will never overwrite any strips but will move them out of place, in case they were overlapping. In figure 1, the dropped yellow strip will *expand* the original red-green sequence by moving the green strip to the right.

  The exact result of the operation, however, depends upon the drop location. If, for example, the yellow strip is dropped at the beginning of the red strip, then both red & green strips are moved to the right and the yellow strip is placed in front of them. If the yellow strip is dropped at the end of the green strip, then it will be added at the tail of the existing red-green strips. If it is dropped (as in the example of figure 1), then the green strip is moved to the right and the yellow strip is inserted.

  The Expand mode works also with multiple, selected clips. If there are any gaps between the moving strips, these will be preserved.
..
Expand オプションはストリップを上書きすることはありませんが、ストリップが重なっている場合には、ストリップを所定の位置から移動します。図 1 では、ドロップされた黄色のストリップは、緑のストリップを右に移動することによって、元の赤と緑のシーケンスを拡張します。

ただし、操作の正確な結果はドロップ位置によって異なります。たとえば、黄色のストリップが赤のストリップの先頭にドロップされた場合、赤と緑のストリップは両方とも右に移動され、黄色のストリップがそれらの前に配置されます。黄色のストリップが緑のストリップの最後に削除された場合、既存の赤と緑のストリップの最後に追加されます。これがドロップされると (図 1 の例のように)、緑色のストリップが右に移動され、黄色のストリップが挿入されます。

Expand モードは、選択した複数のクリップでも機能します。移動するストリップ間にギャップがある場合、それらは保持されます。

