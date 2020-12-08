# Tool节点分类

此分类下有各种功能性的节点。



## CloseGame

该节点设计目的是方便用户关闭客户端(Launcher)，Editor无效。

![image-20201130161646079](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201130161646.png)

**入口：**

| 端口  | 作用         |
| ----- | ------------ |
| Close | 关闭Launcher |







## CompareStringIgnoreCase

该节点用来判断字符串A与B是否一致，无视大小写。

![image-20201130161813298](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201130161813.png)

**入口：**

| 端口    | 作用    |
| ------- | ------- |
| String1 | 字符串A |
| String2 | 字符串B |

**出口：**

| 端口  | 作用             |
| ----- | ---------------- |
| True  | A与B一致时触发   |
| False | A与B不一致时触发 |