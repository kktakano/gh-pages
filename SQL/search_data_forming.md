# 検索したデータの形成
## データの結合<CONCAT関数>
２つのカラムを併せて１つのカラムとして表示させる  
CONCAT関数は複数の文字列を連結させる事ができる関数。  
`CONCAT(文字列1, 文字列2, ……)`
例）SELECT句を使用し"family_name""first_name"の中身を連結させる。  
`SELECT CONCAT(family_name, first_name)`  
`FROM users`  
## 検索結果のカラム名の変更<AS句>
上のCONCAT関数を使用した検索結果のカラム名は"CONCAT(family_name, first_name)"とSQL文そのままの表示となっている。  
そこで検索結果のカラム名を変更してみる。  
**AS句**  
SELECT句でデータを取得するとき、AS句を併用すると、そのカラムに別名を付けることが出来る。  
`SELECT CONCAT(family_name, first_name) AS "名前"`  
`FROM users`  
ちなみに"AS"は省略する事が可能
## 重複する行の除外<DISTINCT>
DISTINCTを使用すると、指定したカラムの値が重複する行を除外してデータを取得取得する事ができる。  
`SELECT DISTINCT カラム名`  
例）  
`SELECT user_id`  
`FROM shifts`  
`WHERE date = "2015-07-01"`  
これでは一日の内に2コマ分あるひとはuser_idが重複する。  
  
`SELECT DISTINCT user_id`  
`FROM shifts`  
`WHERE date = "2015-07-01"`  
SELECT句がuser_idからDISTINCT user_idとなったことで、"user_id"が重複する行を除いたSQL文となる。  
  
## レコードのグループ化<GROUP BY句>
GROUP BY句を使用すると、指定したカラムが同じ値を持つデータを1つのグループとしてまとめることが出来る。  
`GROUP BY カラム名`  
例）"shifts"テーブルから"date"が"2015-07-01"のレコード取得  
  "user_id"が同じ値のレコードをグループ化し、そのグループ化された一覧の"user_id"のみを表示  
  `SELECT user_id`  
  `FROM shifts`  
  `WHERE date = "2015-07-01"`  
  `GROUP BY user_id`  
  
