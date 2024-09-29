# DOM(Document Object Model)とは

HTMLやXML文書の構造を表現するためのAPI(Application Programming Interface)
要素の取得、追加、削除、属性の取得、設定などが可能

木構造の例
'''
<!DOCTYPE html>
<html>
  <head>
    <title>サンプルページ</title>
  </head>
  <body>
    <h1>これは見出しです</h1>
    <p>これは段落です</p>
  </body>
</html>

↓↓↓

- Document (全体)
  - html
    - head
      - title
    - body
      - h1
      - p



'''

# DOMとJavaScriptの関係
JavaScriptを使ってウェブページの構造や内容、見た目を動的に操作できる

DOMメソッドの例
document.getElementById(id)：指定されたIDを持つ要素を取得
document.querySelector(selector)：CSSセレクタを使って要素を取得
element.textContent：要素内のテキストを取得・設定
element.innerHTML：要素内のHTML内容を取得・設定
element.style：要素のスタイルを操作（色や大きさの変更など）

DOMの利用例
フォームの入力内容の検証：送信ボタンが押されたときに、入力が正しいかチェック
動的なリストの作成：ユーザーのアクションに応じて、新しいアイテムをリストに追加
リアルタイムのデータ表示：SNSで新しいメッセージを自動表示


# 01_HTMLファイルを動かしDOMをみてみる

VScodeで開くなら拡張機能「Live Server」がおすすめ
右クリック→「Open with Live Server」を選択

sample01.htmlについて
'''
- Document (ルートノード)
  - html
    - head
      - meta (charset="UTF-8")
      - meta (name="viewport" content="width=device-width, initial-scale=1.0")
      - title ("DOM Study")
    - body
      - h1 (id="title", text="Hello World")
      - button (id="changeText", text="change text")
      - script
        - テキストノード (JavaScriptコード)
      - script (Live Serverが注入したコード)
'''
[変更後](images\01_after.png)はボタンが押されることによりh1要素のテキストが変更される
