# 2-11. 表組みレイアウトについて

**表組み**のようなレイアウトを表すタグについて。

## 表組みレイアウトとは

料金表や比較表などを表すために使われる表組みレイアウト。  
表組み全体を示す `<table>` や、ヘッダ行を示す `<thead>`、表の行をグループ化する `<tbody>`、横一行を示す `<tr>`、見出しセルを示す `<th>`、データセルを示す `<td>` がある。

## table タグ

表組み全体を示すには `<table>` タグを使用する。 

### border 属性

外枠線の幅を数字( px )で指定する。

```html
<table border="1">
  <tr><td>A</td><td>B</td></tr>
  <tr><td>C</td><td>D</td></tr>
</table>
```

### cellpadding 属性

セルの枠と文書の間隔を数字( px )で指定する。  

```html
<table border="1" cellpadding="10">
  <tr><td>A</td><td>B</td></tr>
  <tr><td>C</td><td>D</td></tr>
</table>
```

### cellspacing 属性

セルの枠と文書の間隔を数字( px )で指定する。

```html
<table border="1" cellspacing="10">
  <tr><td>A</td><td>B</td></tr>
  <tr><td>C</td><td>D</td></tr>
</table>
```

| border | cellpadding | cellspacing | cellspacing="0" |
| :-: | :-: | :-: | :-: |
| ![border](https://user-images.githubusercontent.com/31949692/105187342-069aaa00-5b76-11eb-8cc8-b8ff6eab9c63.png) | ![cellpadding](https://user-images.githubusercontent.com/31949692/105187405-17e3b680-5b76-11eb-849a-bc74a53f2363.png) | ![cellspacing](https://user-images.githubusercontent.com/31949692/105187443-25993c00-5b76-11eb-9a96-3785e5ae613d.png) | ![cellspacing_zero](https://user-images.githubusercontent.com/31949692/105187474-2f22a400-5b76-11eb-8abf-6e26f9812369.png) |

## thead タグ

`<thead>` タグは表の中のヘッダ行（見出し）に使われる要素。

| thead |
| :-: |
| <img width="680" alt="スクリーンショット 2021-01-20 23 24 14" src="https://user-images.githubusercontent.com/31949692/105187946-b3752700-5b76-11eb-9b78-3dbfcd743e33.png"> |

## tbody タグ

`<tbody>` 要素は表のボディ部分（本体）を定義するタグ。

| tbody |
| :-: |
| <img width="670" alt="スクリーンショット 2021-01-20 23 32 37" src="https://user-images.githubusercontent.com/31949692/105188986-d5bb7480-5b77-11eb-89a6-d94e4f45c7e2.png"> |

## tr・th・td タグ

表組みの中には行とセルを設置する必要がある。セルは見出しセルとデータセルに分かれる。  

| tr・th・td |
| :-: |
| <img width="666" alt="スクリーンショット 2021-01-21 10 54 31" src="https://user-images.githubusercontent.com/31949692/105269406-2e6e2a00-5bd7-11eb-9218-4659e94df973.png"> |

```html
<table border="1" cellpadding="10">
  <thead>
    <tr><th>商品</th><th>単価</th><th>数量</th><th>小計</th></tr>
  </thead>
  <tbody>
    <tr><td>りんご</td><td>100円</td><td>10</td><td>1000円</td></tr>
    <tr><td>バナナ</td><td>200円</td><td>5</td><td>1000円</td></tr>
    <tr><td>みかん</td><td>150円</td><td>12</td><td>1800円</td></tr>
    <tr><td>ぶどう</td><td>120円</td><td>3</td><td>360円</td></tr>
  </tbody>
</table>
```