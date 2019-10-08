# 地点检索 v2.0

> 官方文档地址：[http://lbsyun.baidu.com/index.php?title=webapi/guide/webservice-placeapi](http://lbsyun.baidu.com/index.php?title=webapi/guide/webservice-placeapi)

## 行政区划区域检索

```php
$keyword = '关键词';
$region = '行政区域，如北京、131（北京的code）、海淀区、全国，等';
$options = [
    'tag' => '美食',
    // 更多可选参数请参考官方文档
];

$webApi->place_search->region($keyword, $region, $options);
```

## 圆形区域检索

```php
$keyword = '关键词';
$longitude = '经度';
$latitude = '纬度';
$options = [
    'radius' => '1000',
    // 更多可选参数请参考官方文档
];

$webApi->place_search->circle($keyword, $longitude, $latitude, $options);
```

## 矩形区域检索

```php
$keyword = '关键词';
$bounds = '矩形区域的经纬度，38.76623,116.43213,39.54321,116.46773 lat,lng(左下角坐标),lat,lng(右上角坐标)';

$latitude = '纬度';
$options = [
    'tag' => '美食',
    // 更多可选参数请参考官方文档
];

$webApi->place_search->rectangle($keyword, $longitude, $latitude, $options);
```


> `$bounds` 参数支持数组类型：
>
>  $bounds = [38.76623, 116.43213, 39.54321, 116.46773];

## 地点详情检索

````php
$uid = 'poi 的 uid';

$scope = 1; // 检索结果详细程度, 1: 基本信息 2: 详细信息

$webApi->place_search->get($uid, $scope);
````

> `$uid` 参数支持数组类型：
>
>  $uid = ['uid1', 'uid2', 'uid3'];
