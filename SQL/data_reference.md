# データの参照
SELECT 文を用いてデータベースに欲しいデータを生成するように指示する
## 基本的な検索の構文
`SELECT * FROM テーブル名`  
* FROM句  
テーブル名を指定  
`FROM テーブル名`  
* SELECT句  
カラム名を指定  
`SELECT カラム名`  
注）アスタリスクは全てのカラムを取得するというワイルドカード
## 取得レコードの制限
* WHERE句  
WHERE句では取得するレコードの条件を指定し、その条件が正のレコードを取得。  
`WHERE 条件`  
WHERE句の条件には、以下のように"="や"<="のような比較演算子を使用することが出来ます。  
**加えてANDやORのような、論理演算子を使用する**  
  * AND演算子  
  ageが20以下かつprefectureが福岡県のレコードを取得  
  `SELECT *`  
  `FROM users`  
  `WHERE age <= 20 AND prefecture = "福岡県"`  
  * OR演算子  
  ageが20以下もしくはprefectureが福岡県であるレコードを取得  
  `SELECT *`  
  `FROM users`  
  `WHERE age <= 20 OR prefecture = "福岡県"`  
  * NOT演算子  
  prefectureが福岡県でないレコードを取得  
  `SELECT *`  
  `FROM users`  
  `WHERE NOT prefecture = "福岡県"`  
**範囲指定に使える演算子**  
  * BETWEEN演算子  
  ageが20以上25以下のuserを取得  
  `SELECT *`  
  `FROM users`  
  `WHERE age BETWEEN 20 AND 25`  
  