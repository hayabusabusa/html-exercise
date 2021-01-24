# 2-1. メディアクエリによる表示の切り替え

レスポンシブデザインを実装するうえで重要な**メディアクエリ**について。

## メディアクエリとは

**メディアクエリ**はCSSの記述に条件を加える記法のこと。  

CSS2ではメディアタイプというものがあり、メディアごとにCSSの適用範囲を変えることができた。  
しかし、スマホやタブレットの普及によりWebサイトで多様なデバイスに対応する需要が高まりCSS3で登場したのがメディアクエリ。

JS を使ってレスポンシブ対応させることはできるが、メディアクエリの方がシンプルで分かりやすい。

## Viewportの指定

メディアクエリを正しく動作させるには **Viewport** の指定が必要。  
**Viewport** で画面のサイズを限定しないと意図しない表示になる場合があるので必ず設定する。

```html
<meta name="viewport" content="width=device-width">
```

## インライン記述方法

メディアクエリで**ブラウザサイズを指定**して**その {} 内にCSSを書く**ことで特定のブラウザサイズでのみ動作するCSSを書くことができる。

以下の CSS の記述は

- ブラウザサイズが `1280px` 以下の時
- `h1 { color: #f00; }` を適用する

```css
@media (max-width: 1280px) {
  h1 {
    color: #f00;
  }
}
```

また、以下の CSS では

- ブラウザサイズが `768px` 以上かつ `1080px` 以下の時
- `.text { color: #0f0; }` を適用する

```css
@media (min-width: 768px) and (max-width: 1080px) {
  .text {
    color: #0f0;
  }
}
```

## アウトライン記述方法

`media` 属性にサイズ等を指定して、CSS を読み込む時にファイルごと条件を指定することもできる。

以下の記述では

- ブラウザサイズが `767px` 以下の時
- `mobile.css` を適用する

```css
<link href="css/mobile.css" rel="stylesheet" type="text/css" media="max-width: 767px" >
```

## ブラウザサイズの指定方法

`max-width` と `min-width` でブラウザサイズを指定できる。

### max-width

`max-width` はビューエリアの最大幅を指定できる。  
`max-width` で指定した幅より小さい場合にスタイルが適用される。  

### min-width

`min-width` はビューエリアの最小幅を指定できる。  
`min-width` で指定した幅より大きい場合にスタイルが適用される。  

## よく使うメディアクエリ

### スマホのみ CSS を適用する

iPad の 768px を基準にして、767px 以下の場合 CSS を適用する。

```css
@media all and (max-width: 767px) {

}
```

### PCのみ CSS を適用する

ホバーのアニメーションをつける時などに使うらしい。

```css
@media all and (min-width: 980px) {

}
```

## メディアタイプについて

メディアクエリと似たような記述でメディアタイプというものがある。
以下の CSS の `all` の部分が該当する。

```css
@media all and (min-width: 768px) {
  h1 {
    color: #f00;
  }
}
```