opCsvExportPlugin
=================

SNS 内メンバのデータを csv 形式で出力する OpenPNE のプラグイン

# How to Use (Web)

sns.example.com というドメインで SNS を動かしているとき，下記のようなURLにアクセスしてください．

    http://sns.exmaple.com/pc_backend.php/csvExport/download

フォームに必要な情報を記入して「ダウンロード」ボタンをクリックします．

<table>
<tr>
<th>フォーム名</th><th>詳細</th>
</tr>
<tr>
<td>from</td><td>メンバID 開始位置 整数値 (inclusive)</td>
</tr>
<tr>
<td>to</td><td>メンバID 終了位置 整数値 (exclusive)</td>
</tr>
</table>


## Useful way to make easy to access

管理画面「メンバ管理」でメニューを表示させたい場合は下記コマンドでパッチを適用してください．

    $ patch -p1 < plugins/opCsvExportPlugin/data/patches/op36.patch

# How to Use (Task)

    $ ./symfony opCsvExport:export

## Options

<table>
<tr>
<th>オプション名</th><th>詳細</th><th>デフォルト値</th>
</tr>
<tr>
<td>from</td><td>メンバID 開始位置 整数値 (inclusive)</td><td>1</td>
</tr>
<tr>
<td>to</td><td>メンバID 終了位置 整数値 (exclusive)</td><td>なし（最後まで）</td>
</tr>
<tr>
<td>header</td><td>各データ名を csv の最初に付与するか true/false </td><td>true</td>
</tr>
</table>
