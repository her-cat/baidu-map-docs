# 坐标转换

> 官方文档: http://lbsyun.baidu.com/index.php?title=webapi/guide/changeposition

```php
$coords = '114.21892734521,29.575429778924'; // 需转换的源坐标，多组坐标以“；”分隔
$from = 1;  // 源坐标类型，参考官方文档
$to = 5;    // 目标坐标类型，5：bd09ll(百度经纬度坐标)，6：bd09mc(百度米制经纬度坐标)

$webApi->coords_convert->get($coords, $from, $to);
```

> `$coords` 参数支持数组类型: ['114.2181,29.5754', '114.2189,29.5754', '114.2189,29.5754']

返回结果示例:

```json
{
    "status":0,
    "result":[
        {
            "x":114.2307519546763,
            "y":29.57908428837437
        }
    ]
}
```
