# FloatingTag变种——DBF数据库查询版本

使用方法与原版FloatingTag基本一致，组件名称为**Floating Tag Dbf**

![image-20210727151147119](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210727151147.png)

## 设置组件属性

![image-20210729161045564](https://gitee.com/Azureusbin/pic-lib/raw/master/imags/20210729161045.png)

| 属性名称         | 作用描述                                                     |
| ---------------- | ------------------------------------------------------------ |
| Query Field      | 指定查询的字段，查询关键字为该Entity的名称                   |
| Title Field      | 指定结果的字段，将查询得到的记录对应的字段用作FTag的标题     |
| Style name       | 指定FTag样式，即FLASH内导出的对应元件名称                    |
| GroupID          | 设定该FTag所属的Group ID，方便批量管理                       |
| Display Distance | 该FTag的显示距离，超出距离会被隐藏                           |
| Enable Scale     | 启用或禁止缩放                                               |
| Scale Factor     | 缩放系数，系数越大缩放的越慢                                 |
| Max Size         | 限定FTag的最大显示大小，100表示与原生尺寸一致。              |
| Min Size         | 限定FTag的最小显示大小，距离屏幕越远则FTag大小越接近**Min Size** |
| Attach to Camera | 启用后，FTag不在屏幕内时，会在屏幕边缘显示（注意性能问题）   |
