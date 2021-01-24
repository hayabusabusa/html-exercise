# 3-10. 要素に枠線をつける

要素に枠線をつける方法について。

## 要素に枠線を付ける

HTML要素には枠線の装飾をつけることができる。  
枠線はスタイル・太さ・色の３種類を指定することができる。

- `border-style`
- `border-width`
- `border-color`

これらは `border` で1つにまとめることができる。

```css
border: スタイル 太さ 色;
```

## 枠線のスタイルについて

`border` は1本線以外にもいくつかスタイルがある。

- `solid` ( 1本線 )
- `double` ( 2本線 )
- `dashed` ( 破線 )
- `dotted` ( 点線 )

```css
border: dotted 2px red;
```

## 上下左右を分けて指定する

一部分だけ枠線を指定したい場合は以下のプロパティを指定する。

- `border-top`
- `border-right`
- `border-bottom`
- `border-left`

```css
border-bottom : solid 1px red;
```