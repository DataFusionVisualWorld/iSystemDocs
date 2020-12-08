# MeasureTools

该节点用于启用测量功能。*****代码内部指定**Delete键**为删除选中的测量结果，与端口**Delete Select**等效

![image-20201130145546548](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201130145553.png)

**入口：**

| 入口名称      | 作用描述               |
| ------------- | ---------------------- |
| Create_Line   | 创建线段进行长度测量   |
| Create_Shape  | 创建多边形进行面积测量 |
| Allow_Select  | 允许选择创建的测量体   |
| Delete_Select | 删除当前选择的测量体   |
| Delete_All    | 删除所有测量体         |

 

**出口：**

| 出口名称 | 作用描述 |
| -------- | -------- |
| Log      | 暂无作用 |