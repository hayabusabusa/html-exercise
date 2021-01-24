# 3-9. 要素に余白を空ける

要素の周りや内側に対して余白をつくる方法。

## margin と padding の違い

余白を設定するプロパティは `margin` と `padding` の2種類があり、それぞれ**外側の余白**と**内側の余白**を指定する。

| margin と padding |
| :-: |
| ![diffarence_margin_and_padding](https://user-images.githubusercontent.com/31949692/105623805-047b6880-5e60-11eb-8711-1a30a3beb2f1.png) |

## margin auto

要素自体を中央に寄せたい場合には `margin` に `auto` を指定する。

```css
margin: auto;
```

## 上下左右それぞれに余白を設定する

`margin` と `padding` は上下左右それぞれに余白を設定することができる。
それぞれ `x-top`、`x-right`、`x-bottom`、`x-left` で指定する。

```css
margin-top: 16px;
```

また、省略して記述することもできる。  

### 上下と左右

以下の場合**上下に 30px で左右に 60px の余白**を設定することができる。

```css
margin: 30px 60px;
```

### 上と左右と下

以下の場合は**上に 10px、左右に 30px、下に 40px の余白**を指定することができる。

```css
margin: 10px 30px 40px;
```

### それぞれ

以下の場合は**上に 10px、右に 20px、下に 30px、左に 40pxの余白**を指定することができる。

```css
margin: 10px 20px 30px 40px;
```
