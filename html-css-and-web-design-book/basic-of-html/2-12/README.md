# 2-12. より使いやすいフォームを作る

フォームにラベルを設置して、より使いやすいフォームを作る。

## label タグ

フォームにラベルを付けるには `<label>` タグを使用する。  
`<label>` タグを使うことでフォームのパーツとラベルが関連付けられ、そのテキストを含んだ選択項目全体がクリックできるようになる。

小さなラジオボタンやチェックボックスは操作が難しい場合があるので、ラベルをつけてあげた方がいい。

`<label>` タグの `for` 属性と、フォームの `id` 属性を対応させる。

```html
<input type="checkbox" name="travel" value="日本国内" id="japan">
<label for="japan">日本国内</label>

<input type="checkbox" name="travel" id="europe" value="ヨーロッパ">
<label for="europe">ヨーロッパ</label>
```