
### xyzphp/log

log support in laravel

### 用法

```
composer require xyzphp/log
```

或者在你的 `composer.json` 的 require 部分中添加:

```
"xyzphp/log": "1.0.*"
```

下载完毕之后,直接配置 `app/config.php` 的 `providers`:

```php
        Xyzphp\Log\LogServiceProvider::class,
```

配置日志文件路径 `app/config.php`
```php
    
        'log_path' => env('APP_LOG_PATH', storage_path('logs/laravel.log')),
```

编辑 `.env` 文件
```
        APP_LOG_LEVEL=/tmp/xyzphp.log
```