# 3-13. コーナーに角丸を指定する

四角い要素のコーナーの角を丸くする方法について。

## コーナーを角丸にする

`border-radius` を指定することで、要素のコーナーを角丸にすることができる。  
値は `px` か `%` で指定する。

```css
border-radius: 20px;
```

## 角丸のサイズをバラバラに指定する

角丸のサイズは1箇所ずつ指定することもできる。

- `border-top-left-radius`
- `border-top-right-radius`
- `border-bottom-right-radius`
- `order-bottom-left-radius`

まとめて指定するショートハンドもある。左上・右上・右下・左下の順番で指定する。

```css
border-radius: 10px 20px 30px 40px;
```

## CSSだけでボタンを作る

`border-radius` を使ってCSSだけでボタンを作る。

```css
.button{
  background: #53caff;
  color: #fff;
  text-decoration: none;
  padding: 10px;
  border-radius: 8px;
}
```

## 参考

- [CSSで作る！押したくなるボタンデザイン100（Web用）- サルワカ](https://saruwakakun.com/html-css/reference/buttons)