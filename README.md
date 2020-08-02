# fukuoka-de-longi-bot-prepare
## 概要
- CDを行うために必要なリソースについて作成を行っている
- CDのためのリソース作成をしているので、これそのもののCDはない
- `make create-sam-deploy-user-access-key` で `fukuoka-de-longi-bot-cloud` と `fukuoka-de-longi-bot-layer` 用のIAM Userのアクセスキーを発行している
    - 発行している場合は削除して再発行。
- `make create-ssm-deploy-user-access-key` で `fukuoka-de-longi-bot-ssm` 用のIAM Userのアクセスキーを発行している
    - 発行している場合は削除して再発行。

## 使い方
- 必要なもの
    - `python`: `3.6`以上。
    - `poetry`: `0.12`以上。 Pythonのパッケージ管理に利用しています。
- 使い方
    1. `poetry install`
    1. 環境変数にAWSのクレデンシャルやリージョンを設定
    1. `make deploy`