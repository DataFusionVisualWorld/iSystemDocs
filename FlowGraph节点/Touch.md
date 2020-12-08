# Touch相关节点

触摸屏相关功能节点。



## InitTouchManager

初始化TouchManager的节点

![image-20201130154017051](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201130154017.png)

**入口：**

| 端口 | **作用**  |
| ---- | --------- |
| Init | 初始化TEM |

**出口:**

| 端口      | **作用**       |
| --------- | -------------- |
| Result    | 返回初始化结果 |
| Succeeded | 成功时触发     |
| Failed    | 失败时触发     |







## EventListener

监听触摸屏事件的监听器

![image-20201130155527593](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201130155527.png)

**入口：**

| 端口    | **作用** |
| ------- | -------- |
| Enable  | 开始监听 |
| Disable | 停止监听 |

**出口:**

| 端口         | **作用**                                                 |
| ------------ | -------------------------------------------------------- |
| Contact      | 输出屏幕触点数量                                         |
| On Down      | 无触点变化到有触点时触发，也就是按下不松开只会触发一次。 |
| On Move      | 有触点时持续触发                                         |
| On Completed | 屏幕失去所有触点时触发                                   |
| Start        | OnDown触发时触点的屏幕坐标                               |
| Current      | 持续输出当前触点位置                                     |
| Translation  | 输出触点位移量Delta                                      |
| Scale Factor | 输出缩放因数，平常值为1                                  |
| Rotation     | 输出多点触摸旋转角度Delta                                |









## PlayerController

基于触屏的Player控制器

![image-20201130155812023](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201130155812.png)

**入口:**

| 端口               | **作用**           |
| ------------------ | ------------------ |
| Enable             | 启用               |
| Disable            | 关闭               |
| Speed              | 设定行进速度       |
| Rotate Sensitivity | 设定镜头转向灵敏度 |
| Debug              | 开启Debug模式      |