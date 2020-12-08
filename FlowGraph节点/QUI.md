# QUI相关节点

这里有**iSystem**所有**QUI**分类下的节点介绍。

[什么是QUI?](../QUI/概述.md)



## CompassController

指南针Widget控制器节点。

![image-20201121220052833](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121220052.png)

**入口：**

| 入口名称 | 作用描述 |
| -------- | -------- |
| Show     | 显示     |
| Hide     | 隐藏     |
| Offset   | 角度偏移 |





## DBItemTableView

用于显示Excel xml表格的界面。

![image-20201126164750303](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201126164750.png)

**入口：**

| 入口名称 | 作用描述                  |
| -------- | ------------------------- |
| Locate   | 指的是excel内的工作簿名称 |
| Show     | 显示指定Locate的表格      |







## DbfTableView

用于显示Dbf文件的表格界面。

![image-20201126170524554](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201126170524.png)

**入口：**

| 入口名称  | 作用描述                            |
| --------- | ----------------------------------- |
| Open      | 打开界面                            |
| Hide      | 隐藏界面                            |
| Close     | 关闭界面，释放内存                  |
| Load File | 根据File Path端口指定的路径读取文件 |
| File Path | *.dbf文件的路径                     |







## EventListener

[**QUI系统内部事件（Event）**](../QUI/QUI事件.md)监听器

![image-20201127191304047](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201127191311.png)

**入口：**

| 入口名称     | 作用描述                                          |
| ------------ | ------------------------------------------------- |
| Start        | 开始监听                                          |
| Stop         | 停止监听                                          |
| Group Filter | 设定QUIEvent的Group过滤器，留空则监听所有组的事件 |



**出口：**

| 出口名称 | 作用描述                    |
| -------- | --------------------------- |
| Group    | 监听到的事件的**Group分组** |
| Event    | 监听到的事件的名称          |







# FileDialog

文件对话框，分为打开和保存两种形式。

![image-20201127191805155](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201127191805.png)

**入口：**

| 入口名称    | 作用描述                                                     |
| ----------- | ------------------------------------------------------------ |
| Dialog Type | 对话框类型，可选OpenFile和SaveFile                           |
| Open        | 呼叫对话框                                                   |
| Title       | 设定对话框标题栏                                             |
| Directory   | 指定初始化目录的行为模式，有**Assign分配**、**Last上次打开的目录**、**Default程序默认目录** |
| Assign Dir  | 设定当Directory端口被设定为Assign时，对话框的初始化目录      |
| Filter      | 设定文件对话框的格式过滤器，例如：txt(*.txt)                 |



**出口：**

| 出口名称  | 作用描述                     |
| --------- | ---------------------------- |
| Succeed   | 输出布尔类型数值，TRUE为成功 |
| Full Path | 文件的完整路径               |
| Directory | 文件所在文件夹的路径         |
| File Name | 文件名称，包括扩展名         |







# FloatingToolBarController

可以控制浮动工具条的显示与隐藏。

![image-20201127193001063](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201127193001.png)

**入口：**

| 入口名称 | 作用描述       |
| -------- | -------------- |
| Show     | 显示浮动工具条 |
| Hide     | 隐藏浮动工具条 |





# FloatingToolBarListener

浮动工具条的事件监听节点。

![image-20201127193137300](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201127193137.png)

**入口：**

| 入口名称 | 作用描述           |
| -------- | ------------------ |
| Enable   | 开始监听浮动工具条 |
| Disable  | 停止监听浮动工具条 |



**出口：**

| 出口名称      | 作用描述                                   |
| ------------- | ------------------------------------------ |
| Button ID     | 输出工具条按下的按钮ID（字符串id）         |
| SpawnPoint ID | 输出SpawnPoint子界面按下的按钮ID（整数id） |
| Sequence ID   | 输出Sequenc子界面按下的按钮ID（整数id）    |
| Cam Point ID  | 输出Cam Point子界面按下的按钮ID（整数id）  |
| TOD ID        | 输出TOD子界面按下的按钮ID（整数id）        |







# MessageBox

消息框

![image-20201127193335064](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201127193335.png)

**入口：**

| 入口名称      | 作用描述                                   |
| ------------- | ------------------------------------------ |
| Show          | 显示消息框                                 |
| Hide          | 关闭消息框（不推荐使用）                   |
| Title         | 消息框标题                                 |
| Message       | 消息框内容                                 |
| Type          | 消息框类别  （不同类型会有不同的弹出音效） |
| Modal         | 是否模态                                   |
| Output Result | 是否输出按钮结果                           |

 

**出口：**

| 出口名称      | 作用描述                           |
| ------------- | ---------------------------------- |
| Button Result | 输出对话框按钮选择结果  0-yes 1-no |







# QPushButtonBar

类似[**FloatingToolBar**](#floatingtoolbarcontroller)的一种工具条

![image-20201127194125486](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201127194125.png)

**入口：**

| 入口名称 | 作用描述       |
| -------- | -------------- |
| Show     | 显示浮动工具条 |
| Hide     | 隐藏浮动工具条 |







# SetFocus

为Launcher主窗口设定焦点，针对某些情况下点击工具条使主窗口失去焦点而创建的节点，使用该节点使主窗口重新获得焦点。

![image-20201127194444283](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201127194444.png)

**入口：**

| 入口名称 | 作用描述         |
| -------- | ---------------- |
| Set      | 为主窗口设定焦点 |