# ローカル開発用MySQL

## 概要

ローカル開発で使用してMySQLサーバを立てたい場合に、Dockerで簡単にMySQLサーバを起動する方法です。
また、データをローカルのストレージに永続化します。

## 手順

1. MySQLの使用するDockerイメージの取得

  `docker pull mysql:<version>`

2. docker-compose.ymlの編集

  サンプルのdocker-compose.ymlの編集

  |項目|内容|
  |:---|:--|
  |version|1.で取得したMySQLのバージョン|
  |local_storage|データを保存するローカルパス|
  |passwrod|ルートパスワード|
  |database|データベース名|

3. 起動

  `docker-compose up -d`

4. 停止

  `docker-compose stop`
