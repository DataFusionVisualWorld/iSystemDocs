# FloatingTag节点

浮标点系统的相关节点。



## Controller

FloatingTag控制器节点

![image-20210330180807808](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330180814.png)

**入口：**

| 入口名称             | 作用描述                                   |
| -------------------- | ------------------------------------------ |
| Group Id             | GroupID选择器，-1为选择所有Group           |
| Show                 | 显示选择的Group                            |
| Hide                 | 隐藏选择的Group                            |
| Hide All Except This | 隐藏除了被选择的Group，并显示所选择的Group |
| Hold                 | 隐藏FTag，但不清空当前的Group显示状态      |
| Unhold               | 显示FTag，恢复Hold前的Group显示状态        |