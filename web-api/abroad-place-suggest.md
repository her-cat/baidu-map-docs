# 境外地点输入提示 v1.0

> 官方文档: [http://lbsyun.baidu.com/index.php?title=webapi/place-suggestion-api-abroad](http://lbsyun.baidu.com/index.php?title=webapi/place-suggestion-api-abroad)

```php
$keyword = '公园';   // 关键词
$region = '纽约';    // 检索地区名称，当前建议传入城市名称

$options = [
    'ret_coordtype' => 'gcj02ll',   // 坐标类型，默认 bd09ll（百度经纬度），国外为 wgs84
    // 更多可选参数请参考官方文档
];

$webApi->abroad_place_suggest->get($keyword, $region, $options);
```
