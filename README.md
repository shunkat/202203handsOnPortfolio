# はじめに

### 概要

ポートフォリオをまとめるサイトをJAM STACK構成で作りましょう！

完成イメージ</br>
https://confident-goldwasser-a468fd.netlify.app/

#### ハンズオンのゴール

* Vue.js, Nuxt.js, Vuetifyがちょっとわかる
* Jamstackがちょっとわかる
* モダンな構成のポートフォリオを作り始める第一歩を踏み出せる
  

## 全体の流れ
1. APIを作ってバックエンドの代わりにします。
2. Nuxt.jsを使ってフロントエンドを作ります。
3. フロントエンドとバックエンドをつなげます。
4. （+α）netlifyを使ってデプロイします。

## 事前準備
ハンズオンの中で以下のサービスを利用します。</br>
スムーズに進行するため事前にアカウントの準備をお願いいたします。</br>


<a href="https://github.com/">GitHub</br><img src="/image/octcat.png"></a></br>


おなじみのGitのリモートリポジトリサービスです。基本無料です。</br>
プロジェクトを自分のリソースへFork/Pushするために必要になります。</br>

<p>
※GitHubでは2021年8月13日から<a href="https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/">パスワード認証</a>が廃止されています。</br>
※<a href="https://docs.github.com/ja/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token">トークン</a>を発行し、リポジトリにPushできることを確認しておいてください。
</p></br>

<a href="https://www.gitpod.io/">Gitpod</a></br>
<img src="/image/gitpod.png">
ブラウザ上で仮想環境を立ち上げることのできるサービスです。基本無料です。</br>
ハンズオンでは開発環境を揃えるため、Gitpodに揃えた環境を立ち上げてコマンドやファイルの編集を行います。</br>
GitHubアカウントと連携させる形で登録いただければよいかと思います。</br>

<a href="https://microcms.io/">microCMS</a></br>
<img src="/image/microCMS_logo.png">
和製のヘッドレスCMSサービスです。基本無料です。</br>
今回はバックエンドの代わりのAPIを作成するために使います。</br>





