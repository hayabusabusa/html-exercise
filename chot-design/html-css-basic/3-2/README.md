# 3-2. CSSで文字の色を変更する

CSS で文字の色を変更する方法について。

## カラーネームで色を指定する

文字の色を変更する CSS `color` を使用して文字の色を変更する。  
値には**カラーネーム**、**16進数による表記**、**RGBもしくはRGBAカラーモデル**が入れられる。  

```css
.text { color: red; }
```

## 16進数カラーコードで色を指定する

パソコンやスマートフォンのモニターでは**R( 赤 )・G( 緑 )・B( 青 )**の3色を混ぜ合わせることによって色を表現している( **光の三原色** )。  
それぞれの**色が強ければ強いほど白に近づき、弱ければ弱いほど黒に近づく**。

この３色の強さを16進数で表したのが、**カラーコード**。

```css
.white{ color : #FFFFFF; }
```

## RGB・RGBA カラーモデルで色を指定する

カラーコードは16進数で色の段階を表現していたが、00〜FFまでを10進数で表すと0〜256と表現することができる。  
CSSでは**rgb関数**というものを使えば、10進数でも色の表現をすることができる。

```css
.red{ rgb(255, 0 , 0) }
```

RGBにAlpha( 透過 )が加わったのが**rgba関数**で、色を半透明に出来る。

```css
.red{ rgba(255, 0, 0, 0.5); }
```