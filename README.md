# Database API

## 設定

1. `.env`ファイルを作成し、下記内容をコピーする
2. `APP_NAME`を指定する
3. 本番環境であれば`compose.yml`の`GRAPHILE_EXTRA_OPTIONS_DEV`を`GRAPHILE_EXTRA_OPTIONS_PRODUCTION`に切り替える
4. Postgresqlのユーザー、パスワードを任意の文字列に変更する
5. `postgres/init`以下に作成するテーブルのDDLやテーブル作成後に必要なデータを配置する

```env
APP_NAME="example-db-api"
POSTGRES_USER="postgres"
POSTGRES_PASSWORD="postgres-passsword"
POSTGRES_DB="example-db"
GRAPHILE_EXTRA_OPTIONS_DEV="--enhance-graphiql"
GRAPHILE_EXTRA_OPTIONS_PRODUCTION="--disable-query-log"
```

## 起動

```sh
docker compose up
```

## 停止

```sh
docker compose down
```

## 抹消

```sh
docker container rm コンテナ名
docker volume rm ボリューム名
```

以上
