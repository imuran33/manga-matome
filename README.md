# 漫画まとめサイト（manga-matome）

## 概要

本アプリは、漫画作品の紹介・いいね・コメントなどを行える Web サイト。  
Laravel + MySQL を使い、チームでの共同開発にて制作。  
チーム体制と期間：3人チームで2か月開発。  
週に1回講師とのすり合わせ、1回チームメンバーだけでサイトの方向性などのすり合わせMTGを実施。  

## 主な機能

- 投稿一覧・詳細表示（漫画のタイトル・あらすじ・画像）
- 投稿に対するいいね機能（Ajax対応）
- 投稿の編集・削除（バリデーション付き）
- コメント（リプライ）表示
- 投稿ランキング機能（累計のいいね数を元に、人気投稿をランキング形式で表示）
- 日本語バリデーションメッセージ対応

## 担当箇所（私が実装した機能）

- 投稿一覧表示（投稿のカードデザイン・レイアウト含む）
- 投稿の編集・更新（バリデーション、フォーム制御）
- いいねボタンの実装（非同期通信、カウント更新）
- 投稿ランキング表示（人気順ソート、いいね数集計）
- 日本語バリデーションメッセージの表示設定

## 技術スタック

- フレームワーク: Laravel 10
- フロントエンド: Blade / Tailwind CSS / jQuery
- バックエンド: PHP 8.x
- データベース: MySQL
- その他: GitHub / Docker / VSCode

## セットアップ手順

```bash
git clone https://github.com/imuran33/manga-matome.git
cd manga-matome
cp .env.example .env
composer install
php artisan key:generate
php artisan migrate --seed
php artisan serve
```

## キャプチャなど
トップページ ※最新リプライを右側に表示
![image](https://github.com/user-attachments/assets/fbb2299b-f3df-4fe1-bb46-e5fbbea76737)
いいねランキング
![image](https://github.com/user-attachments/assets/2c078da1-fae3-4296-aa0a-cda469216edf)
ログイン・新規登録時のバリデーションエラー
![image](https://github.com/user-attachments/assets/46765f9f-387c-48b9-aee1-aa4fa6026016)

