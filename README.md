# react-ts-go-docker
template

基本要件：
日付ごとに座席の登録/編集/削除が可能。
日付ごとの座席表を閲覧可能。
座席表にはメールアドレスを表示。
すでに利用登録されている座席への登録は禁止。
1人で2つ以上の座席への登録は禁止。

拡張要件：
座席表に表示する内容をメールアドレスではなく氏名に変更可能。
複数日に一括登録が可能。
直近1ヶ月の座席利用状況の閲覧。
座席表をExcelでダウンロード可能。

座席表表示APIのレスポンス仕様：
seat_id（座席ID）
seat_name（座席名、例：A-1）
is_seated（使用中かどうか、true/false）
user_id（利用者のID）
user_name（利用者の名前）
email（利用者のメールアドレス）
employee_id（利用者の社員番号）


DB接続
docker exec -it goLangMySQL mysql -uroot -ppassword
exit
docker exec -it <コンテナ名> mysql -u<ユーザー名> -p<パスワード>
<コンテナ名> → ${DB_CONTAINER} に指定した値
<ユーザー名> → ${ROOTUSER} または ${USER_NAME}

USE データベース名;
SHOW TABLES;
Empty set (0.00 sec)
DESCRIBE テーブル名;
