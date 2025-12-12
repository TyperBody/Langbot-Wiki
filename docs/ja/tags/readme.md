# Service API 概要

LangBotは、外部サービスと統合するための一連のAPIを提供します。これらのAPIはAPIキーで認証され、HTTP APIのサブセットです。フロントエンドとバックエンドの通信用APIドキュメントを表示するには、[開発](/en/develop/dev-config)セクションにアクセスしてください。

::: warning
Service APIは現在ベータ版であり、一部のAPIは頻繁に変更される可能性があります。
:::

## APIキーの取得

WebUIのサイドバーにある`API Keys`ボタンをクリックして、APIキーを作成します。

![create_api_key](/assets/image/zh/api/create_api_key.png)

作成後、APIキーをコピーして保存します。

![copy_api_key](/assets/image/zh/api/copy_api_key.png)

## APIの使用

左サイドバーには、利用可能なすべてのAPIが一覧表示されています。インスタンスアドレス(バックエンドが公開するポートアドレス、デフォルトは`http://localhost:5300`)とAPIキーを入力し、`Try it out`ボタンをクリックしてAPIを呼び出すことができます。
