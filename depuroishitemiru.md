# デプロイしてみる
Netlifyを使ってデプロイする
ここから先は、自分のgithubレポジトリに
今回のプロジェクトを保存しないとできないので
宿題とします。
(自分のポートフォリオを作成したい人はやってみてください)
以下手順


# Netlifyとgithubを連携する
netlifyの会員登録をしてください。
その後
import new repositoryボタンを押し
githubのレポジトリと連携してみてください。

# 環境変数をnetlifyに入れる
このプロジェクトではセキュリティ的観点で
APIのキーを.envファイルに隠しています。
.envファイルはgithub上には存在しないので
.envファイルの代わりをnetlifyに設定してあげなければいけません。

以下手順
1. githubと連携して、作成したレポジトリを選択
2. Build commandは>npm run generate
3. settingsタブからBuild & deploy画面へ
4. スクロールしていくとEnvironment variablesという設定箇所があるので「Edit variables」ボタンを押す
5. Keyとvalueを設定し、saveボタンを押す（忘れないように）
microCMSを変更したときに自動でビルドするように設定します。
6. Build hooks
