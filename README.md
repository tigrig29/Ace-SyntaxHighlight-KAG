# Ace-SyntaxHighlight-KAG
Ace.jsで利用できるmodeファイル（SyntaxHighlighter）の『KAG』バージョンです。

* [Ace.js](https://ace.c9.io/)

# 概要
ノベルゲーム制作エンジン『吉里吉里』のスクリプトである『KAG』のシンタックスハイライトを行います。  
吉里吉里に限らず、『吉里吉里Z』や『ティラノスクリプト』など、KAG形式のスクリプトであればハイライト可能です。

* [吉里吉里](http://kikyou.info/tvp/)
* [吉里吉里Z](https://krkrz.github.io/)
* [KAGタグリファレンス](http://devdoc.kikyou.info/tvp/docs/kag3doc/contents/)
* [ティラノスクリプト](http://tyrano.jp/)

# 導入方法
## Ace.jsの導入
1. https://github.com/ajaxorg/ace-builds/ からダウンロード
2. src-min-noconflict/ace.js を プロジェクトフォルダに追加
3. HTMLのscriptタグなどでace.jsを読み込む

## SyntaxHighlighterの導入
1. 当リポジトリから、Ace-SyntaxHighlight-KAGをダウンロード
2. srcの中身を全て、**ace.jsと同じ階層に**追加
3. HTMLのscriptタグで mode-javascript.js と mode-kag.js を読み込む

## 実行サンプルコード
```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>Ace Editor sample</title>
</head>
<body>
  <div id="editor" style="height: 600px"></div>
  <script src="./libs/ace.js"></script>
  <script src="./libs/mode-javascript.js"></script>
  <script src="./libs/mode-kag.js"></script>
  <script>
    // エディタ作成
    ace.edit("editor");
    // syntax highlight
    const KAGMode = ace.require("ace/mode/kag").Mode;
    Editor.getSession().setMode(new KAGMode());
    Editor.setTheme("ace/theme/kag-dark");
    // or
    // Editor.setTheme("ace/theme/kag-simple");
  </script>
</body>
</html>
```

# 製作者へのコンタクト
疑問や修正要望、バグ報告などございましたら、Gmail【tigrig.crex】かTwitter【[@Tig_nico](https://twitter.com/Tig_nico)】までご連絡下さい。

AceSyntaxHighlighterの自作方法を知りたいなどの要件でも構いません。お気軽にどうぞ。