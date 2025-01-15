# 微信网页授权

该页面单独发布，用于微信网页授权，授权后跳转回原页面。

## 官方文档

[👉 微信网页开发/网页授权](https://developers.weixin.qq.com/doc/offiaccount/OA_Web_Apps/Wechat_webpage_authorization.html)

## 公众号配置方法

1. 登录服务号，查找 **“设置与开发/账号设置/功能设置”**，在其中配置 **网页授权域名**。

2. 在配置时，需要将校验文件 `MP_verify_jyei6X9Axx8KhFmu.txt` 一并部署在域名根目录下。

## 使用说明

**线上地址**：<https://szh.jshkxcl.cn/wx/getWxGzhAuthCode.html>

### 步骤

1. 在项目中引导用户打开[微信授权接口](https://developers.weixin.qq.com/doc/offiaccount/OA_Web_Apps/Wechat_webpage_authorization.html#0)，具体拼接参数详见官方文档；
2. 微信将携带授权码返回该页面；
3. 在该页面中，`getCode()` 方法会提取授权码，返回至项目页面（目前有抽奖、小程序两个页面）；
4. 在项目中使用授权码进行业务逻辑。

### parameter 参数说明

| 参数     | 说明                                                     | 默认值 |
| -------- | -------------------------------------------------------- | ------ |
| code     | 微信授权码                                               | -      |
| platform | 前往不同的项目平台（目前有：抽奖- choujiang，小程序-wx） | wx     |

> **示例：** <https://szh.jshkxcl.cn/wx/getWxGzhAuthCode.html?platform=choujiang&code=xxxx>
