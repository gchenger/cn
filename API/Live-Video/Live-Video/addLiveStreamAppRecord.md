# addLiveStreamAppRecord


## 描述
添加APP录制配置

## 请求方式
POST

## 请求地址
https://live.jdcloud-api.com/v1/recordApps:config


## 请求参数
|名称|类型|是否必需|描述|
|---|---|---|---|
|**appName**|String|True|直播流所属应用名称|
|**publishDomain**|String|True|您的推流加速域名|
|**template**|String|True|录制模版|

## 示例
    {
        "publishDomain": "push.yourdomain.com",
        "appName": "live",
        "template": "test-live-video"
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
