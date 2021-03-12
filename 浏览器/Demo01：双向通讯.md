# Demo 00 ：网页端与CryEngine双向通讯

对应场景名称为**WebBrowserDemo01**，对应**html**文件为**%ENGINEROOT%/Bin/win_x64/wb/demo/demo2.html**。

该场景展示了如何从网页端向Cryengine发送信息、如何从Cryengine向网页端发送信息。

![image-20210312103344361](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210312103344.png)



## CryEngine接收网页端信息

与Demo00相同，参考Demo00



## CryEngine向网页端发送信息

iSystem提供了节点**QUI:WebBrowser:RunJavaScript**，利用该节点，可以发送信息到网页端，也可以直接执行一段JavaScript代码。

![image-20210312102538360](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210312102538.png)

此处JavaScript内容为：

```javascript
MSGfromCPP("&#x4F20;&#x8F93;&#x4E2D;&#x6587;&#x5230;&#x7F51;&#x9875;")
```

HTML中也有对应的函数：

```javascript
function output(message){
	var output = document.getElementById("output");
	output.innerHTML = output.innerHTML + message + "\n";
}

function MSGfromCPP(message){
	output("CPP调用了函数，参数为: " + message);
}
```



最终效果：

 ![image-20210312102915159](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210312102915.png)



## 注意

实际上RunJavaScript节点并非只能执行函数，它可以执行更为复杂的JavaScript。但是受到FG限制，执行的代码不可换行。

以Demo01执行的JS结果为例，我们可以直接执行以下代码达到同样的效果。

```javascript
op=document.getElementById("output");op.innerHTML=op.innerHTML+"&#x4F20;&#x8F93;&#x4E2D;&#x6587;&#x5230;&#x7F51;&#x9875;\n";
```



最终效果：

 ![image-20210312104745038](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210312104745.png)