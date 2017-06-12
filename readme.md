
### xyzphp/log

log support in laravel

### 安装/配置

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

### 使用
```php
    $data = ['name'=>'xyz','sex'=>'男'];
    
    info("info_message",$data);              //记录info 级别的日志
    notice("notice_message",$data);          //记录notice 级别的日志
    debug("debug_message",$data);            //记录debug 级别的日志
    warning("warning_message",$data);        //记录warning 级别的日志
    critical("critical_message",$data);      //记录critical 级别的日志
    alert("alert_message",$data);            //记录alert 级别的日志
    emergency("emergency_message",$data);    //记录emergency 级别的日志
```

### 记录格式
```log
    {date} {time} {project_name} {level} {method} {request_url} {cli_ip} {server_ip} {message} {data}
    2017-06-12 15:21:01 ucenter INFO GET http://localhost 127.0.0.1 10.118.1.173 info_message {"name":"xyz","sex":"男"} 
```



