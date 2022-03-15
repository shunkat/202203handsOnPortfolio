# APIを作ってみる

今回はmicroCMSというサービスを使って</br>
自分の成果物を返してくれるAPIを作ってみます。

## microCMSとは

日本製のヘッドレスCMSです。\
[microCMS](https://microcms.io)\
![](image/microCMS\_logo.png)\
ヘッドレスCMSとは、一般的なCMS(Wordpressなど)から\
見た目(View)の部分の管理を取り除いたものです。

要は、コードを書かずに\
便利な管理画面から操作するだけで\
簡単にバックエンドAPIを作成できるというサービスです。


## 作ってみよう
一旦加藤がお手本をやってみるので、みながらついてきてください。
1. [microCMS](https://microcms.io)のページに行きます

2. APIを作成します
   1. api名はcontents
   2. エンドポイントもcontentsと入力して「次へ」

![](image/endpoints.png)

   3. リスト形式を選択して「次へ」
   4. slackにおいたファイルをインポートして「完了」

![](image/importJson.png)

3. APIで返す情報を入力します。\
ご自身の成果物の情報を入力してください。\
もしなければ想像でつくってみてください
   1. 右上の「＋追加」ボタン
   2. それぞれの欄を埋めて右上の「公開」ボタン

1. 以下の画像のような画面になれば成功です！

それでは制限時間5分でやってみてください！

![](image/APIgenerated.png)
