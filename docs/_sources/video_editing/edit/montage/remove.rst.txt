Remove/disable
--------------

.. Strips can be removed or disabled with the commands delete, Mute, and Lock.

ストリップは、削除、ミュート、およびロックのコマンドを使用して削除または無効にすることができます。

Delete
......

.. figure:: /images/video_editing_edit_montage_delete_delete.svg
   :alt: Strip menu
   :scale: 50%
   :align: right

   図1 ストリップ メニュー

.. Deleting one or multiple selected strips is done by pressing the :kbd:`X` key or the :kbd:`Delete` key or with the menu Strip > Delete or the context menu with :kbd:`RMB + Click` (see figure 1).

1 つまたは複数の選択したストリップを削除するには、 :kbd:`X` キーまたは :kbd:`Delete` キーを押すか、 [Strip]メニュー > [Delete] または :kbd:`RMB + Click` でコンテキスト メニューを使用します(図1)。

.. This Delete operation can of course be undone with the Undo command or :kbd:`Ctrl Z` key. Deleting a strip that has an associated effect (e.g. Glow or Gaussian Blur) will also delete the effect strip.
もちろん、この削除操作は、[Undo] コマンドまたは :kbd:`Ctrl Z` キーを使用して元に戻すことができます。関連するエフェクト（Glow や Gaussian Blur など）を持つストリップを削除すると、エフェクト ストリップも削除されます。


.. The *preferred* key for deletion is X and not Delete because the X key can be accessed easily with the left hand on a standard (Qwerty) keyboard. That way, you don't have to release the mouse in your right hand (of course, if you are right-handed).

X キーは標準 (Qwerty) キーボードの左手で簡単にアクセスできるため、削除に推奨されるキーは Delete ではなく X です。そうすれば、右手でマウスを放す必要がなくなります (もちろん、右利きの場合)。

Mute
....

.. figure:: /images/video_editing_edit_montage_delete_mute-lock.svg
   :alt: Mute-lock menu
   :align: right

   図2  ミュートとロック メニュー

.. The Mute command will make a strip invisible in the preview. The command was previously called *Hide*, which you can deduce from the shortcut key (H). The strip is still visible in the time line (a little bit greyed out; see figure 2) but it will not contribute to the image in the preview. The effect of the Mute command is the same as clicking on the Mute icon in the Strip properties (see figure 2). If you want to apply the Mute on all selected strips, you have to press the :kbd:`Alt` key while clicking the icon. You can mute the selected strips or the inverse: the unselected strips.

[Mute] コマンドを使用すると、プレビューでストリップが非表示になります。
このコマンドは以前は *Hide* と呼ばれていましたが、これはショートカット キー (H) から推測できます。ストリップはタイムラインにまだ表示されていますが (少しグレー表示されています。図 2 を参照)、プレビューの画像には表示されません。 [Mute] コマンドの効果は、ストリップ プロパティの [Mute] アイコンをクリックした場合と同じです (図 2 を参照)。選択したすべてのストリップにミュートを適用したい場合は、 :kbd:`Alt` キーを押しながら、アイコンをクリックする必要があります。選択したストリップをミュートすることも、その逆、選択されていないストリップをミュートすることもできます。

.. - Mute/Unmute Strips (kbd:`H`, :kbd:`Alt-H`): mute or unmute the selected strips. The strips will be (in) visible in the preview.
.. - Mute/Unmute Deselected Strips (:kbd:`Shift-H`, :kbd:`Ctrl-Alt-H`): mute or unmute all strips but the selected.
- Mute/Unmute Strips (kbd:`H`, :kbd:`Alt-H`): 選択したストリップをミュートまたはミュート解除します。ストリップはプレビューに表示されます。
- Mute/Unmute Deselected Strips (:kbd:`Shift-H`, :kbd:`Ctrl-Alt-H`): 選択したストリップを除くすべてのストリップをミュートまたはミュート解除します。

Lock
....

.. The Lock command prevents the strip from being moved in time or that the duration could be changed. The effect of the Lock command is the same as clicking on the Lock symbol in the Time panel (see figure 2) of the strip properties. If you want to apply the Lock on all selected strips, you have to press the :kbd:`Alt` key while clicking the Lock symbol. The strip is shown as striped in the sequencer.

Lock コマンドは、ストリップが時間内に移動されたり、持続時間が変更されたりすることを防ぎます。 Lock コマンドの効果は、ストリップ プロパティの [Time] パネル (図 2 を参照) で [Lock] シンボルをクリックした場合と同じです。選択したすべてのストリップにロックを適用したい場合は、 :kbd:`Alt` キーを押しながら、Lock 記号をクリックする必要があります。ストリップはシーケンサーではストライプとして表示されます。

.. - Lock Strips (:kbd:`Shift-L`): disables the strip from being changed.
.. - Unlock Strips (:kbd:`Shift-Alt-L`): enables disabled strips allowing them to be changed.
- Lock Strips (:kbd:`Shift-L`): ストリップの変更を無効にします。
- Unlock Strips (:kbd:`Shift-Alt-L`): 無効になっているストリップを有効にし、変更できるようにします。

**Remove gaps**

.. Remove blank columns in the timeline window, starting from project Start (usually frame 1). A blank column is a time/frame location where there isn't any strip in any channel. In other words, the Preview window is empty for that time/frame location.

プロジェクトの開始位置 (通常はフレーム 1) から開始して、タイムライン ウィンドウの空白列を削除します。空白の列は、どのチャンネルにもストリップがない時間/フレームの位置です。つまり、その時間/フレーム位置のプレビュー ウィンドウは空です。

.. You can invoke the command with the menu: Strip > Transform > Remove Gaps or with the :kbd:`Backspace` key. After the command is issued, you can tick the *All Gaps* option to remove other gaps or you can press :kbd:`Backspace` several times to remove the other gaps.

このコマンドは、[Strip]メニュー > [Transform] > [Remove Gaps] を使用するか、 :kbd:`Backspace` キーを使用して呼び出すことができます。
コマンドの発行後、[All Gaps]オプションにチェックを入れて他のギャップを削除するか、数回押してBackspace他のギャップを削除できます。

.. note::
   .. You can move strips between:
   ストリップは次の間で移動できます。[#f1]_

   .. * Scenes: copy the strips (:kbd:`Ctrl - C`), switch to the other scene and paste (:kbd:`ctrl - V`). All strip settings will be copied, *except* the animation keyframes.
   .. * Projects: import the scene with the wanted strips into the current project with the menu File > Append.
   * Scenes: ストリップをコピーし (:kbd:`Ctrl-C`)、他のシーンに切り替えて貼り付けます ( :kbd:`ctrl-V` )。アニメーションのキーフレームを除くすべてのストリップ設定がコピーされます。
   * Projects: メニューの [File] > [Append] を使用して、必要なストリップを含むシーンを現在のプロジェクトにインポートします。

.. rubric:: 訳注

.. [#f1] この省都関係のない noteになっているようです。
