# 2-4. フレックスボックスの実装

`display: flex` を使ったレイアウトの実装について。

## 完成形

| PC | SP |
| :-: | :-: |
| <img width="1440" alt="スクリーンショット 2021-01-26 14 34 17" src="https://user-images.githubusercontent.com/31949692/105804760-f2c2ce00-5fe3-11eb-820a-c14518c8829d.png"> | ![responsive-web-design-coding_2-4_index html(iPhone X)](https://user-images.githubusercontent.com/31949692/105804697-cc9d2e00-5fe3-11eb-93fd-cb57aa2ae666.png) |

## flex について

`display: flex` は複数の CSS プロパティと組み合わせることで様々なレイアウトを表現できる。

### flex-wrap

子要素を**１行に配置するか複数行に配置できるようにするか**指定する。

- `nowrap` 折り返しさせず１行に配置( デフォルト )
- `wrap` 複数行で上から下に配置
- `wrap-reverse` 複数行で下から上に配置

### flex-direction

子要素の表示方向を指定する。

- `row` 左から右に配置( デフォルト )
- `row-reverse` 右から左に配置
- `column` 上から下に配置
- `column-reverse` 下から上に配置

### justify-content

水平方向の配置位置を指定する。

- `flex-start` 左揃え( デフォルト )
- `flex-end` 右揃え
- `center` 中央揃え
- `space-between` 均等割り付け
- `space-around` 両端に子要素の半分の間隔をあけて均等割り付け

### align-items

垂直方向の配置位置を指定する。

- `stretch` 親要素の高さ、またはコンテンツの一番多い子要素の高さに合わせて広げて配置( デフォルト )
- `flex-start` 上揃え
- `flex-end` 下揃え
- `center` 中央揃え
- `baseline` ベースラインに揃える

### flexbox のチートシート

- [チートシート](https://www.webcreatorbox.com/tech/css-flexbox-cheat-sheet)

## 実装

### flex 関連

親要素である `box` には `flex` を指定する。  
その上で `flex-wrap: wrap` を指定して、要素を複数行で並ぶようにする。  
さらに `justify-content: center` で真ん中に並ぶように指定する。

## テキストを任意の行数だけ表示する

Swift の `UILabel` の行数指定みたいに、任意の行数だけ `p` タグに表示したい。  
CSS で `line-height` と `height` と `overflow` で制御できる。

```css
overflow: hidden;
height: 3.6em; /* 2em（行）x line-heightの1.8 */
font-size: 16px;
line-height: 1.8;
```

### 参考

- [CSSだけで希望の行数だけ表示して、それを越える文字は非表示にする - Qiita](https://qiita.com/b95oss/items/ab6a1dddd61831cdb97f)