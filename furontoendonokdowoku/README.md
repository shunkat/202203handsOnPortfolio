# フロントエンドを作ってみる
この章ではフロントエンドのコードを作りながら\
先ほど紹介した三つの技術の感動ポイントを説明していきます。

しかしその前に環境構築をしましょう！
### 環境構築

gitpodで出来上がった環境を配布します。\
gitpod最高！

以下をコピーして、ブラウザのurlにペーストしてください。

> gitpod.io#https://github.com/shunkat/portfolio/tree/handsOnVersion

自動でコマンドが起動し

環境を構築+ローカルサーバーの立ち上げまでやってくれます。

多少時間がかかるので少々おまちください。

#### コラム

veturという拡張機能を使うとコードに色がついて見やすいです。


gitpodを起動したときに\
自動でインストールするように設定しています。\
このような拡張機能のなかで今回の開発におすすめのものは以下です。

* [Material icon thema](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
* [Auto rename tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
* [Auto close tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
* [code runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
* [Vue.peek](https://marketplace.visualstudio.com/items?itemName=dariofuzinato.vue-peek)

興味があれば入れてみてください。\
もしおすすめの拡張機能があれば、教えてください！

### ローカルサーバー起動

さてgitpod起動に成功するとterminal上に


> ? Are you interested in participating? (Y/n) と表示されます。
>

匿名化された情報をNuxtの開発体験向上のために\
利用させても良い場合は"Y"を入力。\
嫌な場合は"n"を入力してEnter

しばらく待って\
以下のような画面が出れば成功です。\
![](../image/successOpeningLocalServer.png)

terminal上で
>http://localhost:3000/
と表示されている部分をcmd+clickしてサイトを見てみましょう。


これ以降、コードに変更を加えることがありますが\
一部の例外以外、変更を勝手に反映してくれます。

今後この資料で「サイトを見てください」と書いてあったら\
サイトを開いたタブを見に行くという意味です。\
なので一度開いたタブを消さないようにしておいてください！

もし、何か問題が起こったら\
ターミナル上でcmd+c(ctrl+c)を打ち込んで、サーバーを停止し\
>yarn dev
で再起動してもらうかもしれません。

### ソースコードを見てみる

まず簡単に全体を説明すると\
今回のコードはフロントエンドを作成するためのもので\
トップページのコードはpages/index.vueに\
各詳細ページはpages/works/\_id/index.vueに存在しています。

![](../image/sourceOutline1st.png)

また表示したい画像はstaticフォルダー以下においており、\
全ページで共通して使うデザイン部分（ヘッダーやフッターはlayouts/default.vueの中に書いてあります。

![](../image/sourceOutline2nd.png)

さてそろそろ具体的なコードを見ていきましょう。\
全てのコードは見切れないため\
Vue.js、Nuxt.js、Vuetifyの特徴が現れている部分を抽出してみていきます。


