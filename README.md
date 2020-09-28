# yunpian-php-sdk

[云片](https://www.yunpian.com/) SDK

## 快速开始

- 添加 composer 依赖

```json
"require": {
        "yunpian/yunpian-php-sdk" : "~1.0"
    }
```

**注**: master 是最新稳定版。我们会更新到[Packagist](https://packagist.org/explore/)

- 使用 YunpianClient

```php
use \Yunpian\Sdk\YunpianClient;

//初始化client,apikey作为所有请求的默认值
$clnt = YunpianClient::create($apikey);

$param = [YunpianClient::MOBILE => '18616020000',YunpianClient::TEXT => '【云片网】您的验证码是1234'];
$r = $clnt->sms()->single_send($param);
//var_dump($r);
if($r->isSucc()){
    //$r->data()
}
```
