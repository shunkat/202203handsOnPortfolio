# デプロイしてみる
Netlifyを使ってデプロイしましょう

ここから先は、\
自分のgithubレポジトリに今回のプロジェクトを保存しないとできないので宿題とします。

(自分のポートフォリオを作成したい人はやってみてください)
以下手順
1. https://github.com/shunkat/portfolioにアクセスして、git cloneする
2. 以下のサイトを参考に自分のレポジトリに追加する(https://qiita.com/S42100254h/items/fcbead402f711c091f8b)
3. 以下のサイトを参考に環境構築をする(https://www.techpit.jp/courses/48/curriculums/51/sections/425/parts/1450)


# Netlifyとgithubを連携する
netlifyの会員登録をしてください。\
その後import new repositoryボタンを押し\
先ほど自分のものとしたレポジトリと連携してみてください。

# 環境変数をnetlifyに入れる
このプロジェクトではセキュリティ的観点で\
APIのキーを.envファイルに隠しています。

.envファイルはgithub上には存在しないので\
.envファイルの代わりをnetlifyに設定してあげなければいけません。

以下手順
1. githubと連携して、作成したレポジトリを選択
2. Build commandは>npm run generate
3. settingsタブからBuild & deploy画面へ
4. スクロールしていくとEnvironment variablesという設定箇所があるので「Edit variables」ボタンを押す
5. Keyとvalueを設定し、saveボタンを押す（忘れないように）

以下はmicroCMSを変更したときに自動でビルドするように設定手順です。

6. NetlifyのBuild & deploy画面からBuild hooksの部分を探してみてください。
7. Build hook nameは適当に決めてsaveボタンを押してください。
8. URLが現れるのでコピーしておいてください。
9. microCMSのAPI設定画面を開いて、Webhookをクリック
10. 追加をクリック
11. Netlifyを選択して、先ほどコピーしてあったURLを入れてください。

これで晴れてサイトの骨組みは完成です。\
お疲れ様でした。

もしわからない箇所や、聞いてみたいことがあればSlackのチャンネルで\
名前(staff)と書いてある人を探して聞いてみてください！

3/22の見せ合い会、楽しみにしております。
