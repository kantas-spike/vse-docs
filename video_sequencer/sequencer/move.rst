.. Move
移動
....

Numpad zero
   .. Pressing the :kbd:`Numpad zero` will pan the Visible Range, so that the playhead is at the center. You have to use the numpad, unless you have set ``Emulate Numpad`` in the User Preferences.

   :kbd:`Numpad zero` を押すと、Playheadが中心になるように表示範囲がパンされます。ユーザー設定で ``Emulate Numpad`` を設定していない限り、テンキーを使用する必要があります。

   .. hint::
      .. If you don't have a 3 button mouse or a numpad (e.g. you are working with a tablet and stylus on a laptop), you can enable ``Emulate 3 Button Mouse`` and/or ``Emulate Numpad`` in the `User Preferences <https://docs.blender.org/manual/en/dev/editors/preferences/input.html>`_. You can use then the regular numeric keys. Pressing the :kbd:`MMB` is simulated by pressing the :kbd:`Alt` key (not :kbd:`Alt Gr`) and the :kbd:`LMB` (or pressing the stylus) together and drag.

      3ボタンマウスまたはテンキーをお持ちでない場合 (たとえば、ラップトップでタブレットとスタイラスを使用して作業している場合)、`User Preferences <https://docs.blender.org/manual/en/dev/editors/preferences/input.html>`_ で ``Emulate 3 Button Mouse`` および/または  ``Emulate Numpad`` を有効にすることができます。通常の数字キーを使用できます。 :kbd:`MMB` を押すことは、:kbd:`Alt` キー ( :kbd:`Alt Gr` ではない) と :kbd:`LMB` を押して(またはスタイラスを押して) または、ドラッグすることによってシミュレートされます。

   .. warning::
      .. Aside from the menu View > Navigation > Goto Current Frame (= Numpad zero), there are no menu items that will move the Visible Range.

      メニューの [View] > [Navigation] > [Goto Current Frame] (= テンキーのゼロ) 以外には、表示範囲を移動するメニュー項目はありません。

MMB  drag
   .. Pressing the :kbd:`MMB` and dragging left or right will pan the Visible Range horizontally. Dragging up or down will move the window vertically. It is not that important where in the sequencer you click (center, top left, ...) because you can keep on dragging beyond the screen border. Of course, vertically, you cannot move further than channel 0, although it is possible to move beyond channel 32 (which is the highest channel you can put strips on).

   :kbd:`MMB` を押して左右にドラッグすると、表示範囲が水平にパンされます。上下にドラッグするとウィンドウが垂直に移動します。0画面の境界線を超えてドラッグし続けることができるため、シーケンサーのどこをクリックするか (中央、左上など) はそれほど重要ではありません。もちろん、垂直方向にはチャンネル 0 より先に移動することはできませんが、チャンネル 32 (ストリップを配置できる最高のチャンネル) を越えて移動することは可能です [#f1]_。

Ctrl - MMB + roll
   .. Pressing the :kbd:`Ctrl MMB` and roll with the wheel will pan the Visible Range horizontally.
   :kbd:`Ctrl` を押して、マウスホイールを回すと表示範囲がが水平にパンされます。

Shift - MMB + roll
   .. Pressing the :kbd:`Ctrl MMB` and roll with the wheel will pan the Visible Range vertically.
   :kbd:`Shift` を押して、マウスホイールを回すと表示範囲がが垂直にパンされます。

Scrollbars
   .. You can also use the horizontal or vertical scrollbars to move the Visible Range. Click at the scrollbar (not the circles) and drag. The width and location of the horizontal scrollbar gives you an indication of how much and what area the Visible Range occupies in the *Strip Range* (see below). The behavior of the scrollbars is somewhat counter-intuitive because it is based on the Strip Range.

   水平または垂直スクロールバーを使用して、表示範囲を移動することもできます。スクロールバー (両端の円部分ではなく) をクリックしてドラッグします。水平スクロールバーの幅と位置によって、表示範囲が *Strip Range* 内でどれだけの範囲とどの領域を占めるかがわかります(以下を参照)。スクロールバーの動作は、 *Strip Range* に基づいているため、いくぶん直観に反しています。

   .. Note::
      .. The Strip Range is calculated as follows:
      Strip Rangeは次のように計算されます。

      - 水平: 開始から終了まで (デフォルトではフレーム 1 からフレーム 250 まで)
      - 垂直: チャンネル 1 ～ 7 [#f2]_

      .. This range is *extended* by any strip outside this range. So, if you add a strip at frame 400 and channel 9, the Strip Range will be extended to frames (0 - 400) and channels (0 - 9).

      この範囲は、この範囲外のストリップによって *拡張* されます。したがって、フレーム 400 とチャンネル 9 にストリップを追加すると、Strip Rangeはフレーム (0 ～ 400) とチャンネル (1 ～ 9) に拡張されます。 [#f2]_

      .. Please note that, if you set your project End at frame 10 000, the horizontal scrollbar will be very small, even if you only have strips.
      プロジェクトの終了をフレーム 10 000 に設定すると、ストリップしかない場合でも、水平スクロールバーが非常に小さくなることに注意してください。

.. Figure 2 shows a project with a span of 100 frames (Start=1; End= 100). Since there are no strips, the Strip Range runs from frame 1 to 100 and from channel 0 to 7 (but this is irrelevant in this example).
図2 は、100 フレームの幅を持つプロジェクトを示しています (開始 = 1、終了 = 100)。ストリップがないため、ストリップ範囲はフレーム 1 から 100、チャンネル 1 から 7 までとなります (ただし、これはこの例では関係ありません)。[#f2]_

.. figure:: /images/editors_vse_sequencer_timeline_scrollbar.svg
   :alt: scrollbars

   図2: Sequencerの水平スクロールバー

.. Because the Visible Range covers only frames 30 - 50, 80% of Strip Range will be hidden (30% from the Start and 50% from the End). Only 20% of the Strip Range is visible. The scrollbar hints to this: the length covers 4 frames. This is 20% of 20 frames, which is the length of the Visible Range. The scrollbar starts at frame 36, which is 6 frames or 30% from the start.

表示範囲はフレーム 30 ～ 50 のみをカバーするため、ストリップ範囲の 80% が非表示になります (開始から 30%、終了から 50%)。Strip Rangeの 20% のみが表示されます。スクロールバーはこれを示唆しています。長さは 4 フレームをカバーしています。これは、表示範囲の長さである 20 フレームの 20% です。スクロールバーはフレーム 36 から始まります。これは、開始から 6 フレームまたは 30% です。

.. Dragging with the little circles at both ends of the scrollbar will zoom in or out. We discuss this behavior in the next section.
スクロールバーの両端にある小さな円をドラッグすると、拡大または縮小します。この動作については次のセクションで説明します。

.. rubric:: 脚注

.. [#f1] Blender4.0では、チャンネルは1〜128が利用可能です。
.. [#f2] Blender4.0では、チャンネルは1はじまりのため、チャンネル0はチャンネル1に書き換えています。
