# 2-5. グリッドレイアウトの実装

グリッドレイアウトの実装について。

## grid の親要素について

横方向の要素のレイアウトは `grid-template-columns` に指定して、縦方向の要素のレイアウトは `grid-template-rows` に指定する。  

以下の CSS では

- 横方向に 3 つの要素があり、1 と 2 番目の要素は `200px` 固定で、残りは `1fr` で可変の幅
- 縦方向に 2 つの要素があり、1 と 2 番目の要素どちらも `200px` で固定

のレイアウトを指定している。

```css
display: grid;
grid-template-columns: 200px 200px 1fr;
grid-template-rows: 200px 200px;
```

## grid の子要素について

子要素は親要素で作成したレイアウトに対して横方向は `grid-column` と、縦方向は `grid-row` に対してどこに配置させるのかを指定する。

```css
grid-column: 2; /* 横位置を② */
grid-row: 1; /* 縦位置を① */

grid-column: 3; /* 横位置を③ */
grid-row: 1 / 3; /* 縦位置を① ~ ③ */
```

| 子要素の指定 PC | 子要素の指定 SP |
| :-: | :-: |
| ![grid_layout](https://user-images.githubusercontent.com/31949692/105812646-dfb6fa80-5ff1-11eb-861b-484b38b9ecae.png) | <img width="432" alt="Frame 5" src="https://user-images.githubusercontent.com/31949692/105816337-84880680-5ff7-11eb-8bc2-3531878b58f0.png"> |

## overflow について

`overflow` は**要素のボックスからはみ出た部分**をどう扱うかを指定する。

- `visible` はみ出た部分が、はみ出たままの状態で表示される場合あり( デフォルト )
- `hidden` はみ出た部分が隠れる
- `scroll` はみ出た部分が隠れてスクロールできる状態に
- `auto` ブラウザにより表示が変わる（基本的にはスクロールできる状態に）

- [【CSS】overflowの使い方：hiddenやscrollの違いは？ - サルワカ](https://saruwakakun.com/html-css/basic/overflow)