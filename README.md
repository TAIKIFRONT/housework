# 初期設定
1. git clone git@github.com:TAIKIFRONT/housework.git

2. docker起動  
cd housework
docker-compose up -d --build

3. laravelセットアップ  
```
docker exec -it app bash
composer update
chown -R 1000:1000 *
chmod -R 777 storage
php artisan migrate
php artisan db:seed --class=Database\\Seeders\\TestDataSeeder
php artisan key:generate
npm install
npm run build
```

4. Larevel Filamentセットアップ
```
php artisan make:filament-user
```

5. 画面表示  
https://localhost

6. ログイン  
https://localhost/admin/login
