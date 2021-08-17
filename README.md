![cordova](https://qianyedoufu.com/images/cordova.png)
# WPS Office办公插件使用说明文档
##前言

###### WPS Office自定义Cordova插件
---
## Cordova 插件介绍
###该插件使用WPS Office SDK 实现了预览、编辑打开doc、pdf、ppt、Excel等文件，编辑模式支持wps office所有功能，比如添加批注、播放等功能。当前插件具体实现：js传递一个文档的网络地址url和文件名filename，首先主app从网络上把文档下载到手机，然后可以设置两种模式（只读/预览和编辑），编辑完，点击保存，保存成功之后，点击右上角返回。返回到主app之后，会收到文档地址。
---
## 效果展示
![wps](https://qianyedoufu.com/images/wps.PNG)


###cordova-plugin-wpsoffice使用方法
```
代码块
//打开云端在线文档
function openwpsol() {
            var sendStr;
            //传值到原生
            sendStr = {
                "url" : "https://www.qianyedoufu.com/plugin/Files/",
                "filename":"PDF.pdf",
                "model":"AIDL"    //edit是编辑模式，AIDL是只读模式
            };
        org.apache.cordova.wpsoffice.openol(sendStr,function(data) {
        alert(data);//data是文档所在位置
                                                                  },
                                                                  function(fail) {

                                                                  return;

                                                                  });
        }
        //打开本地路径文档
        function openwps() {
            var sendStr;
            //传值到原生
            sendStr = {
                "filePath" : "https://www.qianyedoufu.com/plugin/Files/",
                "model":"AIDL"    //edit是编辑模式，AIDL是只读模式
            };
        org.apache.cordova.wpsoffice.openlocal(sendStr,function(data) {
        alert(data);//data是文档所在位置
                                                                  },
                                                                  function(fail) {

                                                                  return;

                                                                  });
        }
```
## 完毕！
[README](https://qianyedoufu.com/app/plugins/wps/README.md)