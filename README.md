# [Fiddler-Everywhere-Crack-CN]

### 

## 前言

本项目中所采用的思路只为了技术交流 请于下载后24小时内删除

后续不会更新了

## 食用方式

需要先登录账号进去，要不然弄好后再去登录时无法登录的，其实看起来似乎并没有真的破解成功，我账号处于30天试用，不敢保证；
再补充一句，我几乎不会用这玩意，，，，因为：
1、深度绑定账号，断网用不了，网络不好（需要富强）打不开
2、有汉化

## main.xxxx.js

打开 `ClientApp/dist/main.xxxxxxxxxxxxxxxxx.js` 搜索 `updateUserLicense` 查看修改详情

## Fiddler.WebUi.il

> 修改 `main.js` 前需要先修改此处 （有文件校验）

```javascript
// il line: 135843
string mainBytes = ElectronMainConstants.mainBytes;
if (mainBytes == null || !mainBytes.Equals(result, StringComparison.OrdinalIgnoreCase))
{
    // 报错点
    error = string.Format(errorTemplatePrefix, "calculating") + errorTemplateSuffix + " Support";
    // il line: 135843
    return false;
}
```

也可以直接替换为项目中的文件 

- main.157031b9c4f17398.js 为OSx的文件(已经做了简单的汉化)
- main.304c864f4d0af6e9.js 为Win的文件(已经做了简单的汉化)

## FiddlerBackendSDK.dll

### method FiddlerBackendSDK.User.UserClient::GetBestAccount

删除 IL_000d - IL_0020 对应 if 语句 删除 IL_003f - IL_0040 对应 `return null;` 语句

### method '<>c__DisplayClass18_0'::'b__0'

删除 IL_0000 - IL_0019 , 在 IL_001e 前插入 `ldc.i4.1` (即函数体直接返回 `true` )

为了方便使用`FiddlerBackendSDK.dll`也提供了修改好的版本 可以直接替换 

----

**感谢下列文章提供方法 作者只是做了简单的汉化**

https://github.com/msojocs/fiddler-everywhere-crack

https://www.52pojie.cn/thread-1654857-2-1.html

https://www.52pojie.cn/thread-1654205-2-1.html

https://www.52pojie.cn/thread-1635558-1-3.html

------

## 🅱️免责声明

该工具仅用于学习

由于传播、利用此工具所提供的信息而造成的任何直接或者间接的后果及损失，均由使用者本人负责，作者不为此承担任何责任。

本人拥有对此工具的修改和解释权。未经网络安全部门及相关部门允许，不得善自使用本工具进行任何攻击活动，不得以任何方式将其用于商业目的。

该工具只授权于企业内部进行问题排查，请勿用于非法用途，请遵守网络安全法，否则后果作者概不负责
