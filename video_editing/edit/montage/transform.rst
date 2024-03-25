Transform
---------

.. We cover three operations in the Transform section: Split, Trim, and Group.
Transform セクションでは、Split、Trim、Group という 3 つの操作について説明します。


Split
.....
.. Splitting a strip is separating the strip into two parts at the position of the playhead. Both parts continue to function as independent strips (who shares the same source). Splitting can be done on all strip types. Splitting an effect strip however will also split the input strip of the effect and vice versa.

ストリップの分割とは、ストリップを再生ヘッドの位置で 2 つの部分に分割することです。両方のパートは引き続き独立したストリップ（同じソースを共有する）として機能します。分割はすべてのストリップ タイプで実行できます。ただし、エフェクト ストリップを分割すると、エフェクトの入力ストリップも分割され、その逆も同様です。

.. In previous versions of Blender and also in a substantial part of the literature this operation was called "Cutting".  In a computer environment however this term is primarily used in the sense of copy-cut-paste, where it implicates delete. So, the term *Split* is preferred, although it stays very visible in terms such as *Jump Cut*, *J- or L-Cut*, ....

Blender の以前のバージョンや文献の大部分では、この操作は "Cutting" と呼ばれていました。
ただし、コンピュータ環境では、この用語は主にコピー、カット、ペーストの意味で使用され、削除を意味します。
したがって、 *Split* という用語が好まれますが、 *Jump Cut*、 *J-Cut* 、 *L-Cut* などの用語でも非常に目立つままです。


.. There are two variants of the command: Split and Hold Split.
このコマンドには、Split と Hold Split の 2 つのバリエーションがあります。

Split :kbd:`K`
   .. With the menu :menuselection:`Strip --> Split` or the shortcut key :kbd:`K` you can split the selected strip in two at the current frame. This will result in two strips which use the same source, fitting the original strip's timing and length.

   [Strip] メニュー  > [Split] またはショートカット :kbd:`K` キーを使用して、選択したストリップを現在のフレームで 2 つに分割できます。これにより、同じソースを使用する 2 つのストリップが作成され、元のストリップのタイミングと長さに適合します。

   .. warning::
      .. If you are using the shortcut :kbd:`K`, then it matters which side of the playhead the mouse cursor is (see figure 1). If the cursor is at the left hand side of the playhead, then the left strip is the active one (white outline & text overlay) and therefore also selected. If the mouse cursor is at the right of the playhead, then the right strip is the selected strip (orange outline)  *but* not the active one (no white text overlay). Contrary to what you might suspect, the Time fields then relate to the left strip; not the (selected) right strip.

      ショートカット :kbd:`K` を使用している場合は、マウス カーソルが Playhead のどちら側にあるかが重要になります (図 1)。
      カーソルが Playhead の左側にある場合、左側のストリップがアクティブなストリップ (白い輪郭とテキスト オーバーレイ) になるため、これも選択されます。
      マウス カーソルが Playhead の右側にある場合、右側のストリップは選択されたストリップ (オレンジ色の輪郭) ですが、アクティブなストリップではありません (白いテキスト オーバーレイはありません)。予想に反して、Time フィールドは左側のストリップに関連付けられます。（選択された）右側のストリップではありません。


   .. figure:: /images/video_editing_edit_montage_splitting_split.svg
      :alt: Split command

      図 1: Split コマンドの前後のストリップ プロパティ

   .. Please note, that in figure 1 the result right after the Split command is issued, is shown in the second column. In the third column the right part of the Split is deleted. In the fourth column, the left part is deleted and the right strip is made the active one.

   図 1 では、Split コマンドが発行された直後の結果が 2 列目に示されていることに注意してください。3 番目の列では、分割の右側の部分が削除されます。4 番目の列では、左側の部分が削除され、右側のストリップがアクティブになります。

   .. Also note that the Start frame of the left and right strip is the same: frame 1; even though the right strip starts visually at frame 8. This is accomplished with the Strip Offset Start field. And likewise, the premature ending of the left strip is done with the Strip Offset End field.

   また、左右のストリップの開始フレームが同じであることにも注意してください: フレーム 1; 右ストリップは視覚的にはフレーム 8 から始まりますが、これは Strip Offset Start フィールドで実現されます。同様に、左側のストリップの途中での終了は、Strip Offset End フィールドで行われます。

   .. From either part of the split, you can restore the entire original strip. It suffices to reset the Strip Offset fields to zero. This can also be done by dragging the left or right handle.

   分割のどちらかの部分から、元のストリップ全体を復元できます。Strip Offset フィールドをゼロにリセットするだけで十分です。これは、左ハンドルまたは右ハンドルをドラッグしても実行できます。



.. _hold-split-command:

Hold Split :kbd:`Shift-K`
   .. The menu :menuselection:`Strip --> Hold Split` or the shortcut :kbd:`Shift-K` splits a strip in two distinct strips; however you will not be able to drag the handles to show the frames past the split of each resulting strip.

   [Strip] メニュー  > [Hold Split] またはショートカット :kbd:`Shift-K` キーを使用して、選択したストリップを現在のフレームで 2 つに分割できます。ただし、ハンドルをドラッグして、結果として得られる各ストリップの分割を超えたフレームを表示することはできません。

   .. figure:: /images/video_editing_edit_montage_splitting_hold-split.svg
      :alt: Hold Split command

      図2 Hold Split コマンドの前後のストリップ プロパティ

   .. There are *subtle* differences between figure 1 and 2: the resulting strips are almost mirrored. Also, note that the first left part is renamed. For the Strip command, the most important part of the split operation seems to be the first (left) part. For the Hold Split command it is the second part.

   図 1 と図 2 の間には微妙な違いがあります。結果として得られるストリップはほぼ鏡像になっています。また、最初の左側の部分の名前が変更されていることに注意してください。Strip コマンドの場合、Split 操作の最も重要な部分は最初 (左側) の部分のようです。Hold Split コマンドの場合、これは 2 番目の部分です。

   .. The Start frame of the second (right) part and the End frame of the first (left) part are recalculated with the Hold Offset Start and Hold Offset End value. The name *Hold* indicates that the Start and End frame are fixed. The strip will start or end there and dragging the handles will not reveal any new frames.

   2 番目 (右) パーツの開始フレームと最初 (左) パーツの終了フレームは、ホールド オフセット開始値とホールド オフセット終了値を使用して再計算されます。Holdという名前は、開始フレームと終了フレームが固定されていることを示します。ストリップはそこで開始または終了し、ハンドルをドラッグしても新しいフレームは表示されません。

   .. As in the Split command, from either part of the Hold Split, you can restore the entire original strip. It suffices to reset the Hold Offset fields to zero. This *cannot* be done by dragging the left or right handle. The result of dragging is that the first or last frame is duplicated, inducing a Freeze Frame effect (see :ref:`(see Time panel of Movie strip <time-panel>` for more info).

   Split コマンドと同様に、Hold Split のどちらかの部分から、元のストリップ全体を復元できます。Hold Offset フィールドをゼロにリセットするだけで十分です。これは、左右のハンドルをドラッグしても実行できません。ドラッグの結果、最初または最後のフレームが複製され、フリーズ フレーム効果が引き起こされます (詳細については、 :ref:`(see Time panel of Movie strip <time-panel>` を参照してください)。

*Freeze frames*

   .. Suppose that you have the following strip (see figure 3) and you want to introduce some freeze frames effect.
   次のストリップ (図 3 を参照) があり、freeze frames エフェクトを導入するとします。

   .. figure:: /images/video_editing_edit_montage_splitting_freeze.svg
      :alt: Freeze frames
      :align: center

      図3 フリーズ フレームの例

   .. The Freeze at the Start and End of the strip is easy. You only have to drag the handles to introduce a Still Offset (see :ref:`Time Panel > Still Offset <time-panel>` for more detailed information. The left panel of figure 3 has a still Offset Start of 3 frames and so has the Still Offset End field of the right panel.

   ストリップの最初と最後でのフリーズは簡単です。ハンドルをドラッグするだけで静止オフセットを導入できます (詳細については、 :ref:`Time Panel > Still Offset <time-panel>` を参照してください。図 3 の左側のパネルには 3 フレームの still Offset Start フィールドがあり、右側のパネルの Still Offset End フィールドもあります)  [#f1]_ 。


   .. The Freeze in the middle of the strip is more complicated. First, you need a Hold Split at frame 6 (playhead at 7) of the original strip. That way there is a Hold flag on frame 6 so that dragging the right handle will duplicate frame 6. You need this Hold flag on the left part of the split e.g. freeze.001. This is a Hold Offset End value of 4 because the original strip was 10 frames long.

   ストリップの中央のフリーズはさらに複雑です。まず、元のストリップのフレーム 6 (再生ヘッドは 7) でホールド スプリットが必要です。そうすれば、フレーム 6 にホールド フラグが存在するため、右ハンドルをドラッグするとフレーム 6 が複製されます。このホールド フラグは、freeze.001 などの分割の左側の部分に必要です。元のストリップの長さが 10 フレームだったので、これは Hold Offset End 値 4 です。

   .. The strip in figure 3 has a brown color because it is an image sequence. You can add the Still Offset fields to the Time panel with a little Python code (see :doc:`useful scripts </extra-tools/python-useful-scripts>` ).

   図 3 のストリップは画像シーケンスであるため、茶色になっています。小さな Python コードを使用して、[Still Offset fields] フィールドを [Time] パネルに追加できます ( :doc:`useful scripts </extra-tools/python-useful-scripts>` を参照) [#f1]_ 。


*Classic Cuts*

   Jump Cut
      ..
        A jump cut is a cut in film editing in which a single continuous sequential shot of a subject is broken into two parts, with a piece of footage being removed in order to render the effect of jumping forward in time. ... Jump cuts tend to draw attention to the constructed nature of the film. (From `Wikipedia <https://en.wikipedia.org/wiki/Jump_cut>`_) In essence, a jump cut allows the editor to jump forward in time.

        It can also be used in conversations and interviews, to jump from the perspective of speaker 1 to that of speaker 2.
      ..
      ジャンプ カットは、映画編集におけるカットであり、被写体の 1 つの連続した連続ショットが 2 つの部分に分割され、時間内で前方向にジャンプする効果を表現するために映像の一部が削除されます。… ジャンプカットは、映画の構成的な性質に注意を向けさせる傾向があります。( `Wikipedia <https://en.wikipedia.org/wiki/Jump_cut>`_ より) 本質的に、ジャンプ カットを使用すると、編集者は時間を前に進めることができます。

      また、会話やインタビューで、話者 1 の視点から話者 2 の視点にジャンプするために使用することもできます。

   L-cut and J-cut
      ..
        In an L-cut, you are hearing the audio from the previous shot, even though you are viewing another shot. The name of the L-cut is derived from the shape of the resulting edit (see figure 4)

        A J-Cut is essentially the opposite of an L-Cut. Here you hear the audio before you see the video. So, the audience is is looking at strip 2 but still hearing audio from strip 1 (see figure 4).
      ..
      L カットでは、別のショットを見ている場合でも、前のショットの音声が聞こえます。L カットの名前は、編集結果の形状に由来しています (図 4 を参照)。

      J カットは本質的に L カットの逆です。ここでは、ビデオを見る前に音声が聞こえます。したがって、聴衆はストリップ 1 を見ていますが、ストリップ 2 からの音声が聞こえてきます (図 4 を参照)。

      .. figure:: /images/video_editing_edit_montage_splitting_j-l-cut.svg
         :alt: J- & L-cut

         図4 L カットと J カットの例

   Action cut
      .. An action cut is made when you cut in the middle of an action to another shot that matches the first shot's action.
      アクション カットは、アクションの途中で最初のショットのアクションと一致する別のショットにカットするときに作成されます。


Trim
----

.. Trimming is changing the duration of a strip by altering the In and Out point. In figure 1, the original strip of channel 2 starts at frame 1 and has a duration of 11138 frames. It is duplicated to channel 3 and trimmed. The new In point is at frame 2226 (1 + Strip Offset Start) and the new Out point at frame 7665 (Duration - Strip Offset End). As already discussed in the section on the :ref:`Time panel <time-panel>` or the :doc:`Split operation  </video_editing/edit/montage/striptypes/movie>` trimming and splitting is done with the use of the Strip Offset fields.

トリミングとは、インポイントとアウトポイントを変更してストリップの長さを変更することです。図5 では、チャネル 2 の元のストリップはフレーム 1 で始まり、継続時間は 11138 フレームです。チャンネル 3 に複製され、トリミングされます。新しいイン ポイントはフレーム 2226 (1 + ストリップ オフセット開始) にあり、新しいアウト ポイントはフレーム 7665 (継続時間 - ストリップ オフセット終了) にあります。 :ref:`Time panel <time-panel>` または :doc:`Split operation  </video_editing/edit/montage/striptypes/movie>` のセクションですでに説明したように、TrimとSplitは「Strip Offset」フィールドを使用して行われます。

.. figure:: /images/video_editing_edit_montage_trimming.png
   :alt: Example of trimming

   図5 ムービー ストリップのトリミング

.. Trimming of strips is mostly done with the mouse. You can however also change the Strip Offset fields directly by entering a value with the keyboard or use the slider of the property. Values can be negative. This will result in duplicating (freezing) the first and/or last frame.

ストリップのトリミングは主にマウスで行われます。ただし、キーボードで値を入力するか、プロパティのスライダーを使用して、[Strip Offset]フィールドを直接変更することもできます。値は負の値になる場合があります。これにより、最初および/または最後のフレームが複製 (フリーズ) されます。

.. :kbd:`LMB Click` on handles and dragging
:kbd:`LMB Click` によるハンドルのドラッグ

    .. The *Strip Offset Start* property of a strip could be selected by :kbd:`LMB Click` on the left handle of the strip. In figure 1 this handle has a white color for the selected and active strip and an orange color for the selected but non-active strip. Holding the LMB down and then moving the mouse left/right changes the IN point of the selected strips by the number of frames you moved it. The frame number label at the bottom left corner of the strip displays the frame number of the new IN point, only if the height of the strip bar is sufficient (see figure 1).

    ストリップの [Strip Offset Start]プロパティは、ストリップの左側のハンドルを :kbd:`LMB Click` で選択できます。
    図 5 では、このハンドルの色は、選択されアクティブなストリップについては白色、選択されているが非アクティブなストリップについてはオレンジ色となっています。LMB を押したままマウスを左右に動かすと、選択したストリップの IN ポイントが移動したフレーム数だけ変更されます。ストリップ バーの高さが十分な場合にのみ、ストリップの左下隅にあるフレーム番号ラベルには、新しい IN ポイントのフレーム番号が表示されます (図 5 を参照)。

    .. If you have a 20-image sequence strip, and drag the left handle to the right by 10 frames, the strip will start at image 11 (images 1 to 10 will be skipped). Use this to clip off a roll-up or undesired lead-in. Dragging the left arrow left will create a lead-in (copies) of the first frame for as many frames as you drag it. Use this when you want some frames for a transition at the start of the clip.

    20 個の画像シーケンス ストリップがある場合、左ハンドルを右に 10 フレーム分ドラッグすると、ストリップは画像 11 から始まります (画像 1 ～ 10 はスキップされます)。これを使用して、ロールアップまたは不要なリードインを切り取ります。左にドラッグすると、ドラッグした数のフレームの最初のフレームのリードイン (コピー) が作成されます。クリップの開始時にトランジション用にいくつかのフレームが必要な場合にこれを使用します。

    .. The *Strip Offset End* of a strip could be selected by :kbd:`LMB Click` on the right handle of the strip; holding it down (or pressing G grab) and then moving the mouse changes the OUT point within the strip. The frame number label at the bottom right corner of the strip displays the frame number of the OUT point.

    ストリップの[Strip Offset End]は、 ストリップの右側のハンドルを :kbd:`LMB-Click` で選択できます。それを押したまま（または G グラブを押して）マウスを動かすと、ストリップ内の OUT ポイントが変更されます。ストリップの右下隅にあるフレーム番号ラベルには、OUT ポイントのフレーム番号が表示されます。

    .. Dragging the right arrow to the left shortens the clip; any original images at the tail are ignored. Use this to quickly clip off a roll-down. Dragging the right arrow to the right extends the clip. For movies and images sequences, more of the animation is used until exhausted. Extending a clip beyond its end results in Blender making a copy of the last image. Use this for transitions out of this clip.

    右ハンドルを左方向にドラッグするとクリップが短くなります。末尾にある元のイメージは無視されます。これを使用すると、ロールダウンを素早く切り取ることができます。右ハンドルを右にドラッグすると、クリップが延長されます。ムービーや画像シーケンスの場合、使い果たされるまでさらに多くのアニメーションが使用されます。クリップを終端を超えて延長すると、Blender は最後の画像のコピーを作成します。このクリップからのトランジションにこれを使用します。

    .. You can select multiple left or right handles of different strips with :kbd:`Shift LMB`. The selected handles are colored: white for the active strip and orange for the non-active strips. :kbd:`LMB Click & drag` on any selected handle will move all selected handles in the same direction as your mouse movement and with the number of frames that the mouse is moved.
    :kbd:`Shift LMB` を使用して、異なるストリップの複数の左ハンドルまたは右ハンドルを選択できます。
    選択されたハンドルは色付けされます。アクティブなストリップは白、非アクティブなストリップはオレンジになります。
    選択したハンドル上で :kbd:`LMB Click & drag` すると、選択したすべてのハンドルがマウスの移動と同じ方向に、マウスが移動したフレーム数だけ移動します。

.. note::
    .. Selecting handles can be done with the :kbd:`LMB`, the special Box Select with Handles (:kbd:`Ctrl B`) or the the menu Select > Handle; see section on :doc:`Selecting <select>` for more details.
    :kbd:`LMB`  によるハンドルの選択は、 特別なボックス選択 ( :kbd:`Ctrl B` )、または [Select]メニュー > [Handle] を使用して行うことができます。詳細については、 :doc:`Selecting <select>` のセクションを参照してください。

.. :kbd:`LMB Click` on handles and :kbd:`G` (Grab)
:kbd:`LMB Click` による handles 選択 と :kbd:`G` (Grab)
    .. In stead of :kbd:`LMB Click` on handles and dragging, you could also select all handles and press :kbd:`G`. This will result in the same trimming. The advantage is that you don't need to click and drag on a strip area. It is sufficient to press :kbd:`G` and move the mouse (where ever it is positioned).
    :kbd:`LMB Click`でハンドルを選択してドラッグする代わりに、すべてのハンドルを選択して :kbd:`G` を押すこともできます。
    これにより、同じトリミングが行われます。利点は、ストリップ領域をクリックしてドラッグする必要がないことです。:kbd:`G` を押して、マウスを動かすだけで十分です(マウスの位置はどこでも)。

.. :kbd:`LMB Click` on strips and :kbd:`E` (Extend)
:kbd:`LMB Click` による handles 選択 と :kbd:`E` (Extend)
    .. You can move or extend/shorten (thus, trimming) selected strips *without* selecting the handles with the :kbd:`E` key or the menu Strip > Transform > Move/Extend from Current Frame key. However, the position of the Current Frame (playhead) and the initial mouse position are important here.
    :kbd:`E` キーまたは [Strip]メニュー > [Transform] > [Move/Extend from Current Frame] キーを使用してハンドルを選択しなくても、選択したストリップを移動または延長/短縮 (つまりトリミング) できます。ただし、ここでは現在のフレーム (Playhead) の位置とマウスの初期位置が重要です。

   .. - If the playhead is outside the range of the selected strips, the :kbd:`E` will move the all selected strips in the direction of the mouse movement. This mimics the move behavior of an entire strip with :kbd:`G` key.
   .. - If the playhead is within the range of (some) selected strips, the :kbd:`E` key will trim the selected strips. If the mouse is at the left side of the playhead, the IN points of the selected strips will follow the direction of the mouse (as if trimming with the left strip handle). If the mouse is at the right side of the playhead, the OUT point will follow the direction of the mouse (as if trimming with the right strip handle).
   - Playhead が選択したストリップの範囲外にある場合、 :kbd:`E` は選択したすべてのストリップがマウスの移動方向に移動します。これは、:kbd:`G` キーによるストリップ全体の移動動作を模倣します。
   - Playhead 選択した（一部の）ストリップの範囲内にある場合、:kbd:`E` キーは選択したストリップをトリミングします。マウスが再生ヘッドの左側にある場合、選択したストリップの IN ポイントはマウスの方向に従います (左側のストリップ ハンドルでトリミングするかのように)。マウスが再生ヘッドの右側にある場合、OUT ポイントはマウスの方向に従います (右のストリップ ハンドルでトリミングするかのように)。

    .. In summary, all selected strip handles from the “mouse side” of the current frame indicator (playhead) will transform together, to move or extend/shorten the selected strips.
    要約すると、現在のフレーム インジケーター (Playhead) の「マウス側」から選択されたすべてのストリップ ハンドルが一緒に変形し、選択されたストリップを移動または延長/短縮します。

Clear strip offsets: :kbd:`ALT O`
    .. All the trimming of selected strips can be cleared with the :kbd:`Alt O` or the menu Strip > Transform > Clear Strip Offset. The Strip Offset Start and End fields are reset to zero for the selected strips.
    選択したストリップのすべてのトリミングは、 :kbd:`Alt O` または [Strip]メニュー > [Transform] > [Clear Strip Offset] を使用してクリアできます。選択したストリップの[Strip Offset Start]フィールドと[Strip Offset End]フィールドがゼロにリセットされます。

.. Precision trimming
精密なトリミング
    .. Although the movie strips of the sequencer timeline can display thumbnails (Show Overlay > Thumbnails), trimming with precise visual feedback is not possible with these thumbnails.
    Sequencer タイムラインのムービー ストリップにはサムネイルを表示できますが ([Show Overlay] > [Thumbnails])、これらのサムネイルでは正確な視覚的フィードバックを伴うトリミングはできません。

    .. The Preview window however only shows the Current Frame (frame at the position of the playhead) by default. With the menu View > Preview during Transform of the Preview window, you can enable precision trimming. The Preview window will temporarily display the frame at the position of the selected handle of the active strip (see figure 2).
    ただし、デフォルトでは、Preview ウィンドウには現在のフレーム (Preview の位置にあるフレーム) のみが表示されます。Preview ウィンドウのメニューの [View] > [Preview during Transform] を使用すると、精密トリミングを有効にすることができます。Preview ウィンドウには、アクティブなストリップの選択したハンドルの位置にフレームが一時的に表示されます (図6 を参照)。


.. figure:: /images/video_editing_edit_montage_trimming_preview_during_transform.gif
   :alt: Preview during Transform

   図6: 変換中のプレビューを有効にしてトリミング (Tin2Tin の例)


:kbd:`Esc`
    .. Pressing :kbd:`Esc` *while* trimming will reset the strip handles to the original position and will cancel the trim operation.
    トリミング中に :kbd:`Esc` を押すと、ストリップ ハンドルが元の位置にリセットされ、トリム操作がキャンセルされます。



Group
.....

.. _bpy.types.MetaSequence:

.. Selected strips can easily be grouped together into one so-called meta strip with :kbd:`Ctrl-G`. A Meta Strip is a strip that can contain multiple strips, but is treated as if it was one strip. The max number of strips that can be grouped is 128, due to the max number of available channels in the sequencer. The duration of the Meta strip will span from the earliest Start time until the latest End time of any strip.

選択したストリップは、 :kbd:`Ctrl-G` を使用して 1 つのいわゆるメタ ストリップに簡単にグループ化できます。
メタ ストリップは、複数のストリップを含めることができるストリップですが、1 つのストリップであるかのように扱われます。
Sequencer で使用可能なチャンネルの最大数により、グループ化できるストリップの最大数は 128 です。メタ ストリップの長さは、ストリップの最も早い開始時間から最も遅い終了時間までとなります。

.. figure:: /images/video_editing_edit_montage_grouping.png
   :align: center

   図1 メタ ストリップの例

.. The Metaaaa strip has a very specific appearance because the channels of the grouped strips are represented by small horizontal bars within the Meta strip. In figure 1, the grouped strips occupy 4 channels, so the Meta strip contains 4 (small) horizontal bars. The grouped strips themselves are represented by their own color in the Meta strip. For example, the two purple areas at the top come from the text strips at channel 6. The color of the Meta strip itself is blueish purple, which covers the areas where no grouped strip is available. If there is only one strip to group, then the color of the Meta strip is very similar to the grouped strip (most of the time a little darker) and it's hard to recognize a Meta strip as such.

Meta ストリップは、グループ化されたストリップのチャネルが Meta ストリップ内の小さな水平バーで表されるため、非常に特殊な外観を持っています。
図 1 では、グループ化されたストリップが 4 つのチャネルを占有するため、メタ ストリップには 4 本の (小さな) 水平バーが含まれています。
グループ化されたストリップ自体は、メタ ストリップ内で独自の色で表されます。
たとえば、上部の 2 つの紫色の領域は、チャンネル 6 のテキスト ストリップからのものです。メタ ストリップ自体の色は青みがかった紫で、グループ化されたストリップが利用できない領域をカバーしています。グループ化するストリップが 1 つだけの場合、メタ ストリップの色はグループ化されたストリップと非常に似ており (ほとんどの場合、少し暗い)、メタ ストリップ自体を認識するのは困難です。

.. The Meta strip replaces the selected strips in the sequencer timeline and is placed at the channel of the active strip. This could result in somewhat unexpected positions when box selecting the group (the active strip isn't changed by box selecting).

メタ ストリップは、Sequencer タイムラインで選択したストリップを置き換え、アクティブなストリップのチャンネルに配置されます。
これにより、グループをボックス選択するときに、多少予期しない位置が発生する可能性があります (アクティブなストリップはボックス選択によって変更されません)。

.. note::
   .. Figure 1 is a bit misleading because a Meta strip and the grouped strips could never be visible at the same time in the timeline. The Meta strip *replaces* the grouped strips.
   図 1 は、メタ ストリップとグループ化されたストリップがタイムラインで同時に表示されることはないため、少し誤解を招きます。メタ ストリップは、グループ化されたストリップを置き換えます。

   .. Figure 1 is made by creating a Meta strip, duplicating it and un-meta-ing the duplicate.
   図 1 は、メタ ストリップを作成し、それを複製し、その複製をメタ化解除することによって作成されます。



.. The Meta strip is in fact a completely new strip with its own (independent) properties such as position X & Y, scale, rotation, .... It's like if the grouped strips are rendered out and the render result is imported back into the timeline as a new (meta) strip. For example, increasing the duration of the grouped strips *after* creating the Meta strip will *not* increase the duration of the Meta strip. You have to do that manually by dragging the strip handles.

実際、メタ ストリップは、位置 X と Y、スケール、回転などの独自の (独立した) プロパティを備えた完全に新しいストリップです。
これは、グループ化されたストリップがレンダリングされ、そのレンダリング結果が新しい (メタ) ストリップとしてタイムラインにインポートされるようなものです。
たとえば、メタ ストリップの作成後にグループ化されたストリップの長さを増やしても、メタ ストリップの長さは長くなりません。ストリップ ハンドルをドラッグして手動で行う必要があります。

.. Meta strips can be nested. For example, you can copy one Meta strip and paste it into another.
メタ ストリップはネストできます。たとえば、1 つのメタ ストリップをコピーして、別のメタ ストリップに貼り付けることができます。

Make Meta Strip :kbd:`Ctrl-G`
   .. To create a Meta strip, select all the strips you want to group, and bd:`Ctrl-G` to group them. The Meta strips will span from the beginning of the first strip to the end of the last one, and condenses all channels into a single strip. The Meta strip is placed at the channel of the active strip.
   メタ ストリップを作成するには、グループ化するすべてのストリップを選択し、 :kbd:`Ctrl-G` を押してグループ化します。メタ ストリップは、最初のストリップの始まりから最後のストリップの終わりまで続き、すべてのチャンネルが 1 つのストリップに凝縮されます。メタ ストリップは、アクティブ ストリップのチャネルに配置されます。

UnMeta Strip :kbd:`Ctrl-Alt-G`
   .. Separating (ungrouping) the Meta strip restores the strips to their relative positions and channels. This can be used if you choose to delete a Meta strip and want to keep the strips inside.
   メタ ストリップを分離 (グループ解除) すると、ストリップが相対的な位置とチャンネルに復元されます。これは、メタ ストリップを削除することを選択し、内部のストリップを保持したい場合に使用できます。

   .. Be aware that effects added to the Meta strip will be removed.
   メタ ストリップに追加されたエフェクトは削除されることに注意してください。

Edit a Meta strip :kbd:`Tab`
   .. You can edit the content inside a Meta strip by pressing :kbd:`Tab`. This will expand the strip to the original group and hide any other strips. To exit the Meta strip press :kbd:`Tab` again. Meta strips can also be nested, which make editing them a little confusing. To exit out one level of Meta Strip make sure you do not have a Meta strip selected when you press :kbd:`Tab` (select nothing or anoter regulare strip).
   :kbd:`Tab` を押すと、メタ ストリップ内のコンテンツを編集できます。
   これにより、ストリップが元のグループに展開され、他のストリップが非表示になります。メタ ストリップを終了するには、Tabもう一度押します。
   メタ ストリップはネストすることもできるため、編集が少し混乱します。
   メタ ストリップの 1 レベルを終了するには、押したときにメタ ストリップが選択されていないことを確認してくださいTab(何も選択しないか、別の通常のストリップを選択します)。

.. Warning::
   .. Adding effects e.g. Glow to a Meta strip is possible but the effects will be removed if you unMeta the strip.
   メタ ストリップにグローなどのエフェクトを追加することは可能ですが、メタ ストリップを解除するとエフェクトは削除されます。

   .. The default blend mode for a Meta strip is Replace (all strips below will not be visible). There are many cases where this alters the results of the animation so be sure to check the results and adjust the blend mode if necessary.
   メタ ストリップのデフォルトのブレンド モードは置換です (以下のすべてのストリップは表示されません)。これによりアニメーションの結果が変わる場合が多いため、必ず結果を確認し、必要に応じてブレンド モードを調整してください。

   .. Because of the above, adding a new strip to an existing meta strip should not be done by unMeta, followed by adding the new strip and recreate the Meta strip again. Better is to copy the new strip (on the clipboard), go into the Meta strip (Tab), paste the new strip and go out of the the Meta strip.
   上記のため、既存のメタ ストリップに新しいストリップを追加は、メタストリップは利用せず、
   その後新しいストリップを追加してメタ ストリップを再度再作成する必要があります。新しいストリップを (クリップボード上に) コピーし、メタ ストリップ (タブ) に移動し、新しいストリップを貼り付けて、メタ ストリップから出る方が良いでしょう。

.. The Meta strip is primarily an organization tool but has numerous other use cases.
メタ ストリップは主に整理ツールですが、他にも多数の使用例があります。

.. * If you are using a lot of strips with complicated arrangement, you can group them together using Meta strips. It allows you to reduce the vertical space used in the Sequencer.
.. * You can extend the limit of 128 channels with Meta Strips. The grouped strips will occupy only one channel.
.. * A Meta strip is a handy way to keep audio and video together in a synced way. Unfortunately, you will loose the advantage of thumnails.
.. * You can use it for adding speed effects in a simpler manner. See `Blender Frenzy <https://www.youtube.com/watch?v=jnrOzrPDAA0>`_ for a detailled tutorial about the procedure.
.. * One convenient use for Meta strips is when you want to apply the same effect to multiple strips. It is much more convenient to apply a single set of effects to one Meta strip than applying it to each individual strip. It is also possible to do the similar task described above with an Adjustment Layer.
* 複雑な配置で多数のストリップを使用している場合は、メタ ストリップを使用してそれらをグループ化できます。これにより、シーケンサーで使用される垂直方向のスペースを削減できます。
* メタ ストリップを使用すると、128 チャンネルの制限を拡張できます。グループ化されたストリップは 1 つのチャンネルのみを占有します。
* メタ ストリップは、オーディオとビデオを同期した状態に保つための便利な方法です。残念ながら、サムネイルの利点が失われます。
* より簡単な方法で Speed Effect を追加するために使用できます。手順の詳細なチュートリアルについては、 `Blender Frenzy <https://www.youtube.com/watch?v=jnrOzrPDAA0>`_ を参照してください。
* メタ ストリップの便利な使い方の 1 つは、複数のストリップに同じ効果を適用したい場合です。エフェクトのセットを 1 つのメタ ストリップに適用する方が、個々のストリップに適用するよりもはるかに便利です。調整レイヤーを使用して、上記と同様のタスクを実行することもできます。



.. rubric:: 脚注

.. [#f1] Blender4.0では、 [Still Offset Start/End]フィールドは廃止されています。代わりに[Strip Offset Start/End]フィールドに負の値を設定します。
