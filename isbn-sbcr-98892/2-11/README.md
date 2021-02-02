# 2-11 フォームを作る

お問い合わせや検索ボックスなどのフォームを作ってみる。

## form タグ

`<form>` タグはフォームを作るためのタグで、フォームで使用する全てのパーツを `<form>` で囲う。

```html
<form action="example.php" method="post" name="contact-form">
    <!-- フォームの部品 -->
</form>
```

> `<form>` タグ内で使う部品は PHP 等と連携して動かすらしい。

## フォームで使うパーツ

フォーム内で使う各パーツを設置するタグについて。

### input タグ

`<input>` タグで**1行のテキスト**を入力するエリアを設置できる。  
`type="url"` などで属性値を指定することで、入力された値が正しい書式になっているかをチェックしてくれる。

```html
名前: <input type="text" placeholder="名字 名前">
```

### ラジオボタン

複数ある選択肢のうち、1つのみを選択して欲しい場合には**ラジオボタン**を使用する。  
複数の選択肢があるラジオボタンでは、それぞれに同じ `name` 属性の値をつけることで1つのグループとしてまとめることができて、ユーザーはグループから1つだけ選択できるようになる。

```html
<input type="radio" name="gender" value="男性">男性
<input type="radio" name="gender" value="女性" checked>女性
<input type="radio" name="gender" value="その他">その他
```

### チェックボックス

複数ある選択肢のうち、複数の項目を選択して欲しい場合には**チェックボックス**を使用する。  
ラジオボタンと同じく、それぞれに同じ `name` 属性の値をつけることで1つのグループとしてまとめることができる。  

```html
<input type="checkbox" name="color" value="赤">赤
<input type="checkbox" name="color" value="青" checked>青
<input type="checkbox" name="color" value="黄">黄
<input type="checkbox" name="color" value="緑">緑
```

### 送信ボタン

フォームに入力した内容を送信するためのボタンは `<input>` タグの `type="submit"` を指定する。
デフォルトだと結構小さくなるので CSS 等で調節した方が良さげ。

```html
<input type="submit" value="送信する">
```

### セレクトボックス

多くの選択肢から1つ選択して欲しい場合は `<select>` と `<option>` でセレクトボックスを作る。

```html
<select name="bloodtype">
    <option value="A">A</option>
    <option value="B">B</option>
    <option value="O">O</option>
    <option value="AB">AB</option>
    <option value="その他" selected>その他</option>
</select>
```

### テキストエリア

複数行のテキストを入力したい場合は `<textarea>` を使用する。  

```html
<textarea name="message" placeholder="メッセージを入力"></textarea>
```