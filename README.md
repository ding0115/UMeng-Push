<h1 align="center"> umeng </h1>

<p align="center"> 友盟推送.</p>


## Installing

```shell
$ composer require hedeqiang/umeng -vvv
```

## Usage

```php
require __DIR__ .'/vendor/autoload.php';

use Hedeqiang\UMeng\Android;
use Hedeqiang\UMeng\IOS;

//安卓 友盟 KEY
$android_AppKey = '5b1df163f29d98*****';
$android_Message_Secret = '19077a28fb4c1ef3*****';
$android_Master_Secret = 'i7tzdarswtrjw2yok*******';

//IOS 友盟 KEY and secret
$ios_AppKey = '5b1df0d1f29d**********';
$ios_Master_Secret = 'fa9ry9kdk8na9pfqsk***********';

$android = new Android($android_AppKey,$android_Master_Secret,true);


$alias = 113;
$alias_type = 'APP';
$ticker = '通知';
$title = '通知';
$text = 'test ';
$android->sendAndroidCustomizedcast($alias, $alias_type, $ticker, $title, $text,'go_app');

$ios = new IOS($ios_AppKey, $ios_Master_Secret,true);
$ios->sendIOSCustomizedcast($alias, $alias_type, $title, $text);

```


## License

MIT