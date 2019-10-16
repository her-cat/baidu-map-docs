# 静态图

> 官方文档: [http://lbsyun.baidu.com/index.php?title=static](http://lbsyun.baidu.com/index.php?title=static)

> 注意: 支持浏览器端 AK 和 Android/IOS SDK 的 AK，服务端 AK 不支持 sn 校验方式。

```php
use HerCat\BaiduMap\Kernel\Http\StreamResponse;

$longitude = '116.30815';
$latitude = '40.056878';

$options = [
    'width' => 200,  // 图片宽度
    'height' => 100, // 图片高度
    'zoom' => 16,    // 地图级别
    //
];

/** @var StreamResponse $image */
$response = $webApi->static_map->get($longitude, $latitude);

if ($response instanceof StreamResponse) {
    $response->save('your/path', 'file_name');
}
```
