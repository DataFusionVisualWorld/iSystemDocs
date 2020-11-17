# Overview

*在Sandbox内，新增一组下拉菜单‘Block’。

<img src="https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201117155156.png" alt="image-20201117155156422" align="left" />

<font color=red><b>*在Block system未初始化时，部分功能会被锁定。</b></font>



### Sort Selection To ‘Block Layers’

将选中的物体，自动分层到对应的Block图层内，如果图层不存在则创建。

<img src="https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201117171553.png" alt="1" style="zoom:67%;" align="left"/>

选中需要处理的物体，点选**Sort Selection To ‘Block Layers’**即可开始处理，处理前后对比图：
<center>
<img src="https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201117171558.png"/>
<img src="https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201117171559.png"/>
</center>



### Clean up ‘Block Layers’

删除Block相关的空图层，包含物体的图层和非区块对应图层不会被清除。
<center>
<img src="https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201117172350.png"/>
<img src="https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20201117172350.png"/>
</center>


### Export blocks files

导出Block相关图层到内部指定的目录（*/Blocks），并生成Block.conf配置文件。

 

### Convert Selection To Entity

将选择的**Brush**物体转换为**Entity**物体

 

### Convert Selection To Brush

将选择的**Entity**物体转换为Brush物体