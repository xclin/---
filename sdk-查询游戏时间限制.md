# 查询游戏时间限制

>维护人员：**liuy**  
>

## 接口简介
查询游戏时间限制

## 接口详情

### 请求地址
> ```url
> http://apisdk.ggxx.net/apiunionchannels/api/common/1.0.0/real_verification/sdk/get_play_time_limit.php
> ```
>
> ```
> http://apisdk.giantfun.cn/apiunionchannels/api/common/1.0.0/real_verification/sdk/get_play_time_limit.php
> ```
### 请求类型

> GET
>
> POST（application/x-www-form-urlencoded）

##### 请求示例
```url
http://apisdk.ggxx.net/apiunionchannels/api/common/1.0.0/real_verification/sdk/get_play_time_limit.php?Sdkuid=f497659a95c5c3fd10b4358d63f0949d&ver=1.0.0
```
### 请求参数
| 参数名 | 类型 | 必填 | 描述 | 示例值 |
| --- | :---: | :---: | --- | --- |
| ctype | string |  是  | 渠道标识（xyoffical  offical） | xyoffical |
| gid    |  int   |  是  | 游戏id       | 525       |
| c_uid  |  int   |  是  | 用户身份标识 | 6062893 |
| polling_interval | int | 是 | 前端轮询时间间隔，单位秒，最低60秒 | 60 |
| age_level | int | 是 | 用户的年龄标识(0为成年人,1为小于18岁,2为小于16岁,3为小于8岁,默认为0),前端在get_real_verification接口可以查到 | 1 |
| type | int | 是 | 操作系统类型，1：ios； 2：android | 1 |
| ver | string | 否 | 渠道sdk版本号，ios必填 | 1.0.0 |
### 返回正确JSON示例
```json1.1
{
    "code": 0,
    "msg": "ok",
    "data": {
        "allow_login": 1 // 允许当前用户登录
    }
}
```


```
{
    "code": 0,
    "msg": "ok",
    "data": {
        "allow_login": 0 // 禁止当前用户登录
    }
}
```



### 返回错误JSON示例

```json
{
    "code": -1,
    "msg": "必传参数为空",
    "data": []
}
```

```
{
    "code": -2,
    "msg": "轮询时间最低60秒",
    "data": []
}
```



### 备注说明

无
