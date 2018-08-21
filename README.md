# hello-php-app

## Info
* Heroku Simple Tutorial
* 超初歩的な Heroku x php

## Basic Component
```
.
|-- .gitignore
|-- Procfile        # heroku app 処理管理ファイル
|-- app.json        # heroku app パッケージ管理ファイル
|-- composer.json   # php パッケージ管理ファイル, 構成管理用
|-- composer.lock   # php パッケージ管理ファイル, 最新バージョンの保持用
|-- vendor          # 外部スクリプト用ディレクトリ, composer で管理
|   |-- composer
|   |   |-- LICENSE
|   |   |-- installed.json
|   |   |-- autoload_classmap.php
|   |   |-- ...
|   |   `-- ClassLoader.php
|   `-- autoload.php
|-- index.php       # main script
`-- README.md       # this
```

## How to startup?
1. `composer`で使用する php のバージョンを指定

    ```bash
    $ composer require php:~7
    ```

2. `.gitignore`を作成，`vendor/`を追加

    ```bash
    $ echo "vendor/" > .gitignore
    ```

3. git リポジトリと heroku app を作成，リモートに push する

    ```bash
    $ git init
    $ git add . && git commit -m "[$MESSAGE]"
    $ heroku app create [$APP_NAME]
    $ git push heroku master
    ```

4. `curl`および`heroku open`で heroku app を確認

    ```bash
    $ curl https://[$APP_NAME].herokuapp.com
    $ heroku open
    ```


------

## Ref
* PHP アプリをクラウドにデプロイ・運用・スケール - Heroku, [https://jp.heroku.com/php](https://jp.heroku.com/php)