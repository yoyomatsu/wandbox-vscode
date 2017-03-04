# wandbox-vscode ( [🇬🇧 English](https://github.com/wraith13/wandbox-vscode/blob/master/README.md) )
[![](http://vsmarketplacebadge.apphb.com/version/wraith13.wandbox-vscode.svg) ![](http://vsmarketplacebadge.apphb.com/installs/wraith13.wandbox-vscode.svg) ![](http://vsmarketplacebadge.apphb.com/rating/wraith13.wandbox-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=wraith13.wandbox-vscode)

[Wandbox](http://melpon.org/wandbox)([GitHub](https://github.com/melpon/wandbox/)) はソーシャルコンパレーションサービスです。このエクステンションは Visual Studio Code の為の Wandbox フロントエンドです。

> Wandbox は [@melpon](https://github.com/melpon)( 🐕 犬) が個人的に無償(自腹)で提供しているサービスです。
> このサービスが提供され続ける為、このサービスに高負荷をかけないようにしてください。

## 機能

wandbox-vscode はコンパイル、実行、シェアを行う為のいくつかのコマンドをコマンドパレット上で提供します。

> コマンドパレットはキーボードショートカットで表示できます。
>
> Mac: `[F1]` or `[Shift]+[Command]+[P]`
>
> Windows and Linux: `[F1] or [Shift]+[Ctrl]+[P]`

現在 wandbox で利用可能な言語 :
Bash script, C, C#, C++, CoffeeScript, CPP, D, Elixir, Erlang, Groovy, Haskell, Java, JavaScript, Lazy K, Lisp, Lua, Pascal, Perl, PHP, Python, Rill, Ruby, Rust, Scala, SQL, Apple Swift, Vim script


## チュートリアル

### 0. ⬇️ wandbox-vscodeのインストール:
VS Code のクイックオープンを出して(Mac:`[Command]+[P]`, Windows and Linux: `[Ctrl]+[P]`)、 `ext install wandbox-vscode` とタイプし [Enter] キーを押下し、[Install] をクリックします。インストールが終わったら VS Code を再起動してください。

### 1. ✨️ 新規"Hello, World!"を開く:
コマンドパレットを出して(Mac:`[F1]` or `[Shift]+[Command]+[P]`, Windows and Linux: `[F1] or [Shift]+[Ctrl]+[P]`)、 `Wandbox: Hello` コマンドを実行し、適当な "Hello, World!" ファイルを選択します。
> 👉 その他の方法で開いたファイルでも構いません。

### 2. 🚀 wandbox上でのコンパイルと実行:
またコマンドパレットを出して、 `Wandbox: Run` コマンドを実行します。

### 3. 🔗 シェアURLの作成:
さらにまたコマンドパレットを出して、 `Wandbox: Share` コマンドを実行します。


## スクリーンショット

### コマンドリスト
![](https://wraith13.github.io/wandbox-vscode/screenshots/command.list.png)

### 言語
![](https://wraith13.github.io/wandbox-vscode/screenshots/languages.png)
![](https://wraith13.github.io/wandbox-vscode/screenshots/languages2.png)

### コンパイラ
![](https://wraith13.github.io/wandbox-vscode/screenshots/compilers.png)

### オプション
![](https://wraith13.github.io/wandbox-vscode/screenshots/options.png)
![](https://wraith13.github.io/wandbox-vscode/screenshots/options2.png)

## メインコマンド

* `Wandbox: Run` : カレントのドキュメントを wandbox で実行します
* `Wandbox: Share` : シェアURLを作成します

> 自動的にシェアURLを開く挙動は `wandbox.autoOpenShareUrl` の設定で無効化できます。

* `Wandbox: Hello` : 新規 "Hello, World!" を開きます

## 表示コマンド

* `Wandbox: Show Raw JSON` : wandbox の仕様情報を生の JSON で表示します

> 参照： [Wandbox API Reference](https://github.com/melpon/wandbox/blob/master/kennel2/API.rst)

* `Wandbox: Show Web Site` : wandbox web サイトを開きます
* `Wandbox: Show Settings` : wandbox-vscode の全ての設定表示します。
* `Wandbox: Show History` : シェア履歴を表示します。

## 消去コマンド

* `Wandbox: Clear History` : シェア履歴を消去します。

## 設定コマンド

全ての設定コマンドはカレントのドキュメントに対して行われます。
全ての設定コマンドの効果は Visual Studio Code を次回起動した時には消えています。

* `Wandbox: Set Server` : wandboxサーバーURLを設定します。

> [`https://wandbox.fetus.jp/`](https://wandbox.fetus.jp/) を使うこともできます。この Wandbox サーバーには非常に多くの PHP コンパイラがあります。
> Wandbox は [@fetus-hina](https://github.com/fetus-hina) が個人的に無償(自腹)で提供しているサービスです。
> このサービスが提供され続ける為、このサービスに高負荷をかけないようにしてください。

* `Wandbox: Set Compiler` : コンパイラを設定します。
* `Wandbox: Set Options` : コンパイルオプションを設定します。
* `Wandbox: Set Settings JSON` : JSON で一時的な設定をします。
* `Wandbox: Reset Settings` : 全ての一時的な設定をリセットします。


## エクステンションの設定

このエクステンションは次の設定を提供します。

* `wandbox.Servers`: wandboxサーバーURLリスト ( 最初のURLがデフォルト wandboxサーバーURLになります。 )
* `wandbox.simplifyPostData`: postデータを表示の際に簡素化します
* `wandbox.autoOpenShareUrl`: シェアURL作成時に自動的にそのURLを開きます
* `wandbox.outputChannelName`: 出力チャンネル名
* `wandbox.languageMapping`: vscodeでの言語に対しwandboxでの言語を設定します
* `wandbox.languageCompilerMapping`: 言語に対してコンパイラを設定します
* `wandbox.extensionLanguageMapping`: ファイル拡張子に対して言語を設定します
* `wandbox.extensionCompilerMapping`: ファイル拡張子に対してコンパイラを設定します
* `wandbox.options`: コンパイラに対してオプションを設定します
* `wandbox.compilerOptionRaw`: コンパイラに対して生のオプションを設定します
* `wandbox.runtimeOptionRaw`: コンパイラに対して生の実行時オプションを設定します
* `wandbox.helloWolrdFiles`: hello world ファイルを設定
* `wandbox.maxHistorySize`: 最大履歴サイズを設定
* `wandbox.emoji`: 絵文字を設定

> あなたの環境のフォントが貧相な場合は次のような設定にしてください。
>```json
>    "wandbox.emoji": {
>        "stamp": null,
>        "error": null,
>        "warning": null,
>        "hint": null,
>        "signal": null,
>        "link": null,
>        "lap": null,
>        "new": null,
>        "checkedBox": "[o]",
>        "uncheckedBox": "[_]",
>        "checkedRadio": "(o)",
>        "uncheckedRadio": "(_)",
>        "edit": null,
>        "menuSeparator": "---------------------------------------------"
>    }
>```
>
> Mac での `wandbox.emoji` 設定のスクリーンショット ( 参考用 )
>
> ![](https://wraith13.github.io/wandbox-vscode/screenshots/emoji.png?!)

## リリースノート

[marketplace](https://marketplace.visualstudio.com/items/wraith13.wandbox-vscode/changelog) あるいは [github](https://github.com/wraith13/wandbox-vscode/blob/master/CHANGELOG.md) の ChangLog を参照してください。


## "Wandbox に俺の好きなコンパイラがないぞ！"

問題ありません！　あなたは [wandbox](https://github.com/melpon/wandbox/) にプルリクエストを投げることができます！

## サポート

[GitHub Issues](https://github.com/wraith13/wandbox-vscode/issues)

## ライセンス

[Boost Software License](https://github.com/wraith13/wandbox-vscode/blob/master/LICENSE_1_0.txt)

## 謝辞

Thanks [@melpon](https://github.com/melpon)( 🐕 犬) and [@kikairoya](https://github.com/kikairoya)( 🐂 牛) for awesome compilation service!

Thanks [@fetus-hina](https://github.com/fetus-hina)( 👶 baby) for a PHP specialized wandbox service!

Thanks [@rhysd](https://github.com/rhysd)( 🐕 犬) for your support in TypeScript!

Thanks [@chomado](https://github.com/chomado)( 👧 girl) for a great extension icon!