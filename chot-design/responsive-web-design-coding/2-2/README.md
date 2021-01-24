# 2-2. 要素の位置や大きさを変えるレイアウトの実装

要素の位置や大きさを変えるレイアウトの実装について。

## 完成形

| PC | SP |
| :-: | :-: |
| <img width="1440" alt="スクリーンショット 2021-01-25 0 45 58" src="https://user-images.githubusercontent.com/31949692/105635564-dff6af00-5ea6-11eb-9375-24142e1663f9.png"> | <img width="629" alt="スクリーンショット 2021-01-25 0 46 12" src="https://user-images.githubusercontent.com/31949692/105635581-f3097f00-5ea6-11eb-920e-f3552441ce3b.png"> |

## 実装

基本的には PC から実装した方が良さげ。  
`@media` 内でスマホ用のレイアウトの CSS を実装する。

```css
@media all and (max-width: 767px) {
    ...
}
```

# 実装時のハマり

## height: 100% が効かない

画像を全画面表示にしたいので、以下のような CSS にしたが、高さ 100% にならなかった。

```css
.kv {
  height: 100%;
}
```

親要素になる `html` と `body` に対して `height: 100%` を指定するといける。

```css
html {
  height: 100%;
}

body {
  height: 100%;
  margin: 0;
}

.kv {
  height: 100%;
}
```

### 原因

ある要素の `height` に相対値（%）が指定された場合、その高さは包含ブロックの高さに対して計算される。  
その要素が通常フローで配置されており、かつ包含ブロックの高さが明示されていない場合、要素の高さは `auto` として計算されるため。  

- ["height: 100%" の要素が画面の高さ100%にならない場合の対応方法 - Qiita](https://qiita.com/shouchida/items/205fed63b886681661bd)

## 画像にオーバーレイを被せたい

画像の上に白でテキスト載せて、かつオーバーレイで半透明の黒いやつを被せたい。  
`div` でオーバーレイを表現しようとしたけど簡単にできなかった。

### 対策

`<header>` と `<img>` タグを使って作る。  
ヘッダーっぽい部分の場合 SEO 的にも、アクセシビリティ的にも `<header>` タグを使用した方がいい。  

```html
<header>
    <img src="..." alt="...">
</header>
```

```css
header {
    height: 600px;
    width: 100vw;
    background: black;
    overflow: hidden;
}

img {
    height: 600px;
    object-fit: cover;
    opacity: 0.4;
}
```

- [Two ways to create an image with a colour overlay in CSS - dev.to](https://dev.to/ellen_dev/two-ways-to-achieve-an-image-colour-overlay-with-css-eio)