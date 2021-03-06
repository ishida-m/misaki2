---
title       : RStudioでスライドを作成する
subtitle    : 『とある弁当屋の統計技師(データサイエンティスト) 2 ―因子分析大作戦―』補足 
author      : 石田基広
job         : 
framework   : html5slides        # {io2012, html5slides, shower, dzslides, ...}
theme       : default
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---
## Rでプレゼンテーション作成


1. まず[Rをインストール](http://cran.ism.ac.jp/)
2. 続いて[RStudioをインストール](http://www.rstudio.com/ide/)
3. それぞれダウンロードしたらダブルクリックしてインストール

<img src="img/download.png" alt="Pi" style="width: 400px;"/>

--- 
## RStudioを起動

FileメニューからR Presentatin を選択

<img src="img/file.png" alt="Pi" style="width: 400px;"/>

ファイル名を尋ねられるので test とか適当に
(ファイル名は半角英数字をお勧めします)

<img src="img/file2.png" alt="Pi" style="width: 400px;"/>

--- 
## プレビューを観る

とりあえずpreviewを押して

<img src="img/preview.png" alt="Pi" style="width: 400px;"/>

ここを押すと、作成されるイメージが確認できます

<img src="img/preview2.png" alt="Pi" style="width: 400px;"/>

--- 
## プレビューを観る2

また拡大アイコンを押すと、新たにウィンドウが現れます

<img src="img/preview3.png" alt="Pi" style="width: 400px;"/>

<img src="img/preview4.png" alt="Pi" style="width: 400px;"/>


--- 
## スライドを作成する

それでは雛形を修正していきましょう(RStudioは日本語入力に少し難があります)

<img src="img/slide1.png" alt="Pi" style="width: 400px;"/>

ここで再びpreviewボタン押して、右Presentationタブを操作してみます

<img src="img/slide2.png" alt="Pi" style="width: 400px;"/>

Macの場合、問題ないと思いますが、Windows環境だと文字化けしてしまいます

<!-- これは次のように修正します -->

--- 
## Windows環境での文字化け修正


Fileメニューから save with Encoding を選択

<img src="img/encode1.png" alt="Pi" style="width: 200px;"/>

 
ダイアログでUTF-8を選んでOK。previewを実行すると文字化けが解消されます

<img src="img/encode3.png" alt="Pi" style="width: 400px;"/>

--- 
## R Presentationの書き方1

Markdownという書式で記述します

詳細はヘルプで確認できます(ただし英語です)

<img src="img/help.png" alt="Pi" style="width: 400px;"/>

Authorizing R Presentation はRStudio上での使い方

Markdown Quick Reference はMarkdown記法の説明

---

## R Presentationの書き方2

とりあえず次のルールを覚えましょう

1. スライドは =============== で区切る
2. Rの命令は ```` ```{r} 改行 ``` ```` の間に書く 
3. リンクや画像は`[]()`という記法を使う

たとえば以下のように書くと次のスライドができます

    iris とは
    ===============
    iris データの散布図
    ```{r,fig.height=5} 
    plot(cars)
    ```
    [irisについて](http://ja.wikipedia.org/wiki/Iris)



---

## iris とは

iris データの概要と散布図


```r
plot(Sepal.Length ~ Sepal.Width, data = iris)
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 


[irisについて](http://ja.wikipedia.org/wiki/Iris)

---


## 任意の画像を挿入する

自前で用意した画像を挿入するには

    ![画像の説明](img/misaki.png)

という書式を使います

![画像の説明](img/misaki10.png)


<!-- ## コードチャンクそのものを表示させる -->

<!--     iris とは -->
<!--     =============== -->
<!--     iris データの散布図 -->
<!--     ```{r,fig.height=5}  -->
<!--     plot(cars) -->
<!--     ``` -->
<!--     [irisについて](http://ja.wikipedia.org/wiki/Iris) -->


<!-- 
(shell-command "Rscript ~/Dropbox/R/Kyoritsu/IntroStats2/slides/misaki2.R")
-->
