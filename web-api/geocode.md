# 地理编码

> 官方文档: [http://lbsyun.baidu.com/index.php?title=webapi/guide/webservice-geocoding](http://lbsyun.baidu.com/index.php?title=webapi/guide/webservice-geocoding)

```php
$address = '北京市海淀区上地十街10号'; // 待解析的地址，最多支持84个字节。
$options = [
    'city' => '北京', // 地址所在的城市名。
    // 更多可选参数请参考官方文档
];

$webApi->geocode->get($address, $options);
```

返回结果示例:

```json
{
    "status":"0",
    "result":{
        "location":{
            "lng":"116.308420292",
            "lat":"40.0570303335"
        },
        "precise":"1",
        "confidence":"80",
        "comprehension":"100",
        "level":"道路"
    }
}
```
