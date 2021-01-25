# 2-3. カラムの配置が変わるレイアウトの実装

PCでは画像とテキストが横並びになっていて、スマホでは縦並びになるレイアウトの実装。

## 完成形

| PC | SP |
| :-: | :-: |
| ![responsive-web-design-coding_2-3_index html](https://user-images.githubusercontent.com/31949692/105690370-3f080280-5f3f-11eb-89b7-940fd622a186.png) | ![responsive-web-design-coding_2-3_index html](https://user-images.githubusercontent.com/31949692/105690449-5c3cd100-5f3f-11eb-94ff-30e6c553e173.png) |

## 実装

### 画像とテキストの領域

画像要素 `.column-img` とテキスト要素 `.column-texts` の `width` を `%` 指定にすることでブラウザサイズに合わせた比率でエリアが確保されるようになる。  

```css
.column-image {
    width: 40%;
}

.column-texts {
    width: 60%;
}
```

### column-reverse

画像とテキストの位置が2つとも逆なので、SP 表示の場合は片方に `column-reverse` を指定してから縦表示になるように幅の比率を調節する。

```css
@media screen and (max-width: 767px) {
    .column {
        flex-direction: column;
    }

    .column--reverse {
        flex-direction: column-reverse;
    }
}
```