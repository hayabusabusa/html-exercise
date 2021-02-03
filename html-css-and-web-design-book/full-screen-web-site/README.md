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

## ファビコンについて

今回は Web ブラウザ用のファビコンのみ設定したが、他の端末にも対応させたい場合はもう少し処理を記述する必要がある。  

楽をしたい場合は以下のサービスを利用する。

- [RealFaviconGenerator](https://realfavicongenerator.net/)