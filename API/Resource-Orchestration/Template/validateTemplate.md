# validateTemplate


## 描述
模板校验

## 请求方式
POST

## 请求地址
https://jdro.jdcloud-api.com/v1/regions/{regionId}/templateValidate

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域 ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**environment**|Environment|False| | |
|**template**|Object|True| |模板|
|**validateMode**|String|False| |可取值:(validateTemplate (检测模板), validateStack (检测模板和environment)) 默认validateTemplate|

### Environment
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**disableRollback**|Boolean|False| |禁止回滚，默认false，即创建资源栈失败时回滚|
|**name**|String|True| |资源栈名称|
|**params**|Object|False| |自定义参数值map, 内容为键值对形式，key为参数，value为自定义参数值。Params中的参数值会覆盖模板文件中参数的默认值。|
|**timeout**|Long|True| |超时时间，单位分钟，范围10-180|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|Result| |
|**requestId**|String|请求的标识id|

### Result
|名称|类型|描述|
|---|---|---|
|**describe**|String| |
|**result**|Object|验证模板结果信息，JSON格式|

## 返回码
|返回码|描述|
|---|---|
|**200**|验证模板通过|
