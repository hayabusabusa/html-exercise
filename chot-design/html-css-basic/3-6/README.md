# 3-6. 背景色と背景画像を設定する

背景の色を変えたり、画像を設定する方法について。

## 背景の色を設定する

背景色を指定するCSSプロパティは `background-color`。  
値には `color` と同様にキーワード・カラーコード・RGB・RGBAが指定できる。

```css
 background-color: #ff0000;
```

## 背景に画像を設定する

背景に画像を設定する場合は `background-image` に画像のパスを設定する。  

```css
background-image: url(ファイル名.拡張子);
```

### 背景画像のサイズを指定する

`background-size` で背景画像のサイズを指定することができる。  
以下の値を指定できる。

- `auto` (デフォルト)
- `cover`
- `contain`
- `px`
- `%`

`px` と `%` は横幅と高さをスペースで区切って指定する。

```css
 background-size: 200px 100px;
```

- **cover**

縦横比は保持したまま、背景領域を完全に覆う最小サイズになるように拡大縮小される。

- **contain**

縦横比を保持したまま、背景領域に収まる最大サイズになるように拡大縮小される。

| cover | contain |
| :-: | :-: |
| ![cover](https://user-images.githubusercontent.com/31949692/105620643-62995300-5e42-11eb-836d-bc56ead83478.png) | ![contain](https://user-images.githubusercontent.com/31949692/105620646-6d53e800-5e42-11eb-809e-9ef46c1dfb51.png) |

## 背景画像の繰り返しと表示位置を制御する

表示領域より背景画像が小さいと、背景は自動的に繰り返し表示になる。 
繰り返しは `background-repeat` というプロパティで制御することができる。
以下の値を指定できる。

- `repeat` (デフォルト)
- `repeat-x`
- `repeat-y`
- `no-repeat`

横並びだけリピートさせる `repeat-x`、縦並びだけリピートさせる `repeat-y`、繰り返しをなくして1個だけ表示するのを `no-repeat` で設定する。

```css
background-repeat: repeat-y;
```

| repeat | repeat-y | no-repeat |
| :-: | :-: | :-: |
| ![repeat](https://user-images.githubusercontent.com/31949692/105620691-e2bfb880-5e42-11eb-869e-af01ad4fc63d.png) | ![repeat_y](https://user-images.githubusercontent.com/31949692/105620690-e05d5e80-5e42-11eb-859b-876771783e93.png) | ![no_repeat](https://user-images.githubusercontent.com/31949692/105620688-ddfb0480-5e42-11eb-8d7d-113db085c5fe.png) |

## 背景画像の表示位置を制御する

背景画像は要素の一番左上から詰めて並べられる。  
`background-position` で位置を制御することができる。  
以下の値を指定できる。

- キーワード( `top`・`right`・`bottom`・`left` )
- `%`
- `px`

`%` と `px` で指定した場合、左上から X% もしくは Xpx 移動して表示される。

```css
background-position: center center;
```

## ショートハンドを使う

背景色や背景画像、表示位置などは `background-` というプレフィックスがついているが、これらのプロパティは1つのプロパティでまとめて記述することができる。  
複数のプロパティを1つにまとめられる機能のことを**ショートハンド**という。

```css
background: skyblue URL no-repeat  center center / 200px 100px;
```