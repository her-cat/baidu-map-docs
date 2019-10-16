# 地点输入提示 v2.0

> 官方文档: [http://lbsyun.baidu.com/index.php?title=webapi/place-suggestion-api](http://lbsyun.baidu.com/index.php?title=webapi/place-suggestion-api)

```php
$keyword = '欢乐谷';   // 关键词
$region = '深圳';      // 支持全国、省、城市及对应百度编码

$options = [
    'city_limit' => true,   // 是否仅返回 region 中指定城市检索结果
    // 更多可选参数请参考官方文档
];

$response = $webApi->place_suggest->get($keyword, $region, $options);
```

返回结果示例:

```json
{
    "status":"0",
    "message":"ok",
    "result":{
        "name":[
            "欢乐谷",
            "欢乐谷-公交车站",
            "欢乐谷-停车场",
            "深圳欢乐谷停车场",
            "欢乐谷",
            "欢乐谷",
            "成都欢乐谷",
            "武汉欢乐谷",
            "欢乐谷休闲会所(龙华丰源分店)",
            "北京欢乐谷"
        ],
        "location":[
            {
                "lat":"22.547899",
                "lng":"113.987186"
            },
            {
                "lat":"22.543998",
                "lng":"113.985135"
            },
            {
                "lat":"22.547356",
                "lng":"113.984669"
            },
            {
                "lat":"22.547226",
                "lng":"113.982748"
            },
            {
                "lat":"22.827957",
                "lng":"113.696148"
            },
            {
                "lat":"23.189727",
                "lng":"113.279764"
            },
            {
                "lat":"30.729004",
                "lng":"104.040307"
            },
            {
                "lat":"30.59723",
                "lng":"114.399429"
            },
            {
                "lat":"22.653328",
                "lng":"114.029809"
            },
            {
                "lat":"39.873848",
                "lng":"116.501366"
            }
        ],
        "uid":[
            "d04ca873026457d5882fb592",
            "01b005c80c88c3d89222e031",
            "8da74f0ff0cab5deae31e5f6",
            "4bddccbfb89954bdd13ce337",
            "e5533bb8c433824195f08cda",
            "aa4ce5bc922550b2b04c4983",
            "5996cc39129bf8038b2fb5d2",
            "4f161ac9b705745ea8f72916",
            "eef2d528079bbcda3be4a67e",
            "91c13f93bcdcccfa20f0179a"
        ],
        "city":[
            "深圳市",
            "深圳市",
            "深圳市",
            "深圳市",
            "东莞市",
            "广州市",
            "成都市",
            "武汉市",
            "深圳市",
            "北京市"
        ],
        "district":[
            "南山区",
            "南山区",
            "南山区",
            "南山区",
            null,
            "白云区",
            "金牛区",
            "洪山区",
            "龙华区",
            "朝阳区"
        ],
        "business":[
            null,
            null,
            null,
            null,
            null,
            null,
            null,
            null,
            null,
            null
        ],
        "cityid":[
            "d04ca873026457d5882fb592",
            "01b005c80c88c3d89222e031",
            "8da74f0ff0cab5deae31e5f6",
            "4bddccbfb89954bdd13ce337",
            "e5533bb8c433824195f08cda",
            "aa4ce5bc922550b2b04c4983",
            "5996cc39129bf8038b2fb5d2",
            "4f161ac9b705745ea8f72916",
            "eef2d528079bbcda3be4a67e",
            "91c13f93bcdcccfa20f0179a"
        ]
    }
}
```
