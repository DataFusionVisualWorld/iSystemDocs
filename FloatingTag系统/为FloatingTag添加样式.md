# 为FloatingTag添加新的样式

**FloatingTag**核心文件为**FT_HUD.swf**，若想添加样式，需要编辑**FT_HUD.fla**。

![image-20210330191256099](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330191256.png)



## FLASH CS6

新建元件，勾选**为ActionScript导出**，此处**标识符**与FTag组件的**Style name**属性相对应。

 ![image-20210330191505027](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330191505.png)



在元件的内部，新建一个**动态文本框**，将其命名为**TT**。该文本框将会显示FTag组件**Title Label**的内容。

 ![image-20210330191911001](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330191911.png)



保存工程文件，发布swf文件，即可使用新的FTag样式了。

 ![image-20210330192127967](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330192128.png)