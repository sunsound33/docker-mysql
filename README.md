# DockerのMySQLコンテナで日本語が使いたい！
docker-mysqlのディレクトリ内に移動してください。
env.exampleファイルをコピーします。<br>
コピーした`.env`ファイルにお好みの環境を設定してください。<br>
```
 cp .env.example .env
```
mysqlディレクトリ内に使いたいsqlファイルを入れる(サンプルでprefecture.sqlが入っているのでファイルを差し替えてください。)<br>
Dockerをビルドしてコンテナを立ち上げる。
```
dokcer-compose build
docker-compose up -d
```
dbコンテナに入る。
```
docker-compose exec db bash
```
コンテナ内でMySQLにログイン
```
mysql -u$MYSQL_USER -p$MYSQL_PASSWORD
```
これで自由にMySQLで日本語が使える！
