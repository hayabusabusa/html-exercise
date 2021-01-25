# 3-15. 疑似要素の使い方

HTML 上には存在しない要素をCSSだけで擬似的に追加できる疑似要素について。

## 疑似要素を使って文字や記号を追加する

疑似要素 `before` と `after` は、疑似要素を設置したい**セレクタ**に対して付け加える。

```css
.box:after{
  color:red;
  content: "after"
}
```

疑似要素を作成され、その中に `content` というプロパティで `after` という文字列が指定されているので、後ろに `after` の文字列が付け加えられる。  
`before` は該当要素の前、`after` は該当要素の後に擬似要素を作成する。

## 疑似要素を使ってふきだしのデザインを再現する

疑似要素を使ったサンプルとして吹き出しを作ってみる。

```css
.box{
  background: #ffdd3f;
  text-align: center;
  padding: 10px;
  position: relative;
}

.box:after{
  content: '';
  position: absolute;
  border-top: 16px solid #ffdd3f;
  border-right: 12px solid transparent;
  border-left: 12px solid transparent;
  bottom: -16px;
  left: 50%;
  margin-left: -6px;
}
```

## 疑似要素を使ってfloatを解除する

`float` を使った要素の親要素に対して `after` 疑似要素で `clear` すると、`float` 解除ができる。

```css
.box:after{
  content: "";
  display: block;
  clear: both;
}
```

## 擬似要素は何がいいのか

### 細かい装飾が可能

例えば先頭1文字だけ色を変えたい場合など、本来は一旦 `span` 等で一文字だけ装飾する必要があるが、擬似要素を使えば不要なタグを使う必要がなくなる。

```html
<h1><span>見</span>出し</h1>
```

```css
span {
    color: red;
}

/* 擬似要素ならこれだけでいい */
h1::first-letter {
    color: red;
}
```

`position: relative` で親要素を相対配置にしておいて、擬似要素で `position: absolute` にして細かい装飾をするのが結構便利。  



### SEO に気にせず装飾ができる

検索エンジンは CSS である疑似要素をコンテンツの中身として見ていないため、SEO を気にせずにユーザーのための自由な表現ができる。

## 参考

- [CSSの疑似要素とは？beforeとafterの使い方まとめ - サルワカ](https://saruwakakun.com/html-css/basic/before-after)