# Database API

## 設定

1. `APP_NAME`を指定する
2. 本番環境であれば`compose.yml`の`GRAPHILE_EXTRA_OPTIONS_DEV`を`GRAPHILE_EXTRA_OPTIONS_PRODUCTION`に切り替える
3. Postgresqlのユーザー、パスワードを任意の文字列に変更する

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
