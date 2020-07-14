## はじめに
「HTML　テンプレート」等のキーワードで検索すると、プロのデザイナーやコーダーが作成したHTML+CSSのセットが大量にあり、これらをダウンロードしてカスタマイズし、オリジナルのサイトを作ることができます。  
例：[無料テンプレ配布サイト](http://websae.net/html5-templates-20140519/)

今回は、「bolt」というテーマを利用して、自己紹介ページをより魅力的に作ってみましょう。  
（参考：[色辞典](http://www.colordic.org/)も使いながら、配色やレイアウトを変更してみてください）

## bolt
<img src="http://hackers.nexseed.net/images/curriculum_images/bolt_1.png" alt="Overview" style="width: 80%;">

[bolt ダウンロードページ](http://blacktie.co/2013/11/bolt-flat-one-page-theme/)

boltのテンプレートには、以下の技術が使われています。

* **Bootstrap**
    * Twitter社が開発したノンデザイナー向けのHTML+CSSフレームワーク（[公式サイト](https://getbootstrap.com/docs/3.3/)）
* **Font Awesome**
    * 図形をフォント（文字）で表現できる、ノンデザイナーのためのアイコンフォント（[公式サイト](http://fontawesome.io/)）
* **JavaScript**
    * ブラウザ側（クライアントサイド）で動作するプログラミング言語

#### ▼ 練習問題１
boltのテンプレート、もしくはその他のHTMLテンプレートを使って、自分の自己紹介ページを作ってみましょう。  
以下のコンテンツを必ず含めるようにしてください。その他は自由です。

* 名前（ニックネーム）
* 出身地
* 趣味
* その他自己アピール

[こちらから動画で作業を確認できます↓](https://youtu.be/V99s8V32EoE)

[![こちらから動画で作業を確認できます](https://img.youtube.com/vi/V99s8V32EoE/0.jpg)](https://youtu.be/V99s8V32EoE)

## Bootstrap
BootstrapはCSSのフレームワークで、HTMLファイルからCSSフレームワークを読み込むだけで、リッチなスタイルが適用されたデザインを作ることができます。
既に用意されているスタイルを適用するだけなので、HTML/CSSといったWebデザインの知識がない人でも、簡単に見栄えの良いWebページを作成できます。

また、Bootstrapは **レスポンシブデザイン対応** （ウィンドウのサイズに合わせて、自動的にページのデザインを最適化する技術）になっているので、自分でPC用のCSS・スマホ用のCSSを設定することなくレイアウトを整えることができます。

公式サイトからダウンロードして、実際に使ってみましょう。  
ダウンロードしたら、デスクトップにある「basic」フォルダの中にファイルを移動してダブルクリックし、解凍しておいてください。

[Bootstrapの公式サイト](https://getbootstrap.com/docs/3.3/)

### Bootstrapのフォルダ構成

<img src="http://hackers.nexseed.net/images/curriculum_images/bootstrap_1.png" alt="Overview" style="width: 80%;">

### すぐ使えるテンプレート
Bootstrapの公式ページには、すぐにBootstrapを試せるサンプルがあります。

1. 公式サイトのダウンロードページにある「[Basic Templete](http://getbootstrap.com/getting-started/#template)」へ移動
2. このコードをコピーする
3. ダウンロードしたBootstrapフォルダの直下に、index.htmlを作成して2でコピーしたコードを貼り付ける
4. 3で作成したindex.htmlをダブルクリックしてブラウザで開き、「Hello world」が表示されることを確認


#### ▼ 練習問題２
index.htmlに次のコードを追加して、ボタンを作ってみましょう。

```html
<button type="button" class="btn btn-default">Default</button>
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-danger">Danger</button>
```

[公式ページ](http://getbootstrap.com/css/)に、ボタン以外にも色々サンプルが載っていますので参考にしてみてください。

[こちらから動画で作業を確認できます↓](https://youtu.be/rM1oM0-uKW8)

[![こちらから動画で作業を確認できます](https://img.youtube.com/vi/rM1oM0-uKW8/0.jpg)](https://youtu.be/rM1oM0-uKW8)

#### ▼ 練習問題３
公式ページの[テーブル](http://getbootstrap.com/css/#tables-hover-rows)を参考に、index.htmlに次のコードを追加して、テーブルを作ってみましょう。

```html
<table class="table table-hover">
  <thead>
    <th>見出し１</th>
    <th>見出し２</th>
    <th>見出し３</th>
  </thead>
  <tbody>
    <tr>
      <td>セル１</td>
      <td>セル２</td>
      <td>セル３</td>
    </tr>
    <tr>
      <td>aaa</td>
      <td>bbb</td>
      <td>ccc</td>
    </tr>
  </tbody>
</table>
```
[こちらから動画で作業を確認できます↓](https://youtu.be/OPDmB6mJxfY)

[![こちらから動画で作業を確認できます](https://img.youtube.com/vi/OPDmB6mJxfY/0.jpg)](https://youtu.be/OPDmB6mJxfY)

### グリッドシステム
Bootstrapは、 **グリッドシステム** と呼ばれる大きな特徴を持っています。  
グリッドシステムとは、横幅を12個に分割し、合計が12個になるようスタイルを指定することでサイトの枠組みを構築できるシステムです。  
Bootstrapはこのグリッドシステムにより、レスポンシブデザインを手軽に実現できるようになっています。

グリッドシステムは、モバイル・タブレット・デスクトップ・幅広デスクトップの4つの表示領域に対応しています。

[公式ページ](http://getbootstrap.com/css/#grid)

[日本語ページ](http://bootstrap3.cyberlab.info/css/gridSystem.html)

### グリッドシステムの使い方
１．class属性に「row」を指定したdiv要素を用意する（このdiv要素は、clsss属性に「container」を指定した要素内に設置すること）

```html
<div class="container">
	<div class="row">

	</div>
</div>
```

２．１のdiv要素内に、class属性にcol-xx-xxを指定したdiv要素を配置する

```html
<div class="container">
	<div class="row">
		<div class="col-md-4">カラムA</div>
		<div class="col-md-4">カラムB</div>
		<div class="col-md-4">カラムC</div>
	</div>
</div>
```

* col-xx-xxにおける１つ目のxxには、表示幅を意味するxs、sm、md、lgの何れかを指定します。  
  xsはスマホ、smはタブレット、mdはPC、lgはPC大画面（1200px以上）のサイズになります。
* col-xx-xxにおける２つ目のxxには、カラム数を指定します。一行における最大カラム数は **12** です。  
  1つのrow内の合計が12であれば、何個に区切っても構いません。（4:8、3:7:2、12:0 など）

公式ドキュメントではありませんが、以下のサイトもBootstrapについてわかりやすくまとめられているので、興味のある人は見てみてください。

[Bootstrap3の使い方](http://bootstrap3-guide.com/)

#### ▼ 練習問題４
次のコードをindex.htmlに追記してみましょう。ブラウザで表示が確認できたら、「col-xx-xx」の部分を変更して動きを確認してみましょう。

```html
<div class="container">
  <div class="row">
    <div class="col-md-2" style="background-color: red; color: white;">赤</div>
    <div class="col-md-8" style="background-color: blue; color: white;">青</div>
    <div class="col-md-2" style="background-color: green; color: white;">緑</div>
  </div>
</div>
```

## Bootsnipp
[公式ページ](http://bootsnipp.com/)

<img src="http://hackers.nexseed.net/images/curriculum_images/bootsnipp_1.png" alt="Overview" style="width: 80%;">

「snipp」「snippet」は切れ端という意味で、 **Bootsnipp** はBootstrapで作られたスニペットをシェアできるサービスです。  
コンテンツのパーツを作るのに便利なサービスです。

例えば、自分でフォームのデザインを簡単に作れる[Form Builder](http://bootsnipp.com/forms)や、ボタンを簡単に作れる[Button Builder](http://bootsnipp.com/buttons)があります。  
また、他のユーザが作成したレイアウト（スニペット）を閲覧したりそのHTML／CSSを取得することもできます。

#### ▼ 練習問題５
Form BuilderやButton Builderで作成したフォームやボタンを、index.htmlに貼り付けてレイアウトを確認してみましょう。

## 次のページへ
[スキルアップのために](https://github.com/NexSeed00/Prior_Learning/blob/master/09_%E3%82%B9%E3%82%AD%E3%83%AB%E3%82%A2%E3%83%83%E3%83%97%E3%81%AE%E3%81%9F%E3%82%81%E3%81%AB.md)
