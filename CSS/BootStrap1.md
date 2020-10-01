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
``` 
<div class=" bg-success text-center p-5">
   <h2 id="whoami">whoami自己紹介</h2>
   <p>私は公立千歳科学技術大学の科技大太郎だよ。<br> なんつって</p><!--段落-->
</div>
```  
# WORKS
```
<div class="bg-warning text-center p-5">
   <h2 id="works">works</h2>
   <!--gridですよ-->
   <div class="container">
      <div class="row">
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQJUvYGK45eOFgPFlX7pin1W3ptz8jq5i02JA&usqp=CAU" alt="" class="col">
      <p class="col">これはCISTLTサークルのホームページです。<br>画像はサークルメンバーでチーム開発したローランドさんです。<br>React.jsをつかっています。</p>
      </div>
   </div>
</div>
```  
# CONTACT
``` 
<div class=" bg-danger text-center p-5">
     <h2 id="contact">contactアクセス</h2>
     <p>科技大@メールアドレスドットコム</p>
</div>
```  

# Footer
```
<footer class="footer bg-info text- p-5">
      <p>&copy:Copyright CISTLT. ALL rights reserved</p>
</footer>
``` 
