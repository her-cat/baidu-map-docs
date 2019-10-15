# 普通 IP 定位

> 官方文档：http://lbsyun.baidu.com/index.php?title=webapi/ip-api

```php
$ipAddress = '127.0.0.1';   // ip 地址
$coordinateType = null; // 坐标类型, 不传默认百度墨卡托坐标，bd09ll：百度经纬度坐标，gcj02：国测局02坐标

$webApi->ip_locate->get($ipAddress, $coordinateType);
```

返回结果示例:

```json
{
    "address":"CN|广东|深圳|None|CHINANET|0|0",
    "content":{
        "address_detail":{
            "province":"广东省",
            "city":"深圳市",
            "district":"",
            "street":"",
            "street_number":"",
            "city_code":340
        },
        "address":"广东省深圳市",
        "point":{
            "y":"2561692.45",
            "x":"12681452.34"
        }
    },
    "status":0
}
```
