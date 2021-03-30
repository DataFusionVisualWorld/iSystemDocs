# 如何在FloatingTag中显示中文内容？

在目录**CRYENGINE\gamesdk\libs\ui**内，有名为**Config.txt**的文件。

![image-20210330190019222](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330190019.png)

#### 该文件内，编写了FTag转译字段，令FTag支持中文的显示。



 ![image-20210330190432391](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330190432.png)

#### 每一行代表一个字段，以&开始并以&结束。等号左边填入代号，等号右边填入中文或其他文字。



#### 在Sandbox内，选中Entity并编辑FTag组件的属性。修改属性Title Label，填入@+代号。

 ![image-20210330190813165](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330190813.png)

#### 此处填入的值为@Test1，那么FTag将会根据Config.txt的内容显示中文。



## 最终效果如下：

 ![image-20210330190948838](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210330190949.png)