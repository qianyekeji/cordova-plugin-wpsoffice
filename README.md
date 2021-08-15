# cordova-plugin-wpsoffice
 该插件使用WPS Office SDK 实现了预览、编辑打开doc、pdf、ppt、Excel等文件，编辑模式支持wps office所有功能，比如添加批注、播放等功能。当前插件具体实现：js传递一个文档的网络地址url和文件名filename，首先主app从网络上把文档下载到手机，然后可以设置两种模式（只读/预览和编辑），编辑完，点击保存，保存成功之后，点击右上角返回。返回到主app之后，会收到文档地址。
