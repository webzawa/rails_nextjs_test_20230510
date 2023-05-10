# 初回の起動方法

## image の取得と構築

```
$ docker-compose build
```

## 起動

```
$ docker-compose up
```

## database のテーブル作成

```
$ docker-compose run api rails db:create
$ docker-compose run api rails db:migrate
```
