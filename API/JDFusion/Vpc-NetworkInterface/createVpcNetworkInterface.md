# createVpcNetworkInterface


## 描述
根据云提供商创建网卡

## 请求方式
POST

## 请求地址
https://jdfusion.jdcloud-api.com/v1/regions/{regionId}/vpc_networkInterfaces

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**x-jdcloud-nonce**|String|True| |获取方式请参考签名算法指导文档|
|**x-jdcloud-date**|String|True| |获取方式请参考签名算法指导文档|
|**authorization**|String|True| |获取方式请参考签名算法指导文档|
|**x-jdcloud-fusion-cloudid**|String|True| |云注册信息ID|
|**netInterface**|CreateNetInterface|True| |创建网卡|

### CreateNetInterface
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**id**|String|False| |网卡的Id|
|**name**|String|False| |网卡名称|
|**description**|String|False| |网卡描述信息|
|**vpcId**|String|False| |VPC的Id|
|**type**|String|False| |网卡类型|
|**subnetId**|String|True| |子网id|
|**az**|String|False| |可用区的 ID|
|**associatedPublicIp**|String|False| |弹性网卡关联的公网 IP|
|**privateIpAddress**|String|False| |弹性网卡主私有 IP 地址|
|**macAddress**|String|False| |弹性网卡的 MAC 地址|
|**instanceId**|String|False| |弹性网卡附加的实例 ID|
|**createdTime**|String|False| |创建时间|
|**cloudID**|String|False| |所属云提供商ID|
|**securityGroupId**|String|True| |安全组|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|Result| |
|**requestId**|String|请求ID|

### Result
|名称|类型|描述|
|---|---|---|
|**task**|ResourceTFInfo| |
### ResourceTFInfo
|名称|类型|描述|
|---|---|---|
|**uuid**|String|uuid|
|**body**|String|请求体|
|**status**|String|状态|
|**result**|String|执行结果|
|**createdTime**|String|创建时间|
|**updateTime**|String|更新时间|
|**provider**|String|cloud provider|
|**cloudId**|String|cloud ID|
|**userId**|String|user ID|

## 返回码
|返回码|描述|
|---|---|
|**201**|CREATED|