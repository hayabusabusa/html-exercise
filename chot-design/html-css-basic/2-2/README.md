# 文書のメタデータのタグ

`<head>` タグ内に記述するタグとヘッダ情報について。

## title タグ

`<title>` はページのタイトル名を入れるタグ。  
ここに入ったタイトルは、ブラウザのタイトルバーやタブバーに表示される。

また、検索エンジンで検索した時の検索結果の表示にも使われる。

| ブラウザ | 検索エンジン |
| :-: | :-: |
| <img width="675" alt="スクリーンショット 2021-01-20 13 19 58" src="https://user-images.githubusercontent.com/31949692/105126628-86972480-5b22-11eb-95bf-51eaa5b2513e.png"> | <img width="495" alt="スクリーンショット 2021-01-20 13 20 10" src="https://user-images.githubusercontent.com/31949692/105126661-96166d80-5b22-11eb-8cce-41d096b822f6.png"> |


```html
<head>
  <title>chot.design - 毎日ちょっとずつデザインを学ぼう</title>
</head>
```

## meta タグ

`<meta>` タグはブラウザに表示されないそのページの付加情報を定義するタグ。

### charaset

`charaset` にはページの文字コードを指定する。

```html
<meta charset="utf-8">
```

### description

`description` にはページの説明文をいれる。  
説明文は検索エンジンの検索結果に使われる。

| 検索エンジン |
| :-: |
| <img width="314" alt="スクリーンショット 2021-01-20 13 28 20" src="https://user-images.githubusercontent.com/31949692/105127067-64ea6d00-5b23-11eb-8360-f8fe7c81da7f.png"> |

```html
<meta name="description" content="chot.designはWebデザインやUI/UXデザイン、その他デザイン制作について学べるサイトです。">
```

### keyword

`keyword` はページのキーワードをいれるのに使う。  
以前は Google や Yahoo 等の検索エンジンで利用されていたが、今は利用されていないため記述しなくてもいいらしい。

```html
<meta name="keywords" content="chot, design">
```

## link タグ

`<link>` は現在の文書と関連する別の文書を指定するときに使う。  
スタイルシートやファビコンの指定、アプリのアイコンの指定などに使用する。

### rel 属性

`<link>` で指定した文書との関係性を表す。
よく使われるのは `stylesheet` や `icon` など。

### media 属性

`<link>` で指定した文書がどのようなメディアに適用するのかを指定する。  
ブラウザで見ているとき、指定されてるメディアの場合に `<link>` 内の文書が適用される。  

ウェブサイトを作成するとき、一般的には `screen` (パソコンやスマートフォンなどのブラウザ) が適用される。

```html
<link rel="stylesheet" media="screen" href="style/index.css">
```

## style タグ

`<style>` タグは文書内でCSSを記述するときに使う。  
基本的に CSS は `<link>` タグで外部から指定した方がいい。

