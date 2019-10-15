# 时区服务

> 官方文档地址 [http://lbsyun.baidu.com/index.php?title=webapi/guide/timezone](http://lbsyun.baidu.com/index.php?title=webapi/guide/timezone)


```php
$longitude = '经度';
$latitude = '纬度';

// 非必传参数
$timestamp = time();
$coordType = 'bd09ll';  // 请求参数中坐标的类型，bd09ll，gcj02ll，wgs84ll，bd09mc

$webApi->timezone->get($longitude, $latitude, $timestamp, $coordType);
```

返回结果示例:

```json
{
    "status":0,
    "timezone_id":"Asia/Shanghai",
    "dst_offset":0,
    "raw_offset":28800
}
```
