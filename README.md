# はじめに

### 概要

ポートフォリオをまとめるサイトをJam stack構成で作りましょう！


[完成イメージ](https://confident-goldwasser-a468fd.netlify.app/)

#### ハンズオンのゴール
* Vue.js, Nuxt.jsがちょっとわかる
* Jamstackの便利さが少し伝わる
* ポートフォリオサイトが手に入る
  

## 全体の流れ
1. APIを作ってバックエンドの代わりにします。
2. Nuxt.jsを使ってフロントエンドを作ります。
3. フロントエンドとバックエンドをつなげます。
4. （+α）netlifyを使ってデプロイします。

## 事前準備

ハンズオンの中で以下のサービスを利用します。\
スムーズに進行するため事前にアカウントの準備をお願いいたします。


[GitHub](https://github.com)\
![](image/octcat.png)

おなじみのGitのリモートリポジトリサービスです。基本無料です。\
プロジェクトを自分のリソースへFork/Pushするために必要になります。

[Gitpod](https://www.gitpod.io)\
![](image/gitpod.png)&#x20;

ブラウザ上で仮想環境を立ち上げることのできるサービスです。基本無料です。\
ハンズオンでは開発環境を揃えるため、Gitpodに揃えた環境を立ち上げてコマンドやファイルの編集を行います。\
GitHubアカウントと連携させる形で登録いただければよいかと思います。

[microCMS](https://microcms.io)\
![](image/microCMS\_logo.png)\
和製のヘッドレスCMSサービスです。基本無料です。\
今回はバックエンドの代わりのAPIを作成するために使います。\
アカウントの作成とサービス登録まで進んでください（やり方は以下です。）

サービスを登録方法

1. サービス名を自由に決定し(例：portfolio)
2. サービスIDを誰ともかぶらないように設定してください（例：portfolio-shunk)
3. 「サービス登録が完了しました」と出れば成功です。表示されているURLにアクセスしてください。


