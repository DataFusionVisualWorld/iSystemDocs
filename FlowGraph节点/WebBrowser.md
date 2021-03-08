# 浏览器相关节点

用于控制，交互**Pandora**浏览器的节点

这些节点在**QUI->WebBrowser**分类内。



## Init

初始化**WebBrowserProxy**，一般启动时已经初始化，无需调用。

![image-20210307193835895](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210307193835.png)



**入口：**

| 端口 | **作用**        |
| ---- | --------------- |
| Init | WebBrowserProxy |





## Url

用该节点可以命令浏览器访问**URL**。

![image-20210307194254561](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210307194254.png)



**入口：**

| 端口          | **作用**                                |
| ------------- | --------------------------------------- |
| Open          | 打开指定的URL                           |
| Url           | 指定URL，不含附带协议，更多细节请看注释 |
| Path Protocol | 选择URL的协议                           |



### ***注释**

使用**file**协议时，可以访问本地资源。且可以通过绝对路径和短路径访问。

例如，使用 ’**%ENGINEROOT%/\*.\***‘ 可以访问到引擎根目录的文件。

**常用短路径代号：**

| 代号         | **位置**                                 |
| ------------ | ---------------------------------------- |
| %ENGINEROOT% | 引擎根目录                               |
| %ENGINE%     | 根目录内的Engine文件夹                   |
| %EDITOR%     | 根目录内的Editor文件夹                   |
| %USER%       | 用户文件夹，位置不固定，会受其他设置影响 |





## Geometry

该节点用于设置浏览器的位置，大小。

![image-20210307200821485](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210307200821.png)



**入口：**

| 端口   | **作用**             |
| ------ | -------------------- |
| Set    | 打开指定的URL        |
| PosX   | 设定窗口在桌面的坐标 |
| PosY   | 设定窗口在桌面的坐标 |
| Width  | 设定窗口宽度         |
| Height | 设定窗口高度         |





## Visuals

该节点用于控制浏览器视觉相关内容。

![image-20210307202016279](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210307202016.png)



**入口：**

| 端口      | **作用**   |
| --------- | ---------- |
| Show      | 显示浏览器 |
| Hide      | 隐藏浏览器 |
| Close     | 关闭浏览器 |
| Frame     | 显示边框   |
| Frameless | 无边框     |