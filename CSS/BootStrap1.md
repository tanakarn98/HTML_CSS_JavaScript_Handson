# 前回までの復習

index.html
```
<p class="blue">青にしたいです</p>
```

index.css
```
.blue{
 color:blue;
}
```

# BootStrapとは  
CSSファイルを書かなくて良くなる便利なもの！

https://getbootstrap.jp/  

```
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>  
```  

# 使うには読み込みが必要・・・  

実際のコード
```
<!doctype html>
<html lang="ja">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- ここでBootStrapを読み込んでいるよ！ -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
  </body>
</html>  
```  

# 今回作るもの
https://portfolio-cistlt.web.app/
![screencapture-portfolio-cistlt-web-app-1601515146316](https://user-images.githubusercontent.com/56716847/94755476-a7026e00-03cf-11eb-9382-9c440102b116.png)


# Navbar
これ以降は<body></body>内に書いていきましょう！
親要素に　
```
class="navbar"
```  
子要素に
```
class="navbar-item"
``` 
ページ内リンクは
```
<a href="#works"></a>
``` 
とすることで
```
<div id="works"></div>
``` 
のところまで飛んでくれるよ！

実際のコード
```  
<nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
  <a class="navbar-brand" href="">Top</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link" href="#portfolio">Portfolio <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#whoami">Whoami</a>
      </li>
      <!--works-->
      <li class="nav-item">
        <a class="nav-link" href="#works">Works</a>
      </li>
      <!--works-->
      <li class="nav-item">
        <a class="nav-link" href="#contact">Contact</a>
      </li>
    </ul>
  </div>
</nav>
```  

# ヒーローエリア
##背景色
```
<div class="bg-primary">青色になるよ</div>
``` 
##文字の中央寄せ
``` 
<p class="text-center">真ん中寄せになるよ</p>
``` 
まとめて真ん中寄せ
``` 
<div class="text-center>
  <h2>yeah!</h2>
  <p>wow!</p>
</div>
``` 

##padding
``` 
<div class="p-5">上下左右にpaddingが設定されるよ</div>
```
##画像のソース
どちらでもOK!
``` 
src="絶対パス"
src="相対パス"
```
絶対パス とは・・・https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSq6KW6PvwJa8URGELal4IjFPENpJ0gr0JsVQ&usqp=CAU
相対パス とは・・・自分のパソコンにダウンロードして、ファイルに入れた画像の場所　"./assets/images/dog.jpg"

実際のコード
```  
<div class="bg-primary text-center p-5">
   <h2>logoロゴ</h2>
   <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSq6KW6PvwJa8URGELal4IjFPENpJ0gr0JsVQ&usqp=CAU"><!--画像-->
</div>

<div class="bg-secondary text-center p-5">
    <h1 id="portfolio">ポートフォリオだよ</h1><!--大見出し-->
</div>
```  


# 自己紹介
実際のコード
``` 
<div class=" bg-success text-center p-5">
   <h2 id="whoami">whoami自己紹介</h2>
   <p>私は公立千歳科学技術大学の科技大太郎だよ。<br> なんつって</p><!--段落-->
</div>
```  
# WORKS
##gird
いい感じに並べてくれるくん
親要素
```
<div class="row"></div> 
```
子要素
いくつでも増やせる！
```
<div class="col"></div> 
```

##改行
あんまりよくないけど<br>が便利！
ほんとは改行したい文章ごとに<p></p>で囲おう！

実際のコード
```
<div class="bg-warning text-center p-5">
   <h2 id="works">works</h2>
   <!--gridですよ-->
   
   <div class="row">
   <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQJUvYGK45eOFgPFlX7pin1W3ptz8jq5i02JA&usqp=CAU" alt="" class="col">
   <p class="col">これはCISTLTサークルのホームページです。<br>画像はサークルメンバーでチーム開発したローランドさんです。<br>React.jsをつかっています。</p>
   </div>
   
</div>
```  

# CONTACT
実際のコード
``` 
<div class=" bg-danger text-center p-5">
     <h2 id="contact">contactアクセス</h2>
     <p>科技大@メールアドレスドットコム</p>
</div>
```  

# Footer
実際のコード
```
<footer class="footer bg-info text-center p-5">
      <p>&copy:2020 CISTLT. ALL rights reserved</p>
</footer>
``` 
