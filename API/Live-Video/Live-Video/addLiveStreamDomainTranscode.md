# addLiveStreamDomainTranscode


## 描述
添加域名转码配置

## 请求方式
POST

## 请求地址
https://live.jdcloud-api.com/v1/transcodeDomains:config


## 请求参数
|名称|类型|是否必需|描述|
|---|---|---|---|
|**publishDomain**|String|True|直播的推流域名|
|**template**|String|True|转码模版后缀|


## 示例
    {
        "publishDomain": "push.yourdomain.com",
        "template": "test-live-video
    }

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|requestId|


## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|
