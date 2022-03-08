# APIと連携するためのキーを記述する
プロジェクトのルートに.envという名前のファイルを作ってそこに

```
GET_API_KEY=[あなたのAPIキー]
SERVICE_DOMAIN=[あなたのmicroCMSドメイン]
```
というコードを書いてください。
あなたのAPIキーの見方は
microCMSのページに行き
以下の画像の矢印部分を押してください。
![howToFindYourAPIKey](image/howToFindYourAPIKey.png "howToFindYourAPIKey")
<img src="image/howToFindYourAPIKey.png">
        
# コードを変更する
1. データ取得
/pages/index.vueの73行目から83行目までをコメントアウト解除してください。</br>
このコードで先ほど作成したAPIからデータを取得して</br>
productsという変数の中に格納してくれます。

2. データ反映
次に、34行目から45行目までをコメントアウトし、</br>
48行目から62行目までをコメントアウト解除してください。</br>
この部分でproductsという変数を使ってview要素を更新しています。

以上で今回のハンズオンは終了です。
