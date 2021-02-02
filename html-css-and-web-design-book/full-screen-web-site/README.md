# 4. フルスクリーンのWebサイトを作る

## CSS のグローバルな設定

`font-size: 100%` で指定することで、ユーザーの設定した文字サイズが正しく適応されるようにする。

```css
html {
    font-size: 100%;
}
```

`<a>` タグに `text-decoration: none` で指定することで、リンクの下線を消している。

```css
a {
   text-decoration: none;
}
```

`<img>` タグに最大幅を `100%` で設定することで、親要素より大きくなるのを防いでいる。

```css
img {
   max-width: 100%;
}
```