# Camera类节点

这里有**iSystem**所有**Camera**分类下的节点介绍。



## BlendToPlayerView

此节点可以将Camera从当前视角过渡到游戏原生的Player视角上。

![image-20201121212234704](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121212241.png)

| 端口         | 用途                                                         |
| ------------ | ------------------------------------------------------------ |
| Set          | 设置当前视角为Player视角，并触发过渡效果                     |
| Blend Option | 镜头过渡选项**NoBlend**=无过渡，**CurrentView**=从当前视角过渡到RTSCamera，**FromEntity**=从Entity矩阵过渡到Player视角 |
| From Entity  | 输入EntityId，获取其世界空间矩阵                             |







## GISCameraManager

该节点用于管理GIS摄像机。

![image-20201121212707546](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121212707.png)

**入口：**

| 入口名称        | 作用描述                                                     |
| --------------- | ------------------------------------------------------------ |
| Choose Entity   | 指定Camera实体，开启GIS摄像机后视角绑定到该实体上            |
| Activate        | 启用GIS摄像机                                                |
| Deactivate      | 关闭GIS摄像机                                                |
| Toggle_2D_Mode  | 切换/关闭2D相机模式                                          |
| Zoom_In         | 视角前进                                                     |
| Zoom_Out        | 视角后退                                                     |
| Rotate_Left     | 视角向左旋转                                                 |
| Rotate_Right    | 视角向右旋转                                                 |
| Speed_Factor    | 摄像机移动速度倍率                                           |
| Altitude_Limits | 3维数组，第1位表示最低高度，第2位表最大高度，第3表是否启用功能 |

 

**出口：**

| 出口名称 | 作用描述             |
| -------- | -------------------- |
| Log      | GIS摄像机关闭则输出1 |







## GetViewTransform

获取当前激活的Camera的信息。

![imags-20201121213000](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121213000.png)

**入口：**

| 入口名称 | 作用描述 |
| -------- | -------- |
| Get      | 获取信息 |

 

**出口：**

| 出口名称 | 作用描述                  |
| -------- | ------------------------- |
| Pos      | 输出当前Camera的位置信息  |
| Pitch    | 输出当前Camera的Pitch信息 |
| Yaw      | 输出当前Camera的Yaw信息   |
| Roll     | 输出当前Camera的Roll信息  |
| Dir      | 输出当前Camera所指的方向  |
| Fov      | 输出当前Camera的Fov信息   |







## CameraPointAroundPerspective

绑定一个物体、设定一个中心物体，形成对点环视结构。

![image-20201121213643111](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121213643.png)

**入口：**

| 入口名称         | 作用描述                                                     |
| ---------------- | ------------------------------------------------------------ |
| Choose_Entity    | 设定一个实体，用于围绕中心物体，正常情况下应该绑定一个Camera |
| Center_Object_Id | 输入实体的EntityId来指定中心物体                             |
| Sensitivity_X    | 设定x轴灵敏度                                                |
| Sensitivity_Y    | 设定y轴灵敏度                                                |
| Fov              | 设定摄像机Fov                                                |
| Pitch_Range      | 3维数组，前两位分别表示Pitch最小角度和最大角度               |
| Distance_Setting | 3维数组，前两位分别表示最小距离和最大距离                    |
| Roll_Speed       | Roll速度设定                                                 |
| Blend            | 平滑过程                                                     |
| Dynamic_Update   | 动态更新移动                                                 |
| Enable           | 启动节点                                                     |
| Disable          | 关闭节点                                                     |
| Lock             | 锁定移动                                                     |
| Unlock           | 解锁移动                                                     |







## RTSCamera

属于新Camera系统的一个Camera类型。

![image-20201121213824611](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121213824.png)

| 入口名称     | 作用描述                                                     |
| ------------ | ------------------------------------------------------------ |
| Activate     | 激活                                                         |
| Deactive     | 反激活，激活其他Camera前无需触发，如需返回PlayerView则触发   |
| Plane Height | RTS的基准平面高度                                            |
| Fov          | 视场角度                                                     |
| Blend Option | 镜头过渡选项NoBlend=无，CurrentView=从当前视角过渡到RTSCamera，FromEntity=从Entity矩阵过渡到RTSCamera |
| From Entity  | 输入EntityId，获取其世界空间矩阵                             |



#### *RTSCamera的控制台参数

| 命令                     | 作用                      |
| ------------------------ | ------------------------- |
| RTSCamera.ZoomFactor     | 镜头距离缩放因数          |
| RTSCamera.FovFactor      | 镜头Fov缩放因素           |
| RTSCamera.WheelFactor    | 镜头距离-滚轮缩放因素     |
| RTSCamera.PanMoveFactorX | 镜头移动灵敏度X轴         |
| RTSCamera.PanMoveFactorY | 镜头移动灵敏度Y轴         |
| RTSCamera.RotateFactorX  | 镜头旋转灵敏度X轴         |
| RTSCamera.RotateFactorY  | 镜头旋转灵敏度Y轴         |
| RTSCamera.MinPitchAngle  | 镜头俯仰角的最小角度      |
| RTSCamera.MaxPitchAngle  | 镜头俯仰角的最大角度      |
| RTSCamera.DebugMode      | 调试模式-0为关闭，1为开启 |



#### *使用例子

1. 相机从指定位置过渡到RTSCamera

   ![image-20201121214251920](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121214251.png)


2. 动态修改Plane Height

   ![image-20201121214306546](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121214306.png)









## SetGISCameraTransform

设置当前[GISCamera](#giscameramanager)的视角位置和旋转状态。

![image-20201121214628538](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121214628.png)



**入口：**

| 入口名称 | 作用描述                 |
| -------- | ------------------------ |
| Set      | 把当前数据设定到Camera上 |
| Position | 位置信息                 |
| Rotation | 旋转信息                 |







## CameraSpinder

将Camera实体绑定到目标实体上，并能旋转自身。

![image-20201121215048109](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201121215048.png)

**入口：**

| 入口名称        | 作用描述                                       |
| --------------- | ---------------------------------------------- |
| Choose_Entity   | 设定一个实体，用于绑定到目标实体上             |
| Sensitivity_X   | 设定x轴灵敏度                                  |
| Sensitivity_Y   | 设定y轴灵敏度                                  |
| Fov             | 设定摄像机Fov                                  |
| Pitch_Range     | 3维数组，前两位分别表示Pitch最小角度和最大角度 |
| Blend           | 平滑过程                                       |
| Rotate_Target   | 是否连同Target一起旋转                         |
| Target          | 输入作为目标的实体的EntityId                   |
| Position_Offset | 绑定位置的偏移量                               |
| Enable          | 启动节点                                       |
| Disable         | 关闭节点                                       |
| Lock            | 是否锁定移动                                   |