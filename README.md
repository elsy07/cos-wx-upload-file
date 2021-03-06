# cos-wx-upload-file
微信小程序上传文件到腾讯云v5

## Demo
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/0.gif' width='600' alt='demo'>
</p>

微信小程序仅支持https请求上传文件，所以我们选择了腾讯云作为文件服务器。此外腾讯云提供了配套小程序开发的[SDK](https://github.com/tencentyun/cos-wx-sdk-v5)，方便微信上传文件时调用。

`为了例子的简洁性，这里没有使用服务器鉴权，而采用了前端鉴权`

## 前提
我们假设（哥们儿/妹子）你已经[入门微信小程序开发](https://developers.weixin.qq.com/miniprogram/dev/framework/quickstart/getstart.html#%E7%94%B3%E8%AF%B7%E5%B8%90%E5%8F%B7)

## 准备工作
注册[腾讯云](https://cloud.tencent.com/)

到[COS对象存储控制台](https://console.cloud.tencent.com/cos5) 创建存储桶，

<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/1.png' width='600' alt=''>
</p>

填入存储桶名称等基本信息。为了方便测试，选择公有读私有写
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/2.png' width='600' alt=''>
</p>

为存储桶添加跨域访问规则（重要）
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/3.png' width='600' alt=''>
</p>

如果你不熟悉跨域访问设置，可参考以下配置
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/4.png' width='600' alt=''>
</p>

获取你的 Bucket（存储桶名称), Region（地域名称) 和访问域名
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/5.png' width='600' alt=''>
</p>

到[控制台密钥管理](https://console.cloud.tencent.com/cam/capi) 获取你的 SecretId 和 SecretKey

<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/6.png' width='600' alt=''>
</p>

登录[微信公众平台](https://mp.weixin.qq.com/) 设置 --> 开发设置，将你刚才得到的访问域名填入服务器域名
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/7.png' width='600' alt=''>
</p>

至此，准备工作全部完成

## 运行项目

```sh
git clone https://github.com/piscium2010/cos-wx-upload-file.git
```

编辑cos-wx-upload-file\pages\index\config.js，替换你的 Bucket, Region, SecretId, SecretKey
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/8.png' width='600' alt=''>
</p>

运行小程序
<p align='center'>
<img src='https://raw.githubusercontent.com/piscium2010/cos-wx-upload-file/master/images/9.gif' width='600' alt=''>
</p>


### 写这篇教程就是因为微信的官网教程写得跟___一样，如同意请右上角点赞




#### 羞耻广告位
[designare-table: 企业级react table组件, IE11 下性能完胜Ant Design](https://piscium2010.github.io/designare-table)

[Form 表单联级校验 适配任意UI库：Antd，Office UI fabric， Material ui...](https://github.com/piscium2010/v-form)

[React Proptypes 转 React Typescript 工具](https://github.com/piscium2010/react-proptypes-to-typescript)

[React 轻量级前端控件实例 - 打造你自己的前端控件](https://piscium2010.github.io/lime)



