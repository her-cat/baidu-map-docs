# 普通 IP 定位

> 官方文档：http://lbsyun.baidu.com/index.php?title=webapi/ip-api

```php
$ipAddress = '127.0.0.1';   // ip 地址
$coordinateType = null; // 坐标类型, 不传默认百度墨卡托坐标，bd09ll：百度经纬度坐标，gcj02：国测局02坐标

$result = $webApi->ip_locate->get($ipAddress, $coordinateType);

//  Array
//  (
//      [address] => CN|广东|深圳|None|CHINANET|0|0
//      [content] => Array
//          (
//              [address] => 广东省深圳市
//              [address_detail] => Array
//                  (
//                      [city] => 深圳市
//                      [city_code] => 340
//                      [district] =>
//                      [province] => 广东省
//                      [street] =>
//                      [street_number] =>
//                  )
//
//              [point] => Array
//                  (
//                      [x] => 114.0153235
//                      [y] => 22.53165289
//                )
//
//        )
//
//      [status] => 0
//  )
```