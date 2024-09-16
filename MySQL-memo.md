# MySQL
## ログイン
### localhostのMySQLサーバに接続(root)
```sh
$ mysql -u root -p
```
### 外部のMySQLサーバに接続
```sh
$ mysql -u [ユーザー名] -p -h [host名] -P [ポート番号]
```
## ログアウト
### ログアウト①
```SQL
mysql > quit
```
### ログアウト②
```SQL
mysql > exit
```
## データベース関連
### データベース一覧
```SQL
mysql > SHOW DATABASES;
```
### データベース追加
```SQL
mysql > CREATE DATABASE [追加するデータベース名];
```
### データベースを選択
```SQL
mysql > USE [使用するデータベース名];
```
## テーブル関連
### テーブル一覧
```SQL
mysql > SHOW TABLES;
```
### テーブル内の特定のフィールド検索
```SQL
mysql > SELECT [カラム名] FROM [テーブル名] WHERE [条件式];
```
### テーブルの作成
```SQL
mysql > CREATE TABLE [作成するテーブル名] (
    [フィールド名] [データ型] [オプション],
    [フィールド名] [データ型] [オプション],
    [フィールド名] [データ型] [オプション]
);
```
### テーブル削除
```SQL
mysql > DROP TABLE IF EXISTS [削除するテーブル名];
```
### テーブル名の変更
```SQL
mysql > ALTER TABLE [旧テーブル名] RENAME [新テーブル名];
```
### テーブルにカラムの追加
```SQL
mysql > ALTER TABLE [テーブル名] ADD [追加カラム名] [型] [オプション];
```
### テーブルのカラムの型変更
```SQL
mysql > ALTER TABLE [テーブル名] MODIFY [カラム名] [型] [オプション];
```
### テーブルに格納されているすべてのデータを削除
```SQL
mysql > TRUNCATE TABLE [テーブル名];
```
>外部キー制約を無視する命令  
>SET FOREIGN_KEY_CHECKS=0;
### テーブル設計の確認
```SQL
mysql > DESC [確認したいテーブル名];
```
### テーブル設計の確認(詳細表示)
```SQL
mysql > SHOW FULL COLUMNS FROM [確認したいテーブル名];
```
## レコード操作関連
### レコードの追加
```SQL
mysql > INSERT INTO [テーブル名] (フィールド名1,フィールド名2) VALUES (値1,値2);
```
### レコードの更新
```SQL
mysql > UPDATE [テーブル名] SET [フィールド名]=[値] WHERE [条件式];
```
### 全レコードの削除
```SQL
mysql > DELETE FROM [テーブル名];
```
### 一部レコードの削除
```SQL
mysql > DELETE FROM [テーブル名] WHERE [条件式];
```
