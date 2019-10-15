# 批量请求

> 官方文档: [http://lbsyun.baidu.com/index.php?title=webapi/guide/batch](http://lbsyun.baidu.com/index.php?title=webapi/guide/batch)

```php
$requests = [
    [
        'method' => 'get',
        'url' => '/geocoding/v3/?address=重庆市沙坪坝区学城大道62号&output=json',
    ],
    [
        'method' => 'get',
        'url' => '/reverse_geocoding/v3/?location=35.658651,119.745415&output=json&entensions_poi=0',
    ],
];

$webApi->batch_request->get($requests);
```

返回结果示例: 

```json
{
    "status":0,
    "batch_result":[
        {
            "status":0,
            "result":{
                "location":{
                    "lng":106.3795289775268,
                    "lat":29.609004995890615
                },
                "precise":1,
                "confidence":100,
                "comprehension":100,
                "level":""
            }
        },
        {
            "status":0,
            "result":{
                "location":{
                    "lng":119.74541499999992,
                    "lat":35.65865089820304
                },
                "formatted_address":"山东省青岛市黄岛区港兴大道",
                "business":"",
                "addressComponent":{
                    "country":"中国",
                    "country_code":0,
                    "country_code_iso":"CHN",
                    "country_code_iso2":"CN",
                    "province":"山东省",
                    "city":"青岛市",
                    "city_level":2,
                    "district":"黄岛区",
                    "town":"",
                    "town_code":"",
                    "adcode":"370211",
                    "street":"港兴大道",
                    "street_number":"",
                    "direction":"",
                    "distance":""
                },
                "pois":[

                ],
                "roads":[

                ],
                "poiRegions":[

                ],
                "sematic_description":"",
                "cityCode":236
            }
        }
    ]
}
```