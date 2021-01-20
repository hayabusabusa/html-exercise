# 2-7. レイアウトを区切るタグ

ページ全体のレイアウトを区切るためのタグについて。

## Webページのレイアウト

Webページは基本的に以下のような構成になっている。

| Webページの構成 |
| :-: |
| ![web-page-layout](https://user-images.githubusercontent.com/31949692/105130236-fd83eb80-5b29-11eb-99c1-cd001ad352d2.png) |

上記のようなレイアウトを区切るタグとして以下のタグがある。

- `header`
- `main`
- `aside`
- `footer`

## header タグ

`<header>` タグは文章の導入部分やナビゲーション（目次）などをいれる要素。  
サイトのメインタイトルやロゴ、検索窓やグローバルナビゲーションなどが配置される。  

```html
<header>
  <h1>HTML5</h1>
  <p>HTML5がどのように使われるか説明します。</p>
</header>
```

## main タグ

`<main>` タグはそのページの文章のメインとなるコンテンツをいれる要素。  
そのページ内だけで使われる文章を配置する。ロゴや検索窓のような他のページでも共通で表示するような要素は配置しない。  

```html
<main>
  <article>
    <h2>HTML5の書き方</h2>
    <p>開始タグと閉じタグで文章構造を囲みましょう</p>
  </article>
</main>
```

## aside タグ

`<aside>` 要素はサイドバーなどの文章のメインではない補足情報をいれる要素。  
メインのコンテンツと関係ない広告を表示したり、開いているページに関連する記事の一覧などを配置する。  

```html
<aside>
  <h2>その他の使い方</h2>
  <ul>
    <li>
      <a href="howtocss.html">CSSの使い方</a>
    </li>
    <li>
      <a href="howtojavascript.html">JavaScriptの使い方</a>
    </li>
  </ul>
</aside>
```

## footer タグ

`<footer>` タグは著作権に関する情報や、ナビゲーションなどをいれる要素。  
ヘッダーに表示しきれなかったナビゲーションを、ここには省略せずに表示させることが多い。  

```html
<footer>
  <address>
    <p>Copyright &copy; chot.design</p>
  </address>
</footer>
```