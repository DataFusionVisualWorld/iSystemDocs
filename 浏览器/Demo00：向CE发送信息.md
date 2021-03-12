# Demo 00 ：从网页端发送信息到CryEngine

对应场景名称为**WebBrowserDemo00**，对应**html**文件为**%ENGINEROOT%/Bin/win_x64/wb/demo/demo.html**。

该场景展示了如何从网页端向Cryengine发送信息。

![image-20210312101445332](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210312101445.png)



## 建立与CryEngine的链接

在html内使用JavaScript，与CE建立链接。

```javascript
new QWebChannel(qt.webChannelTransport, function(channel){
                    context = channel.objects.RemoteContext;  // 与C++代码内的变量关联
})
```



## 使用预设的函数发送信息

iSystem提供了名为**OnMessage(string, string)**的函数，此函数可以在html内使用JavaScript进行调用。

```javascript
function sendMsgToCPP(_msg, _params){
	context.OnMessage(_msg, _params);   // 调用C++内对应的槽函数
}
```



### 在CryEngine内接收信息

在CryEngine中，可以使用**QUI:WebBrowser:Listener**节点监听网页端传来的信息。

![image-20210312101258991](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210312101259.png)