## 環境構築
gitpodで出来上がった環境を配布します。

gitpod最高！

以下をコピーして、ブラウザのurlにペーストしてください。
>gitpod.io#https://github.com/shunkat/portfolio

自動でコマンドが起動し

環境を構築+ローカルサーバーの立ち上げまでやってくれます。

多少時間がかかるので少々おまちください。

### コラム
veturという拡張機能を使うとコードに色がついて見やすいです。

gitpodを起動したときに
下におすすめとして出すようにしているので

気になったらinstallしてみてください。

起動に成功するとterminal上に
>? Are you interested in participating? (Y/n) 
と表示されます。

匿名化された情報をNuxtの開発体験向上のために
利用させても良い場合は"Y"を入力。
嫌な場合は"n"を入力してEnter

以下のような画面が出れば成功です。
<img src="/image/successOpeningLocalServer.png">


## pages/works/_id/index.vue
_をつかうことで動的に表示できます。



## APIのキーとサブドメインを設定します
プロジェクトのルート下に.envというファイルがあるので

そのファイルの中身を以下のように書き換えてください。