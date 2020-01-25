# テーブルの操作
## mysqlへの接続
  mysqlを使用して実行する  
  `mysql -u root`  
  このコマンドはmysqlにユーザー名がrootで接続するという意  
  * データベースの一覧  
  `SHOW DATABASES;`  
  SQL文の終わりには`;`を忘れずに  


## データベースの作成
  `CREATE DATABASE データベース名;`
## データベースの選択
  `USE データベース名;`
## テーブルの確認
  データベースにどのようなテーブルが存在するかを一覧で表示  
  `SHOW TABLES;`
## テーブルの作成
  テーブル名と、そのテーブルに作成するカラムの名前とカラムの型を指定することができる。  
  `CREATE TABLE テーブル名 (カラム名 カラム名の型, ……);`  
  例）"INT"型のカラム"id"と、"VARCHAR(255)"型のカラム"name"のある"goods"テーブルの場合  
  `CREATE TABLE goods (id INT, name VARCHAR(255));`となる