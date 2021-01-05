# BlockSystem相关节点

用于**BlockSystem**的节点。



## AddMission

添加直接加载任务。（在系统载入场景后会执行**直接加载任务（Direct Load Mission）**，直接加载地块，会引起卡顿，直至加载完成）

![image-20210106033249628](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210106033256.png)

| 入口     | 用途                       |
| -------- | -------------------------- |
| Load     | 加载                       |
| Location | 用于检测加载地块的基准点。 |







## Listener

**直接加载任务（Direct Load Mission）**的事件监听器。可以监听到**加载开始、加载进度和加载结束**。

![image-20210106034114802](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210106034114.png)

| 出口                | 用途                                                  |
| ------------------- | ----------------------------------------------------- |
| On Mission Start    | 当任务开始时，会触发此端口                            |
| Mission Progress    | 任务加载进度，输出的数值范围为（0~1000），代表0%-100% |
| On Mission Complete | 当任务结束时，会触发此端口                            |