## Web 服务 API

基本用法如下：

```php
$config = [
    'ak' => 'your ak',
//    'sk' => 'your sk',
    'log' => [
        'file' => './baidu-map.log'
    ],
    'response_type' => 'array',
];

$webApi = Factory::webApi($config);
```

`$webApi` 在所有 `Web 服务 API` 的文档中都是指 `Factory::webApi` 得到的示例，就不在每个页面单独写了。
