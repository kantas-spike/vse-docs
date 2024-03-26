Copy - Paste
------------

.. You can copy/paste strips and keyframes within a scene and between scenes and projects. The latter two are a bit more complicated.
シーン内、およびシーンとプロジェクト間でストリップとキーフレームをコピー/ペーストできます。後の 2 つは少し複雑です。

.. Within the same scene
同じシーン内
.....................

.. To copy and paste a strip within the same scene:
同じシーン内でストリップをコピーして貼り付けるには:

.. * Select the strip or strips.
.. * Press :kbd:`Ctrl-C` or menu Strip > Copy or :kbd:`RMB` and select Copy.
.. * Move the playhead to the desired location
.. * Press :kbd:`Ctrl-V` or menu Strip > Paste or :kbd:`RMB` and select Paste.
* 1 つまたは複数のストリップを選択します。
* :kbd:`Ctrl-C` を押すか、 [Strip]メニュー > [Copy] または :kbd:`RMB-Click` 後に[Copy] を選択します
* Playhead を目的の位置に移動します。
* :kbd:`Ctrl-V` を押すか、[Strip]メニュー > [Paste]  または、 :kbd:`RMB-Click` 後に [Paste]を選択します。

.. To duplicate a strip within the same scene
同じシーン内でストリップを複製するには

.. * Select the strips or strips.
.. * Press :kbd:`Shft - D` or menu Strip > Duplicate Strips or :kbd:`RMB` and select Duplicate Strips.
.. * Move the strip by simply moving the mouse (no click or drag). The strip(s) will follow the mouse cursor. When in position, :kbd:`LMB-Click`.
* ストリップを選択します。
* :kbd:`Shft-D` を押すか、[Strip]メニュー > [Duplicate Strips] または、 :kbd:`RMB-Click` 後に [Duplicate Strips]を選択します。
* マウスを動かすだけでストリップを移動できます (クリックやドラッグは不要)。ストリップはマウス カーソルに従います。所定の位置に来たときに、:kbd:`LMB-Click` で配置できます。

.. The result of Duplicate and Copy/Paste is the same. Duplicate however is a bit easier and requires less mouse clicks.
複製とコピー/ペーストの結果は同じです。ただし、複製の方が少し簡単で、マウスのクリック数も少なくなります。

.. There seems to be no **Cut and paste** equivalent. For that operation, you have to copy/paste first the strips and then delete the old strip.
**カットアンドペースト** に相当するものはないようです。この操作では、最初にストリップをコピー/ペーストしてから、古いストリップを削除する必要があります。

.. Important::
   .. The Copy-Paste and Duplicate command will copy the associated keyframes of the source strip (BUT only within the same scene). For example, if the copy-strip has a rotation animation, then animation will be copied and duplicated to the destination strip. The position of the keyframes is calculated relative to the visual start of the strip.
   コピー＆ペーストおよび複製コマンドは、ソース ストリップの関連するキーフレームをコピーします (ただし、同じシーン内のみ)。たとえば、コピー ストリップに回転アニメーションがある場合、アニメーションはコピーされて宛先ストリップに複製されます。キーフレームの位置は、ストリップの視覚的な開始点を基準にして計算されます。


.. Between scenes
異なるシーン間
..............

.. To copy and paste a strip between two scenes:
2 つのシーン間でストリップをコピーして貼り付けるには

.. * Select the strip or strips in the source-scene.
.. * Press :kbd:`Ctrl-C` or menu Strip > Copy or :kbd:`RMB` and select Copy.
.. * Change the scene and move the playhead to the desired location
.. * Press :kbd:`Ctrl-V` or menu Strip > Paste or :kbd:`RMB` and select Paste.
* ソースシーンで 1 つまたは複数のストリップを選択します。
* :kbd:`Ctrl-C` を押すか、 [Strip]メニュー > [Copy] または :kbd:`RMB-Click` 後に [Copy]を選択します。
* シーンを変更し、Playheadを目的の位置に移動します。
* :kbd:`Ctrl-V` を押すか、[Strip]メニュー > [Paste]  または、 :kbd:`RMB-Click` 後に [Paste]を選択します。


.. Important::
   .. 1. You *cannot* use the Duplicate command top make copies between scenes.
   .. 2. Keyframes are *not* copied to the destination strip.
   1. Duplicate コマンドを使用してシーン間でコピーを作成することはできません。
   2. キーフレームは宛先ストリップにはコピーされません。

.. You can use the following work-around to copy the keyframes.
次の回避策を使用してキーフレームをコピーできます。

.. * First; copy and paste the strips as in the workflow from above. Keyframes are not copied.
.. * Select the destination strip and create at least one keyframe for the desired attribute; e.g. rotation. If there are keyframes on multiple attributes, you have to repeat this step for all the attributes that have keyframes.
.. * Switch to the source scene and open the Timeline Editor or the Dope Sheet Editor in a separate window. There, you will see the keyframes.
.. * Make a copy of the keyframes (:kbd:`Ctrl-C`).
.. * Switch to the destination scene, select the destination strip and position the playhead where you want the keyframes to start.
.. * Paste the keyframes (:kbd:`Ctrl-V`).If the keyframe from step 2 is within the range of the copied keyframes, it will be overwritten; else you have to manually delete it.
.. * Repeat the above steps for all attributes.
* 初めに、上記のワークフローのように、ストリップをコピーして貼り付けます。キーフレームはコピーされません。
* 宛先ストリップを選択し、目的の属性に対して少なくとも 1 つのキーフレームを作成します。例えば回転。複数のアトリビュートにキーフレームがある場合は、キーフレームを持つすべてのアトリビュートに対してこの手順を繰り返す必要があります。
* ソース シーンに切り替えて、タイムライン エディタまたはドープ シート エディタを別のウィンドウで開きます。そこにキーフレームが表示されます。
* キーフレームを :kbd:`Ctrl-C` でコピーします。
* 目的のシーンに切り替え、目的のストリップを選択し、キーフレームを開始したい場所にPlayheadを配置します。
* :kbd:`Ctrl-V` で キーフレームを貼り付けます。手順 2 のキーフレームがコピーしたキーフレームの範囲内にある場合は上書きされます。それ以外の場合は、手動で削除する必要があります。
* すべての属性に対して上記の手順を繰り返します。

.. Between projects
異なるプロジェクト間
................

.. You *cannot* copy individual strips between projects. If you need a certain strip from another project, you have to copy the entire scene.
プロジェクト間で個々のストリップをコピーすることはできません。別のプロジェクトから特定のストリップが必要な場合は、シーン全体をコピーする必要があります。

.. * Append the project that contains the desired strip with the menu File > Append
.. * Select the appropriate project and the appropriate scene.
.. * If that scene name already exists in your project, it will be renamed to something as scene.001.
.. * Switch to that scene in the video editing workspace and copy the desired strips.
.. * Paste the strips in another scene (pay attention to the keyframes)
.. * Eventually, delete the appended scene.
* [File] > [Append] メニューを使用して、目的のストリップを含むプロジェクトを追加します。
* 適切なプロジェクトと適切なシーンを選択します。
* そのシーン名がプロジェクトにすでに存在する場合は、scene.001 という名前に変更されます。
* video Editing Workspace でそのシーンに切り替え、目的のストリップをコピーします。
* ストリップを別のシーンに貼り付けます (キーフレームに注意してください)
* 最終的には、追加したシーンを削除します。

