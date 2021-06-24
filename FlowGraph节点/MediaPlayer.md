# Mediaplayer相关节点

用于**MediaPlayer系统**的节点。



## GlobalVolume

用于控制播放系统的总音量，可以通过设置为0达到所有播放静音的效果，设置为1恢复正常。

![image-20210624164730847](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210624164737.png)

| 入口   | 用途                            |
| ------ | ------------------------------- |
| Set    | 触发设置                        |
| Volume | 用于设置的音量数值，取值范围0~1 |







## PlayerVolume

为单个播放器设置音量，**注意：最终音量=全局音量*个体音量**

![image-20210624164948705](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210624164948.png)

| 入口   | 用途                            |
| ------ | ------------------------------- |
| ID     | 播放器ID                        |
| Set    | 触发设置                        |
| Volume | 用于设置的音量数值，取值范围0~1 |





## TexturePlayer

贴图播放器，可以在指定的贴图上播放多媒体。这个贴图可以用在材质上。

![image-20210624171237519](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210624171237.png)

| 入口         | 用途                                                     |
| ------------ | -------------------------------------------------------- |
| Play         | 开始播放指定文件，且从头开始或从Start Pos开始            |
| Pause        | 暂停播放                                                 |
| Resume       | 从暂停播放中恢复                                         |
| Stop         | 停止播放                                                 |
| URL          | 指定多媒体文件的路径，可以是file、rtsp和rtmp等协议       |
| Texture Name | 贴图名称，必须以$开头                                    |
| Loop         | 循环播放开关                                             |
| Async Load   | 异步加载文件或串流，不会阻塞主线程，一般用于加载网络串流 |
| Set Range    | 指定播放范围的开关                                       |
| Start Pos    | 开始位置，使用0~1表示                                    |
| End Pos      | 结束位置，使用0~1表示                                    |

*注意：Start Pos是由指定时间除以总时长得来的一个数，因此数值在0~1之间。



| 出口     | 用途                     |
| -------- | ------------------------ |
| Started  | 播放器开始播放时触发     |
| Paused   | 播放器暂停时触发         |
| Resumed  | 播放器从暂停中恢复时触发 |
| Stopped  | 播放器停止播放时触发     |
| Finished | 播放器播放完毕时触发     |



## ViewportPlayer

使用**视口（Viewport）播放器**播放指定文件，播放画面会呈现在CryEngine的渲染窗口中。

![image-20210624171214709](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210624171214.png)

| 入口       | 用途                                                     |
| ---------- | -------------------------------------------------------- |
| Play       | 开始播放指定文件，且从头开始或从Start Pos开始            |
| Pause      | 暂停播放                                                 |
| Resume     | 从暂停播放中恢复                                         |
| Stop       | 停止播放                                                 |
| URL        | 指定多媒体文件的路径，可以是file、rtsp和rtmp等协议       |
| Loop       | 循环播放开关                                             |
| Play Audio | 是否播放音轨，非静音方式，可能导致视频播放长度有细微变化 |
| Async Load | 异步加载文件或串流，不会阻塞主线程，一般用于加载网络串流 |
| Set Range  | 指定播放范围的开关                                       |
| Start Pos  | 开始位置，使用0~1表示                                    |
| End Pos    | 结束位置，使用0~1表示                                    |

*注意：Start Pos是由指定时间除以总时长得来的一个数，因此数值在0~1之间。



| 出口     | 用途                     |
| -------- | ------------------------ |
| Started  | 播放器开始播放时触发     |
| Paused   | 播放器暂停时触发         |
| Resumed  | 播放器从暂停中恢复时触发 |
| Stopped  | 播放器停止播放时触发     |
| Finished | 播放器播放完毕时触发     |

