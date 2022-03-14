# フロントエンドのコードを書く

### 環境構築

gitpodで出来上がった環境を配布します。

gitpod最高！

以下をコピーして、ブラウザのurlにペーストしてください。

> gitpod.io#https://github.com/shunkat/portfolio/tree/handsOnVersion

自動でコマンドが起動し

環境を構築+ローカルサーバーの立ち上げまでやってくれます。

多少時間がかかるので少々おまちください。

#### コラム

veturという拡張機能を使うとコードに色がついて見やすいです。\


gitpodを起動したときに\
自動でインストールするように設定しています。\
このような拡張機能のなかで今回の開発におすすめのものは以下です。\\

* [Material icon thema](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
* [Auto rename tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
* [Auto close tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
* [code runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
* [Vue.peek](https://marketplace.visualstudio.com/items?itemName=dariofuzinato.vue-peek)

興味があれば入れてみてください。\
もしおすすめの拡張機能があれば、教えてください！

### ローカルサーバー起動

さてgitpod起動に成功するとterminal上に\


> ? Are you interested in participating? (Y/n) と表示されます。\
>

匿名化された情報をNuxtの開発体験向上のために\
利用させても良い場合は"Y"を入力。\
嫌な場合は"n"を入力してEnter\


以下のような画面が出れば成功です。\
![](../image/successOpeningLocalServer.png)\


初回は自動でローカルサーバーを立ち上げるようにしましたが\
この次に起動するときは

> yarn dev をターミナルに打ち込んでいます。

### ソースコードを見てみる

左のファイル一覧からpages/index.vueを見つけクリックしてください\
今回の作るサイトのトップページのソースコードがこちらです。\
コードをいじりながら、vue.jsやNuxt.js、Vuetifyの簡単な使い方を学びましょう。\


すごく簡単に全体を説明すると\
今回のコードはフロントエンドを作成するためのもので\
トップページのコードはpages/index.vueに\
各詳細ページはpages/works/\_id/index.vueに存在しています。

![](../image/sourceOutline1st.png)

また今回のコードでは表示したい画像はstaticフォルダー以下においており、\
全ページで共通して使うものはlayouts/default.vueの中に書いてあります。\
![](../image/sourceOutline2nd.png)

さてそろそろ具体的なコードを見ていきましょう。\
全てのコードは見切れないため\
Vue.js、Nuxt.js、Vuetifyの特徴が現れている部分を抽出してみていきます。\\

### Vueの感動ポイント

ソースコードの36行目を見てください。\\

```
<div v-for="i of 3" :key="i" class="eachProduct">
```

という記述で3回のループ処理をしており\
ループ回数をiという変数に格納しています。\\

それを40行目や42行目で呼び出して\
テキストの変更や呼び出す画像を変えるために使用しています。\\

このように、vueでは繰り返し処理を利用して\
コードの記述量を節約できます。\


今回の記述をvueを使わずに書いた場合と比較してみましょう。\\

![](../image/comparisonVueHtml.png)\
同じものを作るのに必要なコードが半分以下に減って\
読みやすくなったのがわかりますね\
また、v-forは後ほどAPIと連携する時に大きな力を発揮します！\\

### Nuxt.jsの感動ポイント

お次はNuxt.jsの感動ポイントを説明します。\\

前のページでNuxt.jsの良いところは\
ウェブアプリに必要な機能をまとめてインストールしてくれること\
と説明しました。\\

その一つに動的ルーティングをしてくれるという点があります。\
(動的ルーティングとは、簡単にいうと\
違うURLでアクセスしても\
一つの雛形のファイルに遷移できる機能です。)

コードの37行目と42行目をみてください。\\

```
<nuxt-link :to="`/works/`">
〜〜〜〜
</nuxt-link>
```

という記述がありますね。\
このnuxt-linkタグで囲った要素をクリックすると\


`:to=`以下に記述した箇所へ遷移します。 今回は/works/と書いているので/pages/works/index.vueに遷移します。

#### Vuetifyの超基本

お次はVue 2行目をみてください。

`<v-row justify="center">`

というコードがありますね。\
こちらのコードは、中の要素を横に配置したい時に使います。\
`<v-row></v-row>` で囲まれた箇所は横の一列として表示されるということです。\
イメージとしては下のような感じです。 ![imageOfVrow](../image/v-row.png)

続いて7行目をみていただくと

`<v-col cols="12" align="center">`

という記述があると思います。\
これは逆に中の要素を縦に配置したい時に使います。\
この二つを合わせると以下のようなイメージです。

![imageOfVrow](../image/v-col.png)

このように要素を配置する時はv-rowとv-colを組み合わせて\
好きな場所に要素を配置してください。

#### コラム ワイヤーフレーム

vuetifyは公式がワイヤーフレームを提供してくれています。 ワイヤーフレームとはデザインの骨組みのことです。\
基本的な構成はワイヤーフレームのコードを利用してサクッと作って\
こだわりたいところに集中できるようにしてくれるというわけですね\


自分で作るときに、大きくデザインを変えたい場合\
ここからコードを拾えないか試してみるのがおすすめです！\
https://vuetifyjs.com/ja/getting-started/wireframes/

### 自己紹介を入力する

それでは自己紹介を自分のものに変更してみてください。
