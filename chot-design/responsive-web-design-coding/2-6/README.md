# レスポンシブデザインのLP実装

## 完成形

## 画像の準備

PCよりSPの方が大きい画像を使用している場合がある。これは **Retina 対応**するため。  
レスポンシブサイトを作る際にPCの画像をそのままスマホに使ってしまうと画像の解像度が足らずボケてしまうことがあるので注意する。

> 今回は2倍のサイズで作成しているが、iPhone X・iPhone XSに対応する場合は3倍のサイズにする必要があるらしい

- [ロゴ](http://yoshikikojima.github.io/responsive-sample/img/logo.png)
- [キービジュアル]()
- ABOUT
    - [about 1枚目]()
    - [about 2枚目]()
- INTERVIEW
    - [interview 1枚目]()
    - [interview 2枚目]()
    - [interview 3枚目]()
- GALLERY
    - [gallery 1枚目]()
    - [gallery 2枚目]()
    - [gallery 3枚目]()
    - [gallery 4枚目]()
    - [gallery 5枚目]()
    - [gallery 6枚目]()
    - [gallery 7枚目]()
    - [gallery 8枚目]()
    - [gallery 9枚目]()
    - [gallery 10枚目]()
- [フッター]()

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