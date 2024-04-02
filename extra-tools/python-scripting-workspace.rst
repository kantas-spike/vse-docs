*******************
Scripting Workspace
*******************

.. Blender has a dedicated workspace "Scripting" with 7 windows (areas): the Text Editor (middle area), the Info editor (left bottom), the Python console (left middle) and the 3D Viewport (left top). At the right you find the Properties window (bottom) and two versions of the outliner (top); see fig. 1.

Blender には、Text Editor (中央領域)、Info Editor (左下)、Python Console (左中央)、および 3D Viewport (左上) の 7 つのウィンドウ (領域) を備えた専用のワークスペース [Scripting] があります。右側には、[Properties] ウィンドウ (下) と 2 つのバージョンの[Outliner] (上) があります。図1 を参照してください。

.. figure::
    https://devtalk.blender.org/uploads/default/optimized/2X/6/65c4bd501c6df0b0aaa19baf4244f83589822595_2_1035x582.jpg
   :alt: The scripting workspace as defined in the call for workspaces in 2018

   図1 スクリプト ワークスペース (2021 年 2.92)

.. You can use the built-in text editor to write and test your code. But there are, of course numerous other code editors on the market such as Microsoft Visual Studio Code (VS Code), Atom, Sublime, ... and complete integrated code environments (IDE) such as Microsoft Visual Studio (not to be confused with VS Code), Eclipse, Pycharm, ...

組み込みのテキスト エディタを使用してコードを作成し、テストできます。しかし、もちろん、Microsoft Visual Studio Code (VS Code)、Atom、Sublime など、他にも多数のコード エディターが市場に出回っています。また、Microsoft Visual Studio (VS Code と混同しないでください) などの完全な統合コード環境 (IDE) も存在します。 )、Eclipse、Pycharm、…

.. There are also numerous addons for the Script Editor.
スクリプト エディター用のアドオンも多数あります。

.. - `TintwoTin <https://github.com/tin2tin/Script_Editing/>`_ has integrated a few free addons into a script editor template.
.. - `Blender Sensei <https://blendersensei.com/hacker-manual/>`_ has developed a very advanced but paid improvement of the script editor.

- `TintwoTin <https://github.com/tin2tin/Script_Editing/>`_ は、いくつかの無料アドオンをスクリプト エディター テンプレートに統合しました。
- `Blender Sensei <https://blendersensei.com/hacker-manual/>`_ は、スクリプト エディターの非常に高度ではあるが有料の改良版を開発しました。

.. How to use the script editor efficiently?
スクリプトエディタを効率的に使用するにはどうすればよいですか?
=========================================

.. note::
   .. In Blender, keystrokes are sent to the window where the mouse is over. This works very well in, for example, the 3D view but is contra-productive in the Scripting workspace. Each time I want to type something in the Python console, the mouse should be hoovering above that window. A click is not necessary or sufficient as in a standard GUI program.
   Blender では、キーストロークはマウスが置かれているウィンドウに送信されます。これは、たとえば 3D ビューでは非常にうまく機能しますが、スクリプト ワークスペースでは逆効果になります。Python コンソールに何かを入力するたびに、マウスはそのウィンドウの上に移動する必要があります。標準の GUI プログラムのように、クリックするだけでは十分ではありません。

.. Layout the workspace
ワークスペースをレイアウトする
--------------------

.. To minimize the above mentioned annoyance, I should rearrange the scripting workspace into two main windows (see fig 1). At the left is the editor for which you are writing code (for example the sequence editor). At the right is the text editor. If that isn't still enough space, you can always go full screen with Ctrl-Tab or Alt-Shift-Tab.

上記の煩わしさを最小限に抑えるには、スクリプト ワークスペースを 2 つのメイン ウィンドウに再配置する必要があります (図 1 を参照)。左側には、コードを作成しているエディター (シーケンス エディターなど) があります。右側にはテキストエディタがあります。それでも十分なスペースがない場合は、Ctrl-Tab または Alt-Shift-Tab を使用していつでも全画面表示にすることができます。

.. At first sight, you loose a few handy editors within hand reach, in particular the Python console. But for my taste, that area are too small in the default workspace. Besides, it's very easy to replace one of the big windows with another editor. The shortcut Shift-F4 replaces the window with the Python console. To return to the code editor, use Shift-F11. That way, you can keep the mouse cursor most of the time above the text editor (who will receive the keystrokes). For faster coding, it is best to keep the hands as much as possible on the keyboard.

一見すると、手の届く範囲にいくつかの便利なエディター、特に Python コンソールがなくなってしまいます。しかし、私の好みでは、デフォルトのワークスペースではその領域が小さすぎます。さらに、大きなウィンドウの 1 つを別のエディタに置き換えることも非常に簡単です。ショートカット Shift-F4 を使用すると、ウィンドウが Python コンソールに置き換えられます。コードエディタに戻るには、Shift-F11 を使用します。こうすることで、ほとんどの時間、マウス カーソルをテキスト エディター (キーストロークを受け取る人) の上に置くことができます。コーディングを高速化するには、できるだけ手をキーボードの上に置いたままにするのが最善です。

.. Use the Python console
Python コンソールを使用する
----------------------

.. Why would you need the Python console? Among other things (you can use it as a calculator for instance), it is a very handy tool to try things out. What again was the instruction to place the playhead at a certain frame in the Video Sequence Editor (VSE)? Change the text editor temporarily with the Python (Shift-F4), start typing: bpy.context. ... In case of doubt, press Tab to get a list of possible command (code completion). This is also one of the reasons why you need a large window; the code completion list can be quite long. You can't select one of the options, but you can type further and press tab to narrow down the list until you've got the actual keyword.

なぜ Python コンソールが必要なのでしょうか? とりわけ (たとえば、計算機として使用できます)、何かを試すのに非常に便利なツールです。ビデオ シーケンス エディター (VSE) の特定のフレームにPlayheadを配置するという指示は何だったのでしょうか? Python (Shift-F4) を使用してテキスト エディタを一時的に変更し、 "bpy.context" と入力し始めます。... 疑わしい場合は、Tab キーを押して、使用可能なコマンドのリスト (コード補完) を表示します。これも、大きな窓が必要な理由の 1 つです。コード補完リストは非常に長くなる場合があります。いずれかのオプションを選択することはできませんが、実際のキーワードが得られるまで、さらに入力して Tab キーを押してリストを絞り込むことができます。

.. note::
   .. Unfortunately the copy/paste and selection functions of the Python console are rather limited. Selection can only be done with the mouse (but see above). The shortcut Ctrl-Shift-C will copy the complete Python console buffer (the complete history; not the few commands that you see on the screen). You can clear the screen with the commands <code>import os</code> and <code>os.system('cls')</code> for Windows or <code>os.system('clear')</code> for Linux.
   残念ながら、Python コンソールのコピー/ペーストおよび選択機能はかなり制限されています。選択はマウスでのみ行うことができます (ただし、上記を参照)。ショートカット Ctrl-Shift-C を押すと、Python コンソール バッファ全体 (画面に表示されるいくつかのコマンドではなく、完全な履歴) がコピーされます。Windows の場合はコマンド  ``import os``  および  ``os.system('cls')``  または  ``os.system('clear')``  を使用して画面をクリアできます。 > Linuxの場合。

.. You can copy and paste complete code blocks (with for next loops, ...) to the Python console to run and test, for example to inspect the value of some variables.  Refrain however from using blanc lines. You can also run the complete open text editor code with the following command.
完全なコード ブロック (for next ループなど) をコピーして Python コンソールに貼り付けて、実行およびテストすることができます (たとえば、いくつかの変数の値を検査するなど)。ただし、白線の使用は避けてください。次のコマンドを使用して、完全なオープン テキスト エディター コードを実行することもできます。

``exec(compile(bpy.data.texts['Text'].as_string(), 'textblock', 'exec'))``

.. This will run the code from the open text editor window. You can use a `snippet addon <https://github.com/Pullusb/snippetsLibrary>`_ to store these snippets.
これにより、開いているテキスト エディタ ウィンドウからコードが実行されます。 `snippet addon <https://github.com/Pullusb/snippetsLibrary>`_ を使用して、これらのスニペットを保存できます。


.. Use autocompletion/intellisense
オートコンプリート/インテリセンスを使用する
-------------------------------

.. The text editor itself has autocompletion built-in but it is rather limited to the code objects from the file itself. You can install the `Intellisense for Blender Text Editor <https://github.com/tin2tin/Intellisense_for_Blender_Text_Editor>`_ addon by Mackraken and Tintwotin. This works nice albeit that you have to use a weird key combination to invoke it. Another method is presented by `GDQuest <https://www.youtube.com/watch?v=IQgLBnPO2uo>`_ which makes use of the fake bpy modules from `Nutti <https://github.com/nutti/fake-bpy-module>`_.

テキスト エディタ自体にはオートコンプリートが組み込まれていますが、それはファイル自体のコード オブジェクトに限定されています。Mackraken と Tintwotin による `Intellisense for Blender Text Editor <https://github.com/tin2tin/Intellisense_for_Blender_Text_Editor>`_ アドオンをインストールできます。これは、呼び出すために奇妙なキーの組み合わせを使用する必要があるにもかかわらず、うまく機能します。もう 1 つの方法は、 `Nutti <https://github.com/nutti/fake-bpy-module>`_ の`fake bpy modules` を利用することです。これは `GDQuest <https://www.youtube.com/watch?v=IQgLBnPO2uo>`_ で紹介されている。

.. You can also copy code (multiple lines) from the text editor and paste it in the Python console to execute it and to inspect some variables. Sometimes, this does not work very well (empty lines, ...). An alternative is to execute the following command in the console. This will run the open text file in the editor.

テキスト エディターからコード (複数行) をコピーし、Python コンソールに貼り付けて実行し、いくつかの変数を検査することもできます。場合によっては、これがあまりうまく機能しないことがあります (空行など)。別の方法としては、コンソールで次のコマンドを実行します。これにより、開いているテキスト ファイルがエディタで実行されます。

.. The Blender Sensei version of the text editor (see above) has also a very nice autocompletion function.
Blender sensei バージョンのテキスト エディター (上記を参照) にも、非常に優れたオートコンプリート機能があります。

`` exec(compile(bpy.data.texts['Text'].as_string(), 'textblock', 'exec'))``

.. How to use VS Code efficiently?
VS Code を効率的に使用するにはどうすればよいですか?
===============================

..
  There are, of course, several professional code editors on the market. Most of the time they work better, more fluently, have better support and endless extensions for the most diverse things. The only advantage of the Blender text editor is that it integrates smoothly with the other Blender modules and that running code is very easy. However, the integration of VS Code with Blender comes very closely to it.
  The setup is however a little more involved. `Michael Bridges <https://www.youtube.com/playlist?list=PLlu-PIRg8u2nVGQMKRhiqK0KhKqBZfkax>`_ has created three extensive tutorials for setting up VS Code & Blender on Windows, Linux and Mac.
..
もちろん、市場にはプロフェッショナルなコードエディタがいくつかあります。ほとんどの場合、それらはより適切に、より流暢に動作し、より優れたサポートと、最も多様なものに対する無限の拡張機能を備えています。Blender テキスト エディターの唯一の利点は、他の Blender モジュールとスムーズに統合され、コードの実行が非常に簡単であることです。ただし、VS Code と Blender の統合はそれに非常に近いものになります。ただし、セットアップはもう少し複雑です。 `Michael Bridges <https://www.youtube.com/playlist?list=PLlu-PIRg8u2nVGQMKRhiqK0KhKqBZfkax>`_ は、 Windows、Linux、Mac 上で VS Code と Blender をセットアップするための 3 つの広範なチュートリアルを作成しました。

.. On finishing this tutorial, VS Code with the Python extension and the fake-module autocompletion list is installed. You can then use VS Code in two ways:
このチュートリアルを完了すると、Python 拡張機能と `fake-module` のオートコンプリート リストを備えた VS Code がインストールされます。その後、VS Code を次の 2 つの方法で使用できます。

.. Use VS Code as a standalone editor
VS Code をスタンドアロン エディターとして使用する
----------------------------------

.. Write your code in VS Code, save it as a .py file, open that file in the Blender Text Editor, run it, edit it and save it again (attention: shortcut key is Alt-S). Continue in VS Code (the code is real-time updated), save it, switch to Blender text Editor, push Refresh button and continue. Of course, this doesn't offer much advantage except you are using the VS Code editor to enter code.

VS Code でコードを記述し、.py ファイルとして保存し、そのファイルを Blender テキスト エディターで開き、実行して編集し、再度保存します (注意: ショートカット キーは Alt-S です)。VS Code で続行し (コードはリアルタイムで更新されます)、保存して、Blender テキスト エディターに切り替え、更新ボタンを押して続行します。もちろん、VS Code エディターを使用してコードを入力する場合を除いて、これには大きな利点はありません。


.. Use VS Code as an integrated editor
VS Code を統合エディタとして使用する
-----------------------------------

.. First, you have to install the amazing Blender extension by Jaques Luke. Search in the extension library for Blender Development.
まず、Jaques Luke による素晴らしい Blender 拡張機能をインストールする必要があります。Blender 開発用の拡張ライブラリを検索します。

.. figure:: img/script_editor_VSCode_extension.png
   :scale: 50 %
   :alt: Blender extension for VSCode

   図2  VCode の Blender 拡張機能

.. Start an instance of Blender from within VS Code with the command (shortcut = Alt-Shift-P) and choose "Blender: Start". This will start up Blender and move the System Console of Blender into the terminal window of VS Code. You can now access the system console in the Terminal tab. The Python console is available under the debug console tab. You can creates other instances of Blender manually but remember that this particular instance of Blender can only be managed (closed for example) from within VS Code.

コマンド (ショートカット = Alt-Shift-P) を使用して VS Code 内から Blender のインスタンスを起動し、"Blender: Start"を選択します。これにより、Blender が起動し、Blender のシステム コンソールが VS Code のターミナル ウィンドウに移動します。これで、[Terminal] タブからシステム コンソールにアクセスできるようになります。Python コンソールは、[Debug Console] タブで利用できます。Blender の他のインスタンスを手動で作成することもできますが、Blender のこの特定のインスタンスは VS Code 内からのみ管理できる (たとえば閉じられる) ことに注意してください。

.. You can create a new empty script with the command "Blender: New Script" or open an existing script. Edit this script within VS Code. Set the correct context (eg VIDEO SEQUENCER, VIEW_3D, ...) with the command "Blender: Set Script Context" at the beginning of the script. You can run the script from within VS Code with the command "Blender: Run Script". If everything went well, your script will be executed within the Blender environment.  If there are any errors, they will be print in the System Console (Terminal) or the Python console (Debug console).

[Blender: New Script] コマンドを使用して新しい空のスクリプトを作成するか、既存のスクリプトを開くことができます。このスクリプトを VS Code 内で編集します。スクリプトの先頭で [Blender: Set Script Context] コマンドを使用して、正しいコンテキスト (例: VIDEO SEQUENCER、VIEW_3D など) を設定します。 [Blender: Run Script] コマンドを使用して、VS Code 内からスクリプトを実行できます。すべてがうまくいけば、スクリプトは Blender 環境内で実行されます。エラーがある場合は、システム コンソール (ターミナル) または Python コンソール (デバッグ コンソール) に出力されます。


.. figure:: img/script_editor_VSCode_terminal-1.png
   :alt: terminal window of Blender extension

   図3 terminal window of Blender extension

.. For debugging, you can set one or more breakpoints and start the script. The script will stop at the breakpoint. There you can inspect variables, and step through the code. Another debugger is made by `Alan <https://github.com/alanscodelog/blender-debugger-for-vscode>`_.

デバッグのために、1 つ以上のブレークポイントを設定してスクリプトを開始できます。スクリプトはブレークポイントで停止します。そこで変数を検査し、コードをステップ実行できます。別のデバッガは `Alan <https://github.com/alanscodelog/blender-debugger-for-vscode>`_ によって作成されました。
