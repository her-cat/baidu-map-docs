# 逆地理编码

> 官方文档: [http://lbsyun.baidu.com/index.php?title=webapi/guide/webservice-geocoding-abroad](http://lbsyun.baidu.com/index.php?title=webapi/guide/webservice-geocoding-abroad)

```php
$longitude = '116.308420292';
$latitude = '40.0570303335';

$options = [
    'coordtype' => 'bd09ll', // 坐标的类型，默认 bd09ll。目前支持的坐标类型包括：bd09ll（百度经纬度坐标）、bd09mc（百度米制坐标）、gcj02ll（国测局经纬度坐标，仅限中国）、wgs84ll（ GPS经纬度）
    // 更多可选参数请参考官方文档
];

$webApi->reverse_geocode->get($longitude, $latitude, $options);
```

返回结果示例:

```json
{
    "status":"0",
    "result":{
        "location":{
            "lng":"116.308420292",
            "lat":"40.0570303984"
        },
        "formatted_address":"北京市海淀区上地十街10",
        "business":"上地,西二旗,回龙观",
        "addressComponent":{
            "country":"中国",
            "country_code":"0",
            "country_code_iso":"CHN",
            "country_code_iso2":"CN",
            "province":"北京市",
            "city":"北京市",
            "city_level":"2",
            "district":"海淀区",
            "town":null,
            "town_code":null,
            "adcode":"110108",
            "street":"上地十街",
            "street_number":"10",
            "direction":"附近",
            "distance":"38"
        },
        "pois":null,
        "roads":null,
        "poiRegions":null,
        "sematic_description":null,
        "cityCode":"131"
    }
}
```
