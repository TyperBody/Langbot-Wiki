# WeCom ボットのデプロイ

WeCom（Enterprise WeChat）ボットをデプロイして LangBot に接続します。

:::info
この統合方法は、企業内部アプリケーション用であり、企業内で使用されます。外部カスタマーサービスが必要な場合は、[WeCom Customer Service 統合ソリューション](wecomcs.md)を確認してください。
:::


## ボットの作成

[WeCom Admin Portal](https://work.weixin.qq.com/)に入り、アカウントにログインし、メインページに入った後、「アプリ管理」、「独自の構築」、「アプリを作成」をクリックし、ボットの基本情報を入力します。作成後、次のようなページが表示されます：
![Bot Page](/assets/image/zh/deploy/bots/wecom/wecom/wecom1.png)

## コールバックアドレスの設定

### WeCom 設定項目の取得

1. WeCom Admin Portal ホームページを開き、「私の企業」をクリックし、下部の Enterprise ID を記録します。

![Enterprise ID](/assets/image/zh/deploy/bots/wecom/wecom/wecom2.png)

2. 連絡先同期権限を有効にします

:::info
- この設定項目は、LangBot の一斉送信機能を実装するためのものです。具体的なコードは libs/wecom_api/api.py にあります。
- LangBot はまだ開発中であるため、この設定項目に関連する機能はまだ実装されていません。
- この設定項目はランダムな文字で埋めることができますが、**空にすることはできません**。
:::

![Contact Permission](/assets/image/zh/deploy/bots/wecom/wecom/wecom5.png)

「セキュリティと管理」、「管理ツール」、「連絡先同期」をクリックします

![Contact Sync Secret](/assets/image/zh/deploy/bots/wecom/wecom/wecom3.jpg)

「Secret を表示」をクリックして記録します。これが contacts_secret（連絡先同期 Secret）です。

3. 「アプリ管理」をクリックし、作成したばかりのボットを見つけ、ボットの secret を表示して記録します。

![Bot Secret](/assets/image/zh/deploy/bots/wecom/wecom/wecom4.png)

この時点で、3 つの設定項目を取得しました：corpid（Enterprise ID）、secret（Bot Secret）、contacts_secret（Contact Sync Secret）。

### コールバックアドレスの設定

ボットページに入ります。

下部の「企業信頼 IP」をクリックし、LangBot がデプロイされているサーバーを追加します。

「メッセージを受信」、「API 受信を設定」をクリックし、サーバーメッセージ受信設定を開始します。

LangBot ホームページで、対応するボットを有効にして選択し、設定ページをクリックして入り、Webhook コールバックアドレスをコピーして URL に入力します。

::: info
まず、[HTTP リバースプロキシの設定](/en/workshop/production/proxy-and-ssl)を参照して LangBot コールバックアドレスを設定することをお勧めします。
:::

![Webhook Callback Address](/assets/image/zh/deploy/bots/wecom/wecom/wecom6.png)

Token と EncodingAESKey をランダムに生成するためにクリックし、それらを記録します

## LangBot に接続

![Connect to LangBot](/assets/image/zh/deploy/bots/wecom/wecom/connect_to_langbot.png)

## コールバックアドレスの保存
上記の 5 つの設定項目が正しく取得され、WeCom アダプターに正確に入力されたら、**LangBot を起動します**。

コールバックアドレス設定ページに戻り、保存をクリックします。上記の設定項目が正しく入力されている場合、保存は成功します。これは、WeCom と LangBot が通信できることを意味します（デプロイ成功）。**openapi request callback address failed** が表示された場合は、設定項目が正しく入力されているかどうかを 3 回確認してください。
