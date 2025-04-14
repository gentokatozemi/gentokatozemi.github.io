---
layout: page
title: Rによる無料データの入手と利用
description: 無料で公開されている社会科学データをRに読み込むためのガイド（２０２５年４月１４日更新）
img: assets/img/Checklist-bro.png
importance: 1
category: work
giscus_comments: false
---

- [<span class="toc-section-number">1</span> 共通説明](#共通説明)
  - [<span class="toc-section-number">1.1</span> 事前準備](#事前準備)
  - [<span class="toc-section-number">1.2</span>
    データ入手後](#データ入手後)
- [<span class="toc-section-number">2</span>
  東大朝日調査（2003-2024）](#東大朝日調査2003-2024)
  - [<span class="toc-section-number">2.1</span>
    有権者調査](#有権者調査)
    - [<span class="toc-section-number">2.1.1</span>
      2022年参院選（2023年実施）](#2022年参院選2023年実施)
    - [<span class="toc-section-number">2.1.2</span>
      2021年衆院選（2022年実施）](#2021年衆院選2022年実施)
    - [<span class="toc-section-number">2.1.3</span>
      2019年参院選（2020年実施）](#2019年参院選2020年実施)
    - [<span class="toc-section-number">2.1.4</span>
      2017年衆院選](#2017年衆院選)
    - [<span class="toc-section-number">2.1.5</span> 2014年衆院選,
      2016年参院選（2波パネル）](#2014年衆院選-2016年参院選2波パネル)
    - [<span class="toc-section-number">2.1.6</span> 2012年衆院選,
      2013年参院選（2波パネル）](#2012年衆院選-2013年参院選2波パネル)
    - [<span class="toc-section-number">2.1.7</span> 2009年衆院選,
      2010年参院選（2波パネル）](#2009年衆院選-2010年参院選2波パネル)
    - [<span class="toc-section-number">2.1.8</span> 2007年4-5月,
      選挙前, 選挙後（3波パネル)](#2007年4-5月-選挙前-選挙後3波パネル)
    - [<span class="toc-section-number">2.1.9</span> 2003年9月,
      2003年衆院選, 2004年参院選,
      2005年衆院選（4波パネル)](#2003年9月-2003年衆院選-2004年参院選-2005年衆院選4波パネル)
  - [<span class="toc-section-number">2.2</span>
    政治家調査](#政治家調査)
    - [<span class="toc-section-number">2.2.1</span>
      2024年衆院選](#2024年衆院選)
    - [<span class="toc-section-number">2.2.2</span>
      2022年参院選](#2022年参院選)
    - [<span class="toc-section-number">2.2.3</span>
      2021年衆院選](#2021年衆院選)
    - [<span class="toc-section-number">2.2.4</span>
      2019年参院選](#2019年参院選)
    - [<span class="toc-section-number">2.2.5</span>
      2017年衆院選](#2017年衆院選-1)
    - [<span class="toc-section-number">2.2.6</span>
      2016年参院選](#2016年参院選)
    - [<span class="toc-section-number">2.2.7</span>
      2014年衆院選](#2014年衆院選)
    - [<span class="toc-section-number">2.2.8</span>
      2013年参院選](#2013年参院選)
    - [<span class="toc-section-number">2.2.9</span>
      2012年衆院選](#2012年衆院選)
    - [<span class="toc-section-number">2.2.10</span>
      2010年参院選](#2010年参院選)
    - [<span class="toc-section-number">2.2.11</span>
      2009年衆院選](#2009年衆院選)
    - [<span class="toc-section-number">2.2.12</span>
      2007年参院選](#2007年参院選)
    - [<span class="toc-section-number">2.2.13</span>
      2005年衆院選](#2005年衆院選)
    - [<span class="toc-section-number">2.2.14</span>
      2004年参院選](#2004年参院選)
    - [<span class="toc-section-number">2.2.15</span>
      2003年衆院選](#2003年衆院選)
- [<span class="toc-section-number">3</span>
  外交に関する世論調査／外国のイメージと時事問題に関する調査
  (2011-13)](#外交に関する世論調査外国のイメージと時事問題に関する調査-2011-13)
  - [<span class="toc-section-number">3.1</span> Wave
    1-12（2011年10月〜2012年9月）パネル＋フレッシュサンプル](#wave-1-122011年10月2012年9月パネルフレッシュサンプル)
  - [<span class="toc-section-number">3.2</span> Wave
    13-24（2012年10月〜2013年9月）パネル＋フレッシュサンプル](#wave-13-242012年10月2013年9月パネルフレッシュサンプル)
  - [<span class="toc-section-number">3.3</span>
    郵送調査（2012年11月）](#郵送調査2012年11月)
- [<span class="toc-section-number">4</span> 日本版 General Social
  Surveys (JGSS,
  2000-2018)](#日本版-general-social-surveys-jgss-2000-2018)
  - [<span class="toc-section-number">4.1</span>
    質問票の確認](#質問票の確認)
  - [<span class="toc-section-number">4.2</span>
    ダウンロード方法（ICPSRの他のデータも同様）](#ダウンロード方法icpsrの他のデータも同様)
- [<span class="toc-section-number">5</span>
  その他の世論調査](#その他の世論調査)
  - [<span class="toc-section-number">5.1</span>
    世論調査の検索](#世論調査の検索)
  - [<span class="toc-section-number">5.2</span>
    大規模国際比較世論調査（含日本）](#大規模国際比較世論調査含日本)
  - [<span class="toc-section-number">5.3</span>
    地域レベルでの国際比較が可能な世論調査](#地域レベルでの国際比較が可能な世論調査)
- [<span class="toc-section-number">6</span>
  選挙データ（選挙区レベル）](#選挙データ選挙区レベル)
  - [<span class="toc-section-number">6.1</span>
    衆議院議員選挙データ（1947-2018）](#衆議院議員選挙データ1947-2018)
  - [<span class="toc-section-number">6.2</span>
    衆議院議員選挙データ（2021, 2024）](#衆議院議員選挙データ2021-2024)
    - [<span class="toc-section-number">6.2.1</span>
      2024年衆院選データ](#2024年衆院選データ)
    - [<span class="toc-section-number">6.2.2</span>
      2021年衆院選データ](#2021年衆院選データ)
  - [<span class="toc-section-number">6.3</span>
    参議院議員選挙データ](#参議院議員選挙データ)
  - [<span class="toc-section-number">6.4</span>
    その他海外の政治家・選挙関連データ](#その他海外の政治家選挙関連データ)
- [<span class="toc-section-number">7</span>
  比較政治（国・地域レベル）データ](#比較政治国地域レベルデータ)
  - [<span class="toc-section-number">7.1</span> Quality of Government
    (QoG)](#quality-of-government-qog)
  - [<span class="toc-section-number">7.2</span>
    その他の集計レベルデータ](#その他の集計レベルデータ)

# 共通説明

## 事前準備

新しい（もしくはデータ分析に使う既存の）Ｒスクリプトファイル準備し、任意の場所に保存しておきます。

その後、データ保存場所のディレクトリを設定します（必要のないコードは消してください）。

``` r
## Ｒスクリプトファイルと同じ場所にする場合
setwd(setwd(dirname(rstudioapi::getActiveDocumentContext()$path)))

## 自分の好きな場所にする場合
setwd("MY/FAVORITE/FILE/PATH")
```

## データ入手後

データがダウンロードできて、一度読み込みに成功したら、<verb>\##データのダウンロード</verb>項目に含まれるコードはもう使わないのでコメントアウトして、<verb>\##データの読み込み</verb>という項目以下にあるコードだけを使用してください。

# 東大朝日調査（2003-2024）

2003年以降、日本の各国政選挙に対応して行われている有権者と政治家に対する調査です。データとコードブックは[このウェブサイト](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex)から公開されています。データの使用に関して、利用許可申請は不要ですが、以下の項目への同意が必要です。

- 本データの使用は学術目的に限ります。
- 本データを用いた著作物等を公開される場合は「東大谷口研・朝日調査データを使用した」旨を明記してください。また，１部を「〒113-0033
  文京区本郷７-３-１東京大学大学院法学政治学研究科谷口研究室」までお届けください。
- 本データ・コードブック・報告書の著作権は調査者に属します。許可なき再配布及び転載を禁じます。
- 本データは随時更新されます。データのダウンロードや分析に関するサポートは行っておりません。

## 有権者調査

<!-- ### 2024年衆院選（2025年実施） -->

<!-- - [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2024) -->

<!-- - [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2023UTASV_codebook20230501.docx) -->

<!-- - Rを使ったデータ入手方法： -->

<!-- ```{r} -->

<!-- ## データのダウンロード -->

<!-- download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2023UTASV20230416.csv", -->

<!--               "2023UTASV20230416.csv") -->

<!-- ## データの読み込み -->

<!-- library(readr) -->

<!-- dt <- read_csv("2023UTASV20230416.csv") -->

<!-- ## 性別変数（1=男性, 2=女性、99=無回答） -->

<!-- table(dt$Q47) -->

<!-- ``` -->

<!-- ```{r} -->

<!-- #| include: false -->

<!-- file.remove("2023UTASV20230416.csv") -->

<!-- ``` -->

### 2022年参院選（2023年実施）

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2022)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2023UTASV_codebook20230501.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2023UTASV20230416.csv",
              "2023UTASV20230416.csv")

## データの読み込み
library(readr)
dt <- read_csv("2023UTASV20230416.csv")
```

    Rows: 1967 Columns: 59
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (1): Prefecture
    dbl (58): ID, Q1, Q3_1, Q3_2, Q3_3, Q3_4, Q3_5, Q3_6, Q3_7, Q5, Q6, Q7, Q29,...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性、99=無回答）
table(dt$Q47)
```


       1    2   99 
     909 1026   32 

### 2021年衆院選（2022年実施）

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2021)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2022UTASV_codebook20220730.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2022UTASV20220730.csv",
              "2022UTASV20220730.csv")

## データの読み込み
library(readr)
dt <- read_csv("2022UTASV20220730.csv")
```

    Rows: 1892 Columns: 60
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (1): Prefecture
    dbl (59): ID, Scale, Q1, Q3_1, Q3_2, Q3_3, Q3_4, Q3_5, Q3_6, Q3_7, Q6, Q8, Q...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性、99=無回答）
table(dt$Q43)
```


      1   2  99 
    911 965  16 

### 2019年参院選（2020年実施）

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2019)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2020UTASV_codebook20220720.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2020UTASV20210319.csv",
              "2020UTASV20210319.csv")

## データの読み込み
library(readr)
dt <- read_csv("2020UTASV20210319.csv")
```

    Rows: 2053 Columns: 38
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr   (1): ID
    dbl  (36): Term, Scale, Area, PR, Q1, Q3, Q4, Q18, Q20, Q30, Q31, Q32_1, Q32...
    date  (1): Date

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性、99=無回答）
table(dt$Q37)
```


       1    2   99 
     945 1084   24 

### 2017年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2017)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2017UTASV20200326.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2017UTASV20200326.csv",
              "2017UTASV20200326.csv")

## データの読み込み
library(readr)
dt <- read_csv("2017UTASV20200326.csv")
```

    Rows: 1778 Columns: 137
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (14): PREFNAME, CITY, Q2FA, Q4FA, Q5FA, Q6FA, Q8FA, Q13FA, Q18FA, Q19FA...
    dbl (123): ID, PREFEC, HRDIST, Q1, Q2, Q3, Q4, Q5_1, Q5_2, Q5_3, Q6_1, Q6_2,...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性、99=無回答）
table(dt$F1)
```


      1   2  99 
    851 910  17 

### 2014年衆院選, 2016年参院選（2波パネル）

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2014)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2014_2016UTASV_codebook20161004.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2014_2016UTASV20161004.csv",
              "2014_2016UTASV20161004.csv")

## データの読み込み
library(readr)
dt <- read_csv("2014_2016UTASV20161004.csv")
```

    Rows: 1813 Columns: 217
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (19): PREFNAME, CITY, W1Q2FA, W1Q4FA, W1Q5FA, W1Q6FA, W1Q14_2FA, W1Q18F...
    dbl (198): ID, PREFEC, HRDIST, W1Q1, W1Q2, W1Q3, W1Q4, W1Q5_1, W1Q5_2, W1Q5_...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性、99=無回答）
table(dt$W1F1)
```


      1   2  99 
    845 954  14 

### 2012年衆院選, 2013年参院選（2波パネル）

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2012)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2012_2013UTASV_codebook20131129.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2012-2013UTASV131129.csv",
              "2012-2013UTASV131129.csv")

## データの読み込み
library(readr)
dt <- read_csv("2012-2013UTASV131129.csv")
```

    Rows: 1900 Columns: 320
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (15): PREFNAME, CITY, Q0102FA, Q0104FA, Q0106FA, Q0120FA, Q0125FA, Q013...
    dbl (303): ID, PREFEC, HRDIST, Q010100, Q010200, Q010300, Q010400, Q010500, ...
    lgl   (2): Q0119FA, Q0137FA

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$Q014100)
```


      1   2 
    942 958 

### 2009年衆院選, 2010年参院選（2波パネル）

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2009)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2009_2010utas_codebook.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2009_2010utas130816.sav",
              "2009_2010utas130816.sav")

## データの読み込み
library(haven)
dt <- read_sav("2009_2010utas130816.sav")
```

``` r
## 性別変数（1=男性, 2=女性, 9=無回答）
table(dt$Q014600)
```

    Warning: Unknown or uninitialised column: `Q014600`.

    < table of extent 0 >

### 2007年4-5月, 選挙前, 選挙後（3波パネル)

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex#2007)

- コードブック：『日本政治研究』第５巻１・２合併号（ゼミ生の場合は[**このリンク**](https://drive.google.com/file/d/1wlH3v6T84vywpJ4Gho_a7iIDPMn7ezfg/view?usp=drive_link)から限定アクセス）

- Rを使ったデータ入手方法(元ファイルが直接Rで読めないので、限定アクセスのGoogle
  Driveに保存している修正済ファイルを使います)：

``` r
## データのダウンロード
## 初回には、GoogleアカウントとTidyverse Packageの接続許可を求められます。
library(httpuv) 
library(googledrive)
with_drive_quiet(drive_download(as_id("1iDm1-Jy8TCTARugm2rjdeJpF-Fjm3pVx"),overwrite = TRUE))

## データの読み込み
library(readxl)
dt <- read_xlsx("utas080112.xlsx")
```

``` r
## 性別変数（1=男性, 2=女性）
table(dt$Q016600)
```


       1    2 
     944 1125 

### 2003年9月, 2003年衆院選, 2004年参院選, 2005年衆院選（4波パネル)

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex#2003)

- コードブック：『日本政治研究』第２巻１号(1)(2)(3)・第３巻１号(4)（ゼミ生の場合は[**このリンク**](https://docs.google.com/spreadsheets/d/1GG2Pq6-GS5Zu8TbK5QZez3flogts_k1C/edit?usp=drive_link&ouid=104478753151003372725&rtpof=true&sd=true)から簡易版が限定アクセス）

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/utas060104xls.zip", "utas060104xls.zip")
unzip("utas060104xls.zip")
file.remove("utas060104xls.zip")

## データの読み込み
library(readxl)
dt <- read_xls("utas060104.xls")
```

``` r
## 性別変数（1=男性, 0=女性）
table(dt$f010100)
```


       0    1 
    1023  955 

## 政治家調査

### 2024年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2024)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2024UTASP_codebook20241125.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2024UTASP20241125.csv",
              "2024UTASP20241125.csv")

## データの読み込み
library(readr)
dt <- read_csv("2024UTASP20241125.csv")
```

    Rows: 1344 Columns: 122
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr   (6): NAME, KANA, Q1_1_FA, Q1_2_FA, Q1_3_FA, SQ9_17_FA
    dbl (116): ID, RESPONSE, PREFEC, DISTRICT, PR, PRBLOCK, PARTY, INCUMB, TERM,...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$SEX)
```


       1    2 
    1030  314 

### 2022年参院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2022)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2022UTASP_codebook20231201.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2022UTASP20220720.csv",
              "2022UTASP20220720.csv")

## データの読み込み
library(readr)
dt <- read_csv("2022UTASP20220720.csv")
```

    Rows: 668 Columns: 111
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr   (6): NAME, Q10, Q1_1_FA, Q1_2_FA, Q1_3_FA, SQ6_16_FA
    dbl (105): ID, RESPONSE, NOELEC, DISTRICT, PARTY, INCUMB, TERM, SEX, AGE, RE...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性、99=無回答）
table(dt$SEX)
```


      1   2 
    458 210 

### 2021年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2021)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2021UTASP_codebook20211208_temporary.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2021UTASP20211126_excludedQ11.csv",
              "2021UTASP20211126_excludedQ11.csv")

## データの読み込み
library(readr)
dt <- read_csv("2021UTASP20211126_excludedQ11.csv")
```

    Rows: 1051 Columns: 120
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr   (6): NAME, KANA, Q1_1_FA, Q1_2_FA, Q1_3_FA, SQ8_16_FA
    dbl (114): ID, RESPONSE, PREFEC, DISTRICT, PR, PRBLOCK, PARTY, INCUMB, TERM,...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$SEX)
```


      1   2 
    865 186 

### 2019年参院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2019)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2019UTASP_codebook20191109.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2019UTASP20191109.csv",
              "2019UTASP20191109.csv")

## データの読み込み
library(readr)
dt <- read_csv("2019UTASP20191109.csv")
```

    Rows: 491 Columns: 126
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr   (5): NAME, Q1_1_FA, Q1_2_FA, Q1_3_FA, SQ7_16_FA
    dbl (121): ID, RESPONSE, NOELEC, DISTRICT, PARTY, INCUMB, TERM, SEX, AGE, RE...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$SEX)
```


      1   2 
    359 132 

### 2017年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2017)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2017UTASP_codebook20180628.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2017UTASP20180628.csv",
              "2017UTASP20180628.csv")

## データの読み込み
library(readr)
dt <- read_csv("2017UTASP20180628.csv")
```

    Rows: 1180 Columns: 77
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (7): NAME, Q1_1_FA, Q1_2_FA, Q1_3_FA, SQ7_1_1_FA, SQ7_1_2_FA, SQ7_1_3_FA
    dbl (70): ID, RESPONSE, PREFEC, DISTRICT, PR, PRBLOCK, PARTY, MINSHIN, INCUM...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$SEX)
```


      1   2 
    971 209 

### 2016年参院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2016)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2016UTASP_codebook20161010.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2016UTASP20161010.csv",
              "2016UTASP20161010.csv")

## データの読み込み
library(readr)
dt <- read_csv("2016UTASP20161010.csv")
```

    Rows: 510 Columns: 94
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (6): NAME, Q14, Q1_1_FA, Q1_2_FA, Q1_3_FA, Q6_15_FA
    dbl (88): ID, RESPONSE, NOELEC, DISTRICT, PARTY, INCUMB, TERM, SEX, AGE, RES...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$SEX)
```


      1   2 
    392 118 

### 2014年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2014)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2014UTASP_codebook20150910.pdf)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2014UTASP20150910.csv",
              "2014UTASP20150910.csv")

## データの読み込み
library(readr)
dt <- read_csv("2014UTASP20150910.csv")
```

    Rows: 1191 Columns: 82
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (8): NAME, Q1_1FA, Q1_2FA, Q1_3FA, SQ8_1FA, SQ8_2FA, SQ8_3FA, Q15FA
    dbl (74): ID, RESPONSE, PREFEC, DISTRICT, PR, PRBLOCK, INCUMB, TERM, PARTY, ...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性、99=無回答）
table(dt$SEX)
```


      1   2 
    993 198 

### 2013年参院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2013)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2013UTASP_codebook131128.doc)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2013UTASP130722.csv",
              "2013UTASP130722.csv")

## データの読み込み
library(readr)
dt <- read_csv("2013UTASP130722.csv")
```

    Rows: 554 Columns: 95
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (2): NAME, Q16
    dbl (93): ID, RESPONSE, NOELEC, DISTRICT, INCUMB, PARTY, PROP, TERM, SEX, RE...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$SEX)
```


      1   2 
    432 122 

### 2012年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2012)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2012UTASP_codebook20150910.pdf)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2012UTASP20150910.csv",
              "2012UTASP20150910.csv")

## データの読み込み
library(readr)
dt <- read_csv("2012UTASP20150910.csv")
```

    Rows: 1504 Columns: 128
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr   (2): NAME, Q15
    dbl (124): RESPONSE, PREFEC, DISTRICT, PR, PRBLOCK, INCUMB, TERM, PARTY, SEX...
    num   (2): ID, Q14

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性）
table(dt$SEX)
```


       1    2 
    1280  224 

### 2010年参院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2010)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2010ates_codebook101105.docx)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2010ates101105.sav",
              "2010ates101105.sav")

## データの読み込み
library(haven)
dt <- read_sav("2010ates101105.sav")
```

``` r
## 性別変数（1=男性, 2=女性, 9=無回答）
table(dt$SEX)
```


      1   2 
    353 104 

### 2009年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex.html#2009)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2009UTASP_codebook20150910.pdf)

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2009UTASP20150910.csv",
              "2009UTASP20150910.csv")

## データの読み込み
library(readr)
dt <- read_csv("2009UTASP20150910.csv")
```

    Rows: 1374 Columns: 97
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (1): NAME
    dbl (96): ID, oldID, RESPONSE, PREFEC, DISTRICT, PRBLOCK, INCUMB, TERM, PART...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 2=女性, 9=無回答）
table(dt$SEX)
```


       1    2 
    1145  229 

### 2007年参院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex#2007)

- コードブック：『日本政治研究』第５巻１・２合併号（ゼミ生の場合は[**このリンク**](https://docs.google.com/spreadsheets/d/1SU4ChFkOVtkXAY7EoYFTyZdWujgmTeo5/edit?usp=drive_link&ouid=104478753151003372725&rtpof=true&sd=true)から簡易版に限定アクセス）

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2007ates071221.sav",
              "2007ates071221.sav")

## データの読み込み
library(haven)
dt <- read_sav("2007ates071221.sav")
```

``` r
## 候補者名変数（最初の数名）※性別変数なし
head(dt$name)
```

    [1] "伊達忠一" "小川勝也" "畠山和也" "浅野隆雄" "千代信人" "羽柴秀吉"

### 2005年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex#2005)

- コードブック：『日本政治研究』第５巻１・２合併号

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2005ates0801171.csv",
              "2005ates0801171.csv")

## データの読み込み
library(readr)
dt <- read_csv("2005ates0801171.csv", locale = locale(encoding = "CP932"))
```

    Rows: 1131 Columns: 50
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr  (7): familyna, firstnam, 小泉評価理由, 小泉支持理由, 望ましい首相, 消費税率, 改正分野...
    dbl (43): pid, response, sex, age, assassim, blockcod, prefectu, prefdist, p...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 0=女性）
table(dt$sex)
```


      1   2 
    984 147 

### 2004年参院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex#2004)

- [コードブック](https://www.masaki.j.u-tokyo.ac.jp/utas/2004UTASP_Q1-Q9_codebook20220410.docx)（Q10,
  Q11については『日本政治研究』第５巻１・２合併号）

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/2004UTASP20220409.csv",
              "2004UTASP20220409.csv")

## データの読み込み
library(readr)
dt <- read_csv("2004UTASP20220409.csv")
```

    Rows: 482 Columns: 54
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (12): name, policy2, support2, admitype2, pm, nenkin2, nenkinout2, futur...
    dbl (42): id, mode, won, electcod, party, age, sex, incumben, response, poli...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 性別変数（1=男性, 0=女性）
table(dt$sex)
```


      1   2 
    390  92 

### 2003年衆院選

- [調査ページ](https://www.masaki.j.u-tokyo.ac.jp/utas/utasindex#2003)

- コードブック：『日本政治研究』第２巻２号

- Rを使ったデータ入手方法：

``` r
## データのダウンロード
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/ates1v1.csv", 
              "ates1v1.csv") # 衆議院議員調査
download.file("https://www.masaki.j.u-tokyo.ac.jp/utas/ates2v1.csv", 
              "ates2v1.csv") # 衆院選候補者調査

## データの読み込み
library(readr)
dt1 <- read_csv("ates1v1.csv", locale=locale(encoding="CP932"))
dt2 <- read_csv("ates2v1.csv", locale=locale(encoding="CP932"))
```

    Rows: 480 Columns: 29
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (22): name, defense, nuclear, treaty, attack, un, smallgov, woman, lifet...
    dbl  (7): id, wave2id, response, blockcod, prefectu, prefdist, partycod

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
    Rows: 1159 Columns: 42
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (31): name, coalitio, pastkoiz, futureko, elecsys1, elecsys2, appeal, ma...
    dbl (11): id, wave1id, response, blockcod, prefectu, prefdist, partycod, inc...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
## 候補者名変数　※性別変数はなし
head(dt1$name)
```

    [1] "横路孝弘"   "吉川貴盛"   "荒井聡"     "佐藤静雄"   "町村信孝"  
    [6] "佐々木秀典"

``` r
head(dt2$name)
```

    [1] "三品孝行" "横路孝弘" "横山博子" "広坂光則" "石田幸子" "三井辨雄"

# 外交に関する世論調査／外国のイメージと時事問題に関する調査 (2011-13)

河野勝（早稲田大学）を中心とした研究グループによって、２０１１年１０月から２０１３年９月まで毎月、合計２４回行われたオンライン調査（調査会社：日経リサーチ）です。特に、外交や国際関係に関する政治争点に注目し、質問を構成しています。各１２ヶ月続いた２つのパネル・サーベイと、毎月新規にサンプルをとって行われたフレッシュ・サンプルサーベイの２つに分かれています。加えてオンラインサーベイとは別に、2012年11月に実施された郵送調査もあります。以下では、[Harvard
Dataverseにアップロードされているデータ](https://doi.org/10.7910/DVN/LTJEO9)の入手・利用方法を説明します。

- [調査概要](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/LTJEO9#)

## Wave 1-12（2011年10月〜2012年9月）パネル＋フレッシュサンプル

- [コードブック](https://dataverse.harvard.edu/api/access/datafile/4791848)

``` r
## データのダウンロード
# library(remotes)
# remotes::install_github("iqss/dataverse-client-r")
library(dataverse)
dt <- get_dataframe_by_name(
  filename = "sifcct_hdv_wave1-12.tab",
  dataset = "10.7910/DVN/LTJEO9", 
  server = "dataverse.harvard.edu", 
  original = TRUE, .f = readr::read_csv)
saveRDS(dt, "sifcct_hdv_wave1-12.rds")

## データの読み込み
dt <- readRDS("sifcct_hdv_wave1-12.rds")
```

``` r
## 性別変数（1=男性, 2=女性, 3=答えたくない)
table(dt$i38)
```


        1     2     3 
    20610 18675    22 

## Wave 13-24（2012年10月〜2013年9月）パネル＋フレッシュサンプル

- [コードブック](https://dataverse.harvard.edu/api/access/datafile/4791842)

``` r
## データのダウンロード
# library(remotes)
# remotes::install_github("iqss/dataverse-client-r")
library(dataverse)
dt <- get_dataframe_by_name(
  filename = "sifcct_hdv_wave13-24.tab",
  dataset = "10.7910/DVN/LTJEO9", 
  server = "dataverse.harvard.edu", 
  original = TRUE, .f = readr::read_csv)
saveRDS(dt, "sifcct_hdv_wave13-24.rds")

## データの読み込み
dt <- readRDS("sifcct_hdv_wave13-24.rds")
```

``` r
## 性別変数（1=男性, 2=女性, 3=答えたくない)
table(dt$i38)
```


        1     2     3 
    19428 18145   198 

## 郵送調査（2012年11月）

- [コードブック](https://dataverse.harvard.edu/api/access/datafile/4791857)

``` r
## データのダウンロード
# library(remotes)
# remotes::install_github("iqss/dataverse-client-r")
library(dataverse)
dt <- get_dataframe_by_name(
  filename = "sifcct_hdv_mail.tab",
  dataset = "10.7910/DVN/LTJEO9", 
  server = "dataverse.harvard.edu", 
  original = TRUE, .f = readr::read_csv)
saveRDS(dt, "sifcct_hdv_mail.rds")

## データの読み込み
dt <- readRDS("sifcct_hdv_mail.rds")
```

``` r
## 性別変数（1=男性, 2=女性, 3=答えたくない)
table(dt$i38)
```


      1   2   3 
    829 798  34 

# 日本版 General Social Surveys (JGSS, 2000-2018)

アメリカにおけるGeneral Social Surveys
(GSS)とパラレルな調査として、日本で継続して実施されてきている社会学系世論調査です。
多くの政治に関連する質問を含んでいます。様々なチャンネルを通じて、データが公開されていますが、明治大学生であれば、[ICPSRのウェブサイト](https://www.icpsr.umich.edu/web/pages/index.html)でMeijiMailでアカウントを作り、ダウンロードするのが一番効率的だと思います。

## 質問票の確認

[JGSS研究センターの調査概要ページ](https://jgss.daishodai.ac.jp/surveys/sur_question.html)に行くと、これまで行われた、すべてのJGSS調査の質問票が確認できます。データをダウンロードする前にここで自分の関心がある質問が（どの年に）聞かれているかどうかを確認しましょう。

ただし、最新のJGSS調査は、一般公開やICPSRからの提供が行われていません。今、ICPSRで利用可能なデータは以下のものだけであることには注意してください。

- JGSS-2017G/2018G統合データ
- JGSS-2017/2018統合データ
- JGSS-2015
- JGSS-2012
- JGSS-2010
- JGSS-2008
- JGSS-2006
- JGSS-2005
- JGSS累積データ 2000-2003
- JGSS-2003
- JGSS-2002
- JGSS-2001
- JGSS-2000

## ダウンロード方法（ICPSRの他のデータも同様）

1.  まずは、[このページ](https://login.icpsr.umich.edu/realms/icpsr/login-actions/registration)に行って、MeijiMailのアドレスでアカウントを作る。

2.  作ったアカウントを使って、ICPSRのウェブサイトにEmailでログインする。

3.  [JGSSのデータリストのページ](https://www.icpsr.umich.edu/web/ICPSR/series/209)から、好きな年のデータを選んでクリックする。

4.  データ説明ページにある「Download」ボタンをクリックし、**SPSS**形式を選択してクリックする（他の形式でも構いませんが、以下ではSPSS形式を前提として説明します）。

5.  Term of Useが出てくるので、目を通した上で「Agree」をクリックする。

6.  すると、Zipファイルでのダウンロード画面がポップアップするので、「Save
    as…
    名前をつけて保存」をクリックし、R分析用のワーキングディレクトリにダウンロードする。

7.  同じワーキングディレクトリにRスクリプトを作って仮保存し、以下を実行する（以下では、[JGSS2017-2018](https://www.icpsr.umich.edu/web/ICPSR/studies/38163)をダウンロードしたとします）。

``` r
## ダウンロードしたZIPファイルの名前
zipname <- "ICPSR_38163-V1.zip"

## zipファイルを解凍して元ファイルを消す
unzip(zipname, overwrite = TRUE)
invisible(file.remove(zipname))
### DS0001サブフォルダの中に英語のデータおよび質問票など、
### DS0002サブフォルダの中に、日本語の質問票やコードブックが入っている

### データ名＋パスの確認
datadir <- paste0(gsub("\\-.*$","",zipname),"/DS0001/")
dataname <- list.files(datadir)[grep("sav$",list.files(datadir))]
print(paste0(datadir,dataname))

## データの読み込み（上で取得した名前を使う）
library(haven)
dt <- read_sav("ICPSR_38163/DS0001/38163-0001-Data.sav")

## 性別変数（1=男性, 2=女性)
table(dt$SEXA)
```


       1    2 
    1255 1405 

# その他の世論調査

以下に、その他無料で入手可能な世論調査へのリンクを紹介します。国際比較調査が多いですが、日本が含まれているものも多くあります。まずは、リンク先のウェブサイトでCodebook/Questionnaireをチェックし、自分の関心のある質問・時期・対象国がカバーされているかチェックしてください。データの入手方法について、需要が高まれば随時アップデートします。

## 世論調査の検索

- [**Social Science Japan
  Archive（SSJDA）**](https://ssjda.iss.u-tokyo.ac.jp/Direct/datasearch.php).
  日本における多種多様な世論調査データが寄託されているデータ・アーカイヴです。非常に幅広いデータがあり、どれも無料で入手できますが、学部生の使用が制限されていたり、使用申請をしてから使用できるまでに時間がかかったりします。検索をしてみて、どう
  しても関心があるデータがある場合は、私まで教えてください。

- [**Inter-university Consortium for Political and Social
  Research（ICPSR）**](https://www.icpsr.umich.edu/web/pages/index.html).
  JGSSの入手方法ですでに紹介しましたが、こちらも多種多様なデータが寄託されているデータアーカイヴで、アメリカ発のサイトですが、日本のデータも多くあります。説明したとおり、明治大学は会員ですので、MeijiMailでアカウントを作れば、無料でデータをダウンロードできます。

- [GESIS](https://search.gesis.org/?source=%7B%22query%22%3A%7B%22bool%22%3A%7B%22must%22%3A%7B%22match_all%22%3A%7B%7D%7D%2C%22filter%22%3A%5B%7B%22term%22%3A%7B%22type%22%3A%22research_data%22%7D%7D%5D%7D%7D%7D).
  社会科学系のデータを集積している、ドイツ発のウェブサイトです。ここも大量のデータを検索できるので、興味のあるトピックを入力して探してみるといいでしょう。特にヨーロッパのデータが充実しています。

## 大規模国際比較世論調査（含日本）

- [**世界価値観調査 (World Values Survey:
  WVS)**](https://www.worldvaluessurvey.org/wvs.jsp).　社会・政治的な価値観に関する多くの設問を含む、古典的な国際比較世論調査で、日本も昔から参加しています。国レベルのデータは、ウェブサイトの
  “Data & Documentation” -\> “Data Download” -\> “Wave X”.
  から、Excel,SPSS,STATA形式のデータがダウンロードできます。ただし、最新データはデータを開く際にエラーが出るという話もあるので、もしトラブルがあった場合は連絡してください。
- [**International Social Survey Programme (ISSP) **](https://issp.org).
  国際的に共通の質問を含めて行われている社会学系世論調査で、日本もJGSSで参加しています。各年によって特定のテーマの質問を含めて行われることが特徴です
  “Data Download”項目から、STATAとSPSS形式でデータが入手できます。
- [**Comparative Study of Electoral Systems (CSES)
  **](https://cses.org).
  様々な国での選挙時世論調査の結果を含めた国際共同プロジェクトです。日本も参加しています。“Download
  Data”項目から、SPSS, Stata, CSV形式でデータがダウンロードできます。
- [**Global Barometer Surveys（GBS)**](https://www.globalbarometer.net).
  下の項目で触れている、LatinoBarometro、Afrobarometer, Asian Barometer,
  Arab Barometer, Eurasia
  Barometerの各研究グループが協力して、これらのサーベイ間で共通した、もしくは近い内容の設問を集めて一つのデータにしたサーベイです。他の調査ではあまり対象になっていないような国が多く入っているのが特徴です。

## 地域レベルでの国際比較が可能な世論調査

**Social Surveys**

- （アメリカ）[General Social Survey (GSS)](https://gss.norc.org).
  JGSSの元になっているアメリカの世論調査です。
- （ヨーロッパ）[European Social Survey
  (ESS)](https://www.europeansocialsurvey.org).　同じくJGSSのヨーロッパ版だと思ってください。
- （東アジア）[East Asian Social Survey (EASS)](https://www.eassda.org).
  JGSSも参加している、東アジアで共通の設問を含める試みです。[**ICPSRからデータを入手**](https://www.icpsr.umich.edu/web/ICPSR/series/486)できます。

**Barometer Surveys**

- （アフリカ)[Afrobarometer](https://www.afrobarometer.org).  
- （中東・北アフリカ）[Arab Barometer](https://www.arabbarometer.org)
- （アジア・含日本）[Asian Barometer](http://www.asianbarometer.org).
- （東南アジア）[AsiaBarometer](https://www.icpsr.umich.edu/web/ICPSR/search/studies?q=AsiaBarometer).　※ウェブサイトはありませんが、ICPSRからダウンロードできます。
- （中央アジア）[Central Asia
  Barometer](https://www.ca-barometer.org/en).
- （中央アジア・コーカサス）[Eurasia
  Baromter](https://office.eurasiabarometer.org/projects/eurasia-barometer).
  ※データはGlobal Barometer
  Surveysを通じてしか公開されていないようです。
- （コーカサス）[Caucasus Barometer](https://caucasusbarometer.org/en/).
- （ヨーロッパ）[Eurobarometer](https://europa.eu/eurobarometer/screen/home).
  ※利用前に申請が必要です。
- （南アメリカ）[Latinobarometro](https://www.latinobarometro.org/lat.jsp).
- （南北アメリカ大陸）[Americas Barometer
  (LAPOP)](https://www.vanderbilt.edu/lapop/).

**アメリカ**

- [American National Election Studies
  (ANES)](https://electionstudies.org).
  アメリカではもっとも有名で、最も長く続いている選挙時世論調査です（対面式）
- [Cooperative Election Study (CES)](https://cces.gov.harvard.edu).
  回答者数などから、最も大規模な世論調査の一つです。オンラインで行われています。

**イギリス**

- [British Election Study (BES)](https://www.britishelectionstudy.com).

# 選挙データ（選挙区レベル）

## 衆議院議員選挙データ（1947-2018）

[The Reed-Smith Japanese House of Representatives Elections
Dataset](https://doi.org/10.7910/DVN/QFEPXD)は、1947年〜2018年までのすべての衆議院議員選挙における候補者と選挙結果をまとめたデータです。東大朝日調査の候補者レベルデータと合わせて使うこともできるはずです。Harvard
Dataverseから入手できます。

- [コードブック（英語）](https://dataverse.harvard.edu/api/access/datafile/:persistentId?persistentId=doi:10.7910/DVN/QFEPXD/IZNSJH)

- Rによるデータ入手方法：

``` r
## データのダウンロード
# library(remotes)
# remotes::install_github("iqss/dataverse-client-r")
library(dataverse)
dt <- get_dataframe_by_name(
  filename = "Reed-Smith-JHRED-CANDIDATES.dta",
  dataset = "10.7910/DVN/QFEPXD", 
  server = "dataverse.harvard.edu", 
  original = TRUE, .f = haven::read_dta)
saveRDS(dt, "Reed-Smith-JHRED-CANDIDATES.rds")

## データの読み込み
dt <- readRDS("Reed-Smith-JHRED-CANDIDATES.rds")
```

``` r
## 候補者名変数（性別変数はなし）
head(dt$name_jp)
```

    [1] "がくし勇三郎"       "ガッツ石松"         "さとうふみや"      
    [4] "ツルネン・マルテイ" "トクマ"             "ト部政巳"          

## 衆議院議員選挙データ（2021, 2024）

Reed-Smithデータに含まれていない2021年と2024年の衆議院議員選挙データに関しては、[高知工科大学の矢内勇生先生のウェブサイト](https://yukiyanai.github.io/jp/resources/)に公開されているものが便利です。

### 2024年衆院選データ

- [コードブック](https://yukiyanai.github.io/jp/resources/data/hr2024election.html)

``` r
## 小選挙区データのダウンロード
download.file("https://yukiyanai.github.io/jp/resources/data/hr2024_districts.csv", "hr2024_districts.csv")

## 小選挙区データの読み込み
library(readr)
dt <- read_csv("hr2024_districts.csv")

## 候補者名変数（性別変数はなし）
head(dt$name)
```

    Rows: 1113 Columns: 19
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (11): prefecture, district, name, yomi, lastname, firstname, last_kana, ...
    dbl  (8): dist_no, age, previous, duplicate, win_smd, win_pr, votes, vshare

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    [1] "小林 悟"   "道下 大樹" "田中 義人" "千葉 尚子" "加藤 貴弘" "山崎 泉"  

``` r
## 比例区（候補者別）データのダウンロード
download.file("https://yukiyanai.github.io/jp/resources/data/hr2024_pr_candidates.csv", "hr2024_pr_candidates.csv")

## 比例区（候補者別）データの読み込み
library(readr)
dt <- read_csv("hr2024_pr_candidates.csv")

## 候補者名変数（性別変数はなし）
head(dt$name)
```

    Rows: 881 Columns: 18
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (11): block, party, name, yomi, lastname, firstname, last_kana, first_ka...
    dbl  (7): rank, age, previous, dup, win_smd, win_pr, loss_ratio

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    [1] "小林 悟"   "山崎 泉"   "鳥越 良孝" "喜多 義典" "伊東 良孝" "加藤 貴弘"

``` r
## 比例区（政党別）データのダウンロード
download.file("https://yukiyanai.github.io/jp/resources/data/hr2024_pr_parties.csv", "hr2024_pr_parties.csv")

## 比例区（政党別）データの読み込み
library(readr)
dt <- read_csv("hr2024_pr_parties.csv")

## 政党名変数
head(dt$party)
```

    Rows: 107 Columns: 7
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (2): block, party
    dbl (5): n_cand, pr_wins, smd_wins, votes, vshare

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    [1] "れいわ新選組" "公明党"       "参政党"       "国民民主党"   "日本共産党"  
    [6] "日本維新の会"

### 2021年衆院選データ

- [コードブック](https://yukiyanai.github.io/jp/resources/data/hr2021election.html)

``` r
## 小選挙区データのダウンロード
download.file("https://yukiyanai.github.io/jp/resources/data/hr2021_districts.csv", "hr2021_districts.csv")

## 小選挙区データの読み込み
library(readr)
dt <- read_csv("hr2021_districts.csv")

## 候補者名変数（性別変数はなし）
head(dt$name)
```

    Rows: 857 Columns: 19
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (11): prefecture, district, name, yomi, lastname, firstname, last_kana, ...
    dbl  (8): dist_no, age, previous, duplicate, win_smd, win_pr, votes, vshare

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    [1] "小林 悟"   "道下 大樹" "船橋 利実" "高橋 祐介" "松木 謙公" "山崎 泉"  

``` r
## 比例区（候補者別）データのダウンロード
download.file("https://yukiyanai.github.io/jp/resources/data/hr2021_pr_candidates.csv", "hr2021_pr_candidates.csv")

## 比例区（候補者別）データの読み込み
library(readr)
dt <- read_csv("hr2021_pr_candidates.csv")

## 候補者名変数（性別変数はなし）
head(dt$name)
```

    Rows: 818 Columns: 17
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (11): block, party, name, yomi, lastname, firstname, last_kana, first_ka...
    dbl  (6): rank, age, previous, win_smd, win_pr, loss_ratio

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    [1] "豊巻 絹子" "佐藤 英道" "荒瀬 正昭" "道下 大樹" "松木 謙公" "荒井 優"  

``` r
## 比例区（政党別）データのダウンロード
download.file("https://yukiyanai.github.io/jp/resources/data/hr2021_pr_parties.csv", "hr2021_pr_parties.csv")

## 比例区（政党別）データの読み込み
library(readr)
dt <- read_csv("hr2021_pr_parties.csv")

## 政党名変数
head(dt$party)
```

    Rows: 103 Columns: 7
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (2): block, party
    dbl (5): n_cand, pr_wins, smd_wins, votes, vshare

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    [1] "ＮＨＫと裁判してる党弁護士法７２条違反で"
    [2] "れいわ新選組"                            
    [3] "公明党"                                  
    [4] "国民民主党"                              
    [5] "日本共産党"                              
    [6] "日本維新の会"                            

## 参議院議員選挙データ

参議院議員選挙については、あまり詳しく説明しませんが、以下のサイトが利用できるでしょう。

- [高知工科大学の矢内勇生先生のウェブサイト](https://yukiyanai.github.io/jp/resources/)にある、2022年参院選のデータ。

- [参議院議員通常選挙データベース（参議院DB）](http://db.cps.kutc.kansai-u.ac.jp)：参議院議員通常選挙の市区町村別データを格納したデータベースなので、詳細な分析ができます。ただし、カバーされる年次は1968年〜2013年です。

## その他海外の政治家・選挙関連データ

（必要に応じて入手方法をアップデートします）

- （アメリカの選挙結果）[Election Return Data from
  MIT](https://electionlab.mit.edu/data). Different election return data
  that are publicly available through people at MIT.
- （アメリカの選挙資金）[Database on Ideology, Money in Politics, and
  Elections (DIME)](https://data.stanford.edu/dime). One of the most
  comprehensive datasets on campaign contributions.  
- （アメリカの議会行動）[Legislative Effectiveness
  Data](https://thelawmakers.org/data-download). About law-making
  process of legislators.
- （イギリスの選挙結果）[BRITISH GENERAL ELECTION CONSTITUENCY
  RESULTS](https://www.pippanorris.com/data). Other datasets are also
  available from this page.
- （政党公約の国際比較）[Comparative Manifesto
  Project](https://manifesto-project.wzb.eu). Coding Party Ideologies by
  manifests.
- （政党イデオロギー位置の国際比較）[Chapel Hill Expert
  Survey](https://www.chesdata.eu). Coding Party Ideologies by expert
  survey.

# 比較政治（国・地域レベル）データ

## Quality of Government (QoG)

[QoG](https://www.gu.se/en/quality-government)は、国レベルで計測されるあらゆる政治に関わる変数を集めた国際比較データです。2025年1月時点での現状を比較するCross-Sectionデータと、年次ごとのパネルデータであるTime-Series
Dataの2種類があります。厳密な分析にはTime-Seriesデータが必須ですが、簡易的にパターンを見たい場合は、Cross-Sectionデータを利用すると良いでしょう。

- [データの概要ページ](https://www.gu.se/en/quality-government/qog-data/data-downloads/standard-dataset)

- [コードブック（2025年1月）](https://www.qogdata.pol.gu.se/data/codebook_std_jan25.pdf)

- Cross-Sectionデータの入手と利用

``` r
## Cross-Section データのダウンロード
download.file("https://www.qogdata.pol.gu.se/data/qog_std_cs_jan25.sav","qog_std_cs_jan25.sav")

## データの読み込み
library(haven)
dt <- read_sav("qog_std_cs_jan25.sav")

## 国名変数
head(dt$cname)
```

    [1] "Afghanistan"         "Albania"             "Algeria"            
    [4] "Andorra"             "Angola"              "Antigua and Barbuda"

- Time-Seriesデータの入手と利用

``` r
## Time-Series データのダウンロード
download.file("https://www.qogdata.pol.gu.se/data/qog_std_ts_jan25.sav","qog_std_ts_jan25.sav")

## データの読み込み
library(haven)
dt <- read_sav("qog_std_ts_jan25.sav")

## 国名変数
head(dt$cname) # パネルなので同じ国名が並ぶ
```

    [1] "Afghanistan" "Afghanistan" "Afghanistan" "Afghanistan" "Afghanistan"
    [6] "Afghanistan"

## その他の集計レベルデータ

（必要に応じて入手方法をアップデートします）

- （民主主義の要素・指標）[Varieties of Democracy
  (V-Dem)](https://www.v-dem.net). Lots of indicators of democracy.

- （戦争・武力紛争）[Correlates of War
  Project](https://correlatesofwar.org). Datasets of war and smaller
  inter-state disputes. Country-year-dyad level dataset is useful.

- （暴動・暴力とデモ）[The Armed Conflict Location & Event Data Project
  (ACLED)](https://acleddata.com). Event level data on violence and
  protests.

- (暴動・デモ、時事) [A Global Database of
  Society（GDELT）](https://www.gdeltproject.org)

- （アメリカの州レベルの政策比較）[The Correlates of State
  Policy](http://ippsr.msu.edu/public-policy/correlates-state-policy).
  US State level datasets on different policies and state
  characteristics.

<!-- # 外交・紛争／戦争データ（peacesciencer) -->

<!-- [peacesciencer](https://svmiller.com/peacesciencer/ms.html)は、[Correlates of War]() -->
