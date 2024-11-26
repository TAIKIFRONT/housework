# 初期設定
1. git clone git@github.com:TAIKIFRONT/housework.git src

2. docker起動  
cd housework-docker
docker-compose up -d --build

3. laravelセットアップ
```
docker exec -it app bash
composer install
chown -R 1000:1000 *
chmod -R 777 storage
php artisan migrate
php artisan key:generate
php artisan storage:link 
npm install
npm run build
```

4. 画面表示  
https://localhost

5. ユーザー作成
```
php artisan make:filament-user
```

6. ログイン画面へアクセス
https://localhost/admin/login

7. 作成したユーザーでログイン
