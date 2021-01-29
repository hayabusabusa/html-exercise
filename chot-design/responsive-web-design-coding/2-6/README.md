# レスポンシブデザインのLP実装

## 完成形

| PC | SP |
| :-: | :-: |
| ![chot-design_responsive-web-design-coding_2-6_index](https://user-images.githubusercontent.com/31949692/106277440-739bf700-627c-11eb-8be0-b3fa98eecfb5.jpg) | ![chot-design_responsive-web-design-coding_2-6_index html(iPhone X)](https://user-images.githubusercontent.com/31949692/106277337-3fc0d180-627c-11eb-9c45-0bc41c3555fa.png) |

## 画像の準備

PCよりSPの方が大きい画像を使用している場合がある。これは **Retina 対応**するため。  
レスポンシブサイトを作る際にPCの画像をそのままスマホに使ってしまうと画像の解像度が足らずボケてしまうことがあるので注意する。

> 今回は2倍のサイズで作成しているが、iPhone X・iPhone XSに対応する場合は3倍のサイズにする必要があるらしい

## ヘッダーの実装

| ヘッダー部分 |
| :-: |
| <img width="1440" alt="スクリーンショット 2021-01-26 21 17 32" src="https://user-images.githubusercontent.com/31949692/105844107-068a2680-601c-11eb-9851-20d89486cb68.png"> |

### wrap について

今回の場合 `header__wrap` というクラスが作られているが、こういう `xxxwrap` みたいなよくみるクラスについて。  
これらは**画面の幅を制御する事に特化した class** のことっぽい。

- [wrapの書き方｜再現度120%！デザイナーの脳内イメージも実装するHTML / CSS - note](https://note.com/ryotodo/n/n58c452d3660c)

## キービジュアルの実装

メディアクエリを使用して画像をスマホ用の物に切り替えたり、絶対位置で配置したテキストの位置を調整する。

| キービジュアル部分 |
| :-: |
| <img width="1440" alt="スクリーンショット 2021-01-26 21 17 39" src="https://user-images.githubusercontent.com/31949692/105844111-08ec8080-601c-11eb-8c84-db26cdf97563.png"> |

## インタビューの実装

| インタビュー部分 PC | インタビュー部分 SP |
| :-: | :-: |
| <img width="1440" alt="スクリーンショット 2021-01-27 20 32 21" src="https://user-images.githubusercontent.com/31949692/105985484-db1c4000-60de-11eb-854e-590aed82457b.png"> | <img width="325" alt="スクリーンショット 2021-01-27 20 32 47" src="https://user-images.githubusercontent.com/31949692/105985521-e7a09880-60de-11eb-87c1-3aeaad20faca.png"> |

### 画像のサイズについて

画像のサイズは基本的には画像自体のサイズが反映される。  
CSS で `width: 100%` とかにしてあげると、その幅に合わせて高さがコンテンツによって変わる。  

そのままでは高さがガタガタになってしまうので、CSS でなんとかさせたい。

```css
.image-box {
  position: relative;
  overflow: hidden;
  padding-top: 60%; /* 比率 */
}
.image-box img {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  height: auto;
  transform: translate(-50%, -50%);
}
```

また、そのままではレイアウトシフトが発生してしまうので、`img` タグにサイズを指定してあげるのが今風らしい。

- [サイズがバラバラな画像をレスポンシブで縦横比を揃えて表示させる - Qiita](https://qiita.com/becolomochi/items/265a7f940a1c809f5ba7)
- [【2020年夏】imgタグにはwidthとheight属性を書くのがいいらしい](https://parashuto.com/rriver/development/img-size-attributes-are-back)