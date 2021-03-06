台本を字幕に起こすスクリプト
====

After Effectsに、事前に作成された台本から、字幕を作成します。

概要
----

After Effectsに、台本ファイルから字幕を作成します。
台本ファイルは、指定の文法のテキストファイル、Excel ワークブック、 Google スプレッドシートが利用できます。


使い方
----

1. After Effects の編集、環境設定、一般設定から、スクリプトによるファイルへの書き込みとネットワークへのアクセスを許可にチェックを入れます。
2. ファイル、スクリプトから、スクリプトファイルの実行を選択し、"ScenarioAnalyser.jsx" を選択します。
3. 台本を選択します。
  * 台本ファイルの場合、そのファイルのプロジェクトフォルダを選択します。
  * Excel の場合はファイルを選択します。
  * Google スプレッドシートの場合は、実行時に解析を開始します。
4. Excel、Googleスプレッドシートの場合、Wavファイルを格納しているフォルダを選択します。
5. 「台本解析器を選択」を選択し、"sa4ae.exe" を選択します。
6. 各パラメタを設定します。
7. 台本解析開始を実行します。

ファイル、フォルダ構成
----

* bin ... バイナリが格納されています。
* doc ... 文書が格納されています。
  * README.html ... README.md.txt のHTML版です。
  * Update.html ... 更新情報です。
  * LICENSE.txt ... このツールのライセンスです。
  * Dependencies.txt ... このツールが利用しているライブラリの表示とライセンス表示です。
  * Template.xltx ... 台本のExcelテンプレートです。
  * 強制停止(Force Stop).bat ... プログラムが暴走した時に強制的に止めるバッチファイルです。暴走したらごめんなさい。
* ScenarioAnalyser.jsx ... After Effects に読み込ませるスクリプトです。
* TypewriteredText.jsxinc ... ScenarioAnalyser.jsx から呼び出される、字幕を作成するスクリプトです。
* sa4ae.exe ... ScenarioAnalyser.jsx の実行時に指定する台本解析機です。


### 台本ファイル

台本スクリプトの文法等は、以下のサイトをご確認ください。

* [台本を字幕に起こすスクリプト](https://midolin.info/app/sa4ae)

#### スプレッドシート

また、Google スプレッドシート、もしくはExcel ワークブックからも字幕が作成できるようになりました。
関連ツール ([Scenario Scripter](https://midolin.info/app/scsc)) と同一モジュールを使用しているため、
台本ファイルのフォーマットは、以下のものである必要があります(後々改善します)。

* 「台本」と「音声」という名前の2つのワークシート
* 「台本」シートのヘッダー(1行目)は、「名前」「セリフ」「注釈」「音量」「話速」「高さ」「抑揚」
* 「音声」シートのヘッダーは、「名前」「キャラ」「音量」「話速」「高さ」「抑揚」
* 「台本」シートの2行目の、「名前」と「セリフ」は、埋められている必要がある
* 「音声」シートの2行目は、各列は埋められている必要がある

スプレッドシートの途中に空行があると、その分を指定されたMarginだけ空けて、次の行を読み取ります。

作者
----

limemidolin <lime@midolin.info> (twitter: @limemidolin)


利用条件
----

MIT.


依存ライブラリのライセンスおよび表示
----

このソフトウェアが成立するためには以下のライブラリが欠かせませんでした。
ここに謝辞として感謝申し上げます。

ライブラリ一覧は、`doc/Dependencies.txt` をご参照ください。

