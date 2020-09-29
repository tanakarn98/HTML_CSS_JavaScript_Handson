# 前回の復習

クラスを当てるとスタイルが反映されましたね！

index.html
```
<p class="blue">ここが青色になります</p>
```

index.css
```
.blue{
 color:blue
}
```

# BootStrapとは  

CSSファイルがなくても、クラス名を当てるだけでスタイルを読み込んでくれます！

https://getbootstrap.jp/  

```
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>  
```  

# BootStrapを読み込みましょう！  

```
<!doctype html>
<html lang="ja">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- ここでBootStrapを読み込んでるよ！ -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
     </body>
</html>  
```  

# ひな形
https://elastic-pike-36aad9.netlify.app/

![screencapture-elastic-pike-36aad9-netlify-app-1601379393820](https://user-images.githubusercontent.com/56716847/94553836-0fe4cb80-0294-11eb-811c-a773b2d3bdfd.png)



# カラー  

```
<p class="text-danger">赤色</p>
```  

# 背景色

```
<p class="bg-primary">背景色が青になりますよ</p>
```  

# ナビゲーションバー

```
<nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
  <a class="navbar-brand" href="#top">Top</a>
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

# グリッド
親要素に row
子要素に col
をつける
子要素は幾つでも増やせます。

```
<div class="row">
  <div class="col">1 of 2</div>
  <div class="col">2 of 2</div>
</div>
``` 


# 最後にOGP

https://ferret-plus.com/610

シェアするときにあった方がいいです！
headの中に書きましょう。

