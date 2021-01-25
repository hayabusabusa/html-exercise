# 3-11. 指定した要素を回り込みさせる

文章などの回り込みの指定について。

## 要素の回り込みを指定する

`float` を使うことで要素を浮かせて左右のどちらかに寄せることができる。  
指定した要素のあとに続く要素は右か左に回り込む。

```css
float: left ;
```

| float 指定なし | float 指定あり |
| :-: | :-: |
| <img width="676" alt="スクリーンショット 2021-01-25 11 06 00" src="https://user-images.githubusercontent.com/31949692/105652731-5c1be180-5efd-11eb-9a7d-ac31463af005.png"> | <img width="677" alt="スクリーンショット 2021-01-25 11 06 11" src="https://user-images.githubusercontent.com/31949692/105652734-5de5a500-5efd-11eb-8391-84ddad68e03f.png"> |

## 回り込みを解除する

`clear` で `float` による回り込みの解除を行うことができる。

```css
clear: both ;
```

## floatやclearの使い所

どちらも左右にコンテンツが横に並ぶようなレイアウトの時に使用する。

| float と clear のサンプル |
| :-: |
| <img width="677" alt="スクリーンショット 2021-01-25 12 04 23" src="https://user-images.githubusercontent.com/31949692/105656416-807bbc00-5f05-11eb-95c4-30e84ab1e264.png"> |

擬似要素による **clearfix** がされていないと、無理やり要素を並べようとしてレイアウトが崩れてしまう。

| レイアウト崩れ |
| :-: |
| <img width="677" alt="スクリーンショット 2021-01-25 12 03 22" src="https://user-images.githubusercontent.com/31949692/105656410-7b1e7180-5f05-11eb-9a42-db27a8bc29a0.png"> |

floatを使う場合は、文字や画像などの要素が増えたときに、レイアウト崩れが発生しないか確かめるようにした方がいい。

# 気づいたこと

## float 指定すると intrinsic content size が効かなくなる

中のコンテンツのサイズによって大きさが変わるようなコンテナを用意して、`float` 指定した要素を中に入れると、要素の持つ最低限のサイズや指定したサイズがコンテナに反映されなかった。

これらは `:after` で **clearfix** してあげると直りそう。

| float 指定なし | float 指定あり |
| :-: | :-: |
| <img width="676" alt="スクリーンショット 2021-01-25 10 59 31" src="https://user-images.githubusercontent.com/31949692/105652475-b36d8200-5efc-11eb-9269-fa198d91ddc3.png"> | <img width="676" alt="スクリーンショット 2021-01-25 11 00 59" src="https://user-images.githubusercontent.com/31949692/105652460-a781c000-5efc-11eb-91bf-3f5e3b6d9b36.png"> |