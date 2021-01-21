# 3-3. テキストの装飾

文字を太くしたり、斜めにしたり、下線を引く方法について。

## 文字を太くする

文字の太さを調節するCSSプロパティは `font-weight`。
`font-weight` には以下の値が入れられる。

- `normal`
- `bold`
- `bolder`
- `lighter`
- `100` 〜 `900`

どれぐらいまで太くなるかは用意されているフォントによって違う。

```css
.bold {
  font-weight: bold;
}
```

## 文字を斜めにする

文字を斜めにするCSSプロパティは `font-style`。  
`font-style` には以下の値が入れられる。

- `normal`
- `italic`
- `oblique`

`italic` と `oblique` の2つがあるが両方とも斜めになる。  
フォントが `italic` を持っていない場合に `italic` を指定すると `oblique` が適用され、その逆の場合も同様の動作となる。

```css
.italic {
  font-style: italic;
}
```

## 文字に下線を引く

文字に下線を引くCSSプロパティは `text-decoration`。
`text-decoration` には以下の値が入れられる。

- `none`
- `underline`
- `overline`
- `line-through`

下線だけでなく、上に線を引いたり、真ん中に線を引くことができる。

```css
.underline {
  text-decoration : underline;
}
```