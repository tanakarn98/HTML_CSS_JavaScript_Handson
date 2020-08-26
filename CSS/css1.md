# CSS Handson

## CSSとは？  
CSSはHTMLにスタイル機能を提供する言語です  
HTMLがページのコンテンツを記述するための言語なのに対し、CSSはそのコンテンツの表示の仕方をコントロールするもの  
つまり、デザインするやつ！！！！  


## CSSを書く場所

index.html  
```
<p style="color: #ff0000;">ねこ</p>
```  
ねこが赤くなる


```
<p>ぞう</p>
<style>
  p{color: #ff0000;}
</style> 
```  
ぞうが赤くなる
など書ける  

### 基本は外部ファイルで書く

cssファイルをつくる
style.cssをhtmlと同じ場所につくろう！  
-index.html  
-style.css

拡張子は.css  


## CSSの書き方の流れ

HTMLのタグにCSSのクラスを当てることでデザインを加えることができます。  
しかし、結構ややこしいので、実際にやりながら見てみましょう！  

まずは、こんな感じでHTMLを書きましょう。

index.html  
```
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="utf-8">
  <title>タイトル</title>
  <meta name="description" content="サイトの説明を記載します">
  <link rel="icon" href="favicon.ico">
</head>
<body>
    <div>
        <h2>logoロゴ</h2>
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSq6KW6PvwJa8URGELal4IjFPENpJ0gr0JsVQ&usqp=CAU"><!--画像-->
    </div>

    <div>
        <h1>ポートフォリオだよ</h1><!--大見出し-->
    </div>

    <div>
        <h2>whoami自己紹介</h2>
        <p>私は公立千歳科学技術大学の科技大太郎だよ。<br> なんつって</p><!--段落-->
    </div>

    <div>
        <h2>contactアクセス</h2>
        <p>科技大@メールアドレスドットコム</p>
    </div>
</body>
</html>
```


**背景色を指定する background-color**  

背景色  
```
background-color:red;
```  
redの部分を好きな色に変えられる  


htmlと同じ階層にstyle.cssを作る  
ここにCSSを当てていきます。  
CSSのコードは以下の形で背景色をつけていきます。

sytle.css  
```
.wrapper{
    background-color: hotpink;
}

.top{
    background-color: brown;
}

.portfolio{
    background-color: blue;
}

.whoami{
    background-color: blueviolet;
}

.contact{
    background-color: chartreuse;
}

```  


cssの外部ファイルを読み込もう！  
headに書こう！
```
<link rel="stylesheet" href="style.css">
```  


**class属性を追加する**  


class属性の書式  
```
divタグの場合
<div class="クラス名"></div>をつける  

pタグの場合
<p class="クラス名">帰納法</p>
```  

  
class属性は、そのタグが所属するグループの名前を指します  


**divタグにclass属性をつけてみよう！**  


index.html  
```
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="utf-8">
  <title>タイトル</title>
  <meta name="description" content="サイトの説明を記載します">
  <link rel="icon" href="favicon.ico">
  <link rel="stylesheet" href="style.css">
</head>
<body>
<div class="wrapper"><!--ここ-->
    
    <div class="top">　<!--ここ-->
        <h2>logoロゴ</h2>
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSq6KW6PvwJa8URGELal4IjFPENpJ0gr0JsVQ&usqp=CAU">
    </div>
    
    <div class="portfolio"> <!--ここ-->
        <h1>ポートフォリオだよ</h1>
    </div>

    <div class="whoami">　<!--ここ-->
        <h2>whoami自己紹介</h2>
        <p>私は公立千歳科学技術大学の科技大太郎だよ。<br> なんつって</p>
    </div>

    <div class="contact">　<!--ここ-->
        <h2>contactアクセス</h2>
        <p>科技大@メールアドレスドットコム</p>
    </div>
</div>
</body>
</html>
```  

classがわかったでしょうか？  
背景色をつけるとグループ分けがわかりやすいですね！  

class属性はHTMLのすべてのタグにつけることができる  
また、複数のタグに同じクラス名をつけることも可能
逆に、1つのタグに複数のクラス名をつけることも可能  


※クラス名は表示するコンテンツの内容を説明するものをつけよう！

## CSSのコメント文  

```
/*
ガールズルール　裸足でSummer シンクロニシティ 
*/
```  
コメント文の中に/*　はいれてはいけない  

## フォント、フォントサイズ

**フォント font-family: serif;**  
sans-serif　ゴシック  
serif 明朝  

style.css  
```
html {
  font-family: sans-serif;
}
```  
デフォはゴシックなので変化はないが、serifにすると変化するので確かめてみてください。  


**フォントサイズ font-size: 20px;**  

font-size: 数字px  
数字でサイズを指定できる  

style.css  
```
p {
  font-size: 22px;
}

```
文字が大きくなることを確認する  


## px % em
px
コンピュータディスプレイの解像度の点の大きさ  
20oxは20個分  

%
スタイルを適用しないときの幅やフォントサイズと比べて何%の大きさで表示させるか  

em
要素に設定されたフォントサイズ  

pxか%で雰囲気でいきこう！(一番よくない)  


## CSSのボックスモデル  
マージン
ボーダー
パディング
コンテンツ領域

![image](https://user-images.githubusercontent.com/44164993/91206041-76c90f00-e741-11ea-854c-2e7245dfa31a.png)  

![image](https://user-images.githubusercontent.com/44164993/91206142-a1b36300-e741-11ea-9424-43e2cae78ea9.png)  


## ロゴを真ん中に配置する  

.top{
  margin: 50px 0 40px 0;
  line-height: 0;
  text-align: center;
}
**text-align**  

テキストでも画像でも揃えられる 
text-align: center;
center left rigntなどある 

**margin: 上 右 下 左;**  

4辺のマージンの大きさを1行で設定できるmarginプロパティ  


## ナビゲーションバーをつくろう

htmlの中  
```
<div class="wrapper">
    <div class="portfolio"> <!--ここ-->
        <h1>ポートフォリオだよ</h1>
    </div>

<!--ここから-->
<nav class="nav">
  <ul>
    <li>Top</li>
    <li>Portfolio</li>
    <li>Whoami</li>
    <li>Contact</li>
  </ul>
</nav>
<!--ここまで-->

<div class="whoami">　<!--ここ-->
        <h2>whoami自己紹介</h2>
        <p>私は公立千歳科学技術大学の科技大太郎だよ。<br> なんつって</p>
    </div>
```  
ナビゲーションバーができた！  

style.cssの一番下  
```
.nav li{
display: inline;
list-style-type: none;
padding-right: 30px;
}
```  
**display: inline**  
インラインボックスとして表示  

**list-style-type**  

list-style-type:none;でナビゲーションバーのリスト  
・あいう
・えおか
・きくけ
の・が消える  

**padding right**  
padding right: 30px;  

パディングの右側を30px開ける  


**ナビゲーションバーの固定**  

```
 .nav{
  position: fixed;
}
```    


???いらないかな？  
## 背景画像の指定  
.nav ul{
  margin: 0 0 0 0;
  padding: 20px 10px 15px 20px;
  background-image: url(../img/back.png);
  background-repeat: repeat-x; //いらない  
}
???

## ナビゲーションバーのリンクの色を変える  
まずナビゲーションバーの遷移先を作ろう！  
```
<nav class="nav">
  <ul>
    <li><a href="#top">Top</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#whoami">Whoami</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
```  
```
<div>class="top" id="top"</div>
<div>class="portfolio" id="portfolio"</div>
<div>class="whoami" id="whoami"</div>
<div>class="contact" id="contact"</div>
```  

リンクの色を変える  

```
.nav a:link{
  color: yellow;
  text-decoration: none;
}

.nav a:visited{
  color: yellow;
  text-decoration: none;
}

.nav a:hover{
  color: yellow;
  text-decoration: none;
}
.nav a:active{
  color: yellow;
  text-decoration: none;
}
```  

a:link　：アクセスしたことのないリンク  
a:visited　：アクセスしたことのあるリンク  
a:hover　：マウスが上に乗っている状態のリンク  
a:active　：クリック中のリンク  


## フッターを作成  

著作権みたいなお作法  
作った人や作った西暦を書く  

index.html  
```
<footer class="footer">
  <p>&copy:2020 Copyright CISTLT. ALL rights reserved</p>
</footer>
```  

style.css  
```
.footer{
  background-color: red;
  margin-top: 30px;
  padding: 80px 15px 20px 15px;
  font-size: 12px;
  color: red;
}
```  

???最大幅の確認ができていない  
## ページの最大幅の設定  

ページの最大幅を設定して、ウインドウ中央に配置する  
style.css  
```
body{
  margin: 0 0 0 0;
}

.wrapper{
margin: 0 auto 0 auto;
max-width: 960px;
}

```  
wrapperのbackground-color: hotpink;を  
body{
  background-color: hotpink;
}
に書き換える  

左右のマージンをautoにするとページが中央ぞろえになる  
ページの幅が横に広くなりすぎると見づらいので、伸縮する最大幅だけは設定する  

max-widthプロパティは、ボックスの最大幅を設定するのに使う。今回はこの値を960pxにしている  


## worksをつくろう!  
**フレックスボックス**  

自己紹介の下にworksをつくる  
```
<div class="works" id="works">
      <img src="3.jpg" alt="" class=works-img>
      <p class="works-p">これはCISTLTサークルのホームページです。サークルメンバーでチーム開発をしました。React.jsをつかっています。</p>
</div>
```  

ナブバーにworksを追加  

```
<li><a href="#works">Works</a></li>
```  

画像サイズの変更  
```
.works-img {
    display: block;
    width: 400px;
}

```


画像とテキストを横に並べる  
```
.works{
    display: flex;
  }
  .works-p {
    border-bottom: 1px dashed #bec2c7;  
    padding: 20px 8px;
 }
  .works-img {
    display: block;
    width: 400px;
    margin-right: 16px;
    }
   ```  
   
display:flexで自動的に横に並ぶ  


.works-img{
  flex: 1 1 auto;
}
横に並んだボックスのうち、幅を伸縮させたい  

.works-p{
  flex: 0 0 400px;
}
横に並んだボックスのうち、幅を固定させたいflex:0 0 固定幅  



## レスポンシブデザイン  

スマートフォンやパソコンなどのすべての端末に対応できるページを作る方法を
レスポンシブデザインという！  

レスポンシブ3か条  
*ページの横幅がウインドウに合わせて伸縮できる
*表示できる面積に合わせて、画像を伸縮できる  
*画面サイズに合わせて、最適なレイアウトに切り替える(スマホならナビゲーションバーが3本線のハンバーガーメニューになるとか)  

chromeブラウザを右クリックで検証し、端末ごとのサイズを見てみよう！  f12かその他のツールデベロッパツール

せいぜい楽しんだら  
```
 <meta name="viewport" content="width=device-width, initial-scale=1" />
 ```  
 を<head>の中に記述する  
  
  ビューポートは表示画面のこと  
  viewportを設定していないPC向けのページをスマートフォンで表示すると、文字もページも小さくなってしまいます。「viewport」の概念は、デスクトップPCだけの環境では意識する必要はあまりありませんでした。ですが、今はデスクトップPCよりタブレット等の使用頻度が高くなり、見やすくするためにそれぞれのデバイスでのズレがないように指定する必要が出てきました。
設定されていないと、横幅いっぱいでおさまらないコンテンツや本文は横のスクロールがついて表示されてしまい、閲覧しにくくなってしまいます。そこで、viewportを指定することで、画面幅いっぱいにコンテンツや本文がおさまるようにしていくのです。  


ただ、viewportを設定しただけでは最適化されたとは言えません。viewportでは表示領域を設定して、ページが見やすいように拡大されているだけになっています。これを解消するために、スマートフォン用にCSSでレイアウトを設定してあげる必要があります。  


表示されている画像を伸縮させる  

<img>タグのcssを追加する  
```
img {
  max-width: 100%;
  height: auto;
}
```  


ブラウザ伸び縮みさせてみてー
変わったのわかった？  

メディアクエリを使用する  
style.cssの一番下に@mediaを記述する  

```
@media (max-width: 768px) {

}
```  


@medhiaはメディアクエリといわれ()の条件をみたしたときに適用するスタイル  
768pxはなに？  
標準的なタブレット端末(ipad)の四辺の短い2辺の長さ
768以下がスマホや小型タブレット
あとはノートパソコン、ディスプレイとか
768をブレイクポイントといい、ipadの画面幅にするのが一般的  
デベロッパーツールのipadを選択すると768pxとなっているのがわかる  


モバイル表示のときだけページの左右にスペースをつくる  
メディアクエリの中
```
.wrapper{
  margin: 0 8px;
}
```  

メディアクエリの条件を満たすときのスタイル  

ロゴ画像のサイズを指定する  
メディアクエリの中
```
.top{
  margin: 30px 0;
}

.top img{
  width: 200px;
}
```  


スマホのとき、ナビゲーションのリストを縦に並べる  
メディアクエリの中  
```
.nav {
  background-color: #dfddda;
}

.nav li{
  display: block;
}
```  



画像とテキストのフレックスボックスを解除する
画面幅が狭いのでレイアウトを解除する必要がある  

メディアクエリの中  
```
.works{
  display: block;
}
.works-img{
  margin-right: 0;
  width: 100%;
}
.works-p{
  width: 100%;
}
```  


おけー！！！！！CSS終わり！！
