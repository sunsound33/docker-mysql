# DockerのMySQLコンテナでも日本語が使いたい！
docker-mysqlのディレクトリ内に移動してくださいね。
env.exampleファイルをコピーします。<br>
コピーした`.env`ファイルにお好みの環境を設定してくださいね。<br>
```
 cp .env.example .env
```
mysqlディレクトリ内に使いたいsqlファイルを入れる(サンプルでprefecture.sqlが入っているので消してね。)<br>
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
