# 如何使用FloatingTag？

要使用FTag，需为Entity添加FloatingTag组件。



## 第一步，添加FloatingTag组件

选中Entity，在属性栏中添加名为Floating Tag的Component。

 ![image-20210330182331051](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330182331.png)



## 第二步，设置FTag属性

在Entity属性栏中，可以设置FTag组件的属性。

 ![image-20210330182611943](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330182612.png)



| 属性名称         | 作用描述                                      |
| ---------------- | --------------------------------------------- |
| Title label      | 该FTag显示的文本                              |
| Style name       | 指定FTag样式，即FLASH内导出的对应元件名称     |
| GroupID          | 设定该FTag所属的Group ID，方便批量管理        |
| Can Trigger      | 勾选后的该FTag可被鼠标点击，并发出相应UIEvent |
| Display Distance | 该FTag的显示距离，超出距离会被隐藏            |



## 第三步，显示或隐藏FTag

可使用FlowGraph节点[Controller](..\FlowGraph节点\FloatingTag.md#Controller)，输入相应的GroupID，进行显示隐藏的操作。