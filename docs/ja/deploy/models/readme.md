# モデルの設定(Models)

モデルはパイプラインによってメッセージ処理に使用されます。最初に設定したモデルがデフォルトパイプラインのモデルとして設定されます。

![arch](/assets/image/zh/deploy/models/arch.png)

複数のモデルを追加して、パイプラインでどのモデルを使用するかを選択できます。

![モデル設定](/assets/image/zh/deploy/models/model_config.png)

これら4つのパラメータを入力します: `モデル名`、`モデルプロバイダー`、`リクエストURL`、`APIキー`、そして送信します。

モデルの機能については、特定のモデルの特性に応じて選択してください:

- ビジュアル機能: 画像を認識するために有効にする必要があります

- Function Calling: 会話でAgentツールを使用するために有効にする必要があります

:::info

*APIキーをお持ちでない場合は、[このリレーステーションから入手できます](https://api.qhaigc.net/)*

サードパーティのAPIリレーや他のモデルプロバイダーを使用する必要がある場合、

`OpenAI`を選択してください

リクエストURLにリレーのBase URLを入力します。例:

![モデル設定](/assets/image/zh/deploy/models/other_provider.png)

:::
