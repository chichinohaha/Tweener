# BezierByComplexCell组件参考

**BezierByComplexCell**组件能够获取目标为当前节点的**沿着路径点进行相对的贝塞尔曲线**的缓动。

![image-20201108130922058](https://raw.githubusercontent.com/chichinohaha/Tweener/gh-pages/docs/Sources/bezierBy.png)

## 组件的选项

| 选项           | 说明                          |
| -------------- | ----------------------------- |
| 加载完成后播放 | 生命周期onLoad时自动播放缓动  |
| 正在编辑       | 是否开启gizmo以对当前数据编辑 |

## 组件的属性

| 属性         | 说明             |
| ------------ | ---------------- |
| 缓动组件标签 | 用于标识的标签   |
| Asset        | 数据集的json资源 |

## 贝塞尔缓动数据的选项

| 选项     | 说明                   |
| -------- | ---------------------- |
| 是否阻塞 | 是否占用时间           |
| 循环     | 是否无限重复这个动作   |
| 首尾相接 | 是否将终点与起始点相连 |

## 贝塞尔缓动数据的属性

| 属性       | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
| 路径信息   | 四维向量数组，<br />四维向量存储的信息为：<br />x:x坐标<br />y:y坐标<br />z:到下一个点的路径长度<br />w：到下一个点的时间 |
| 控制点信息 | 二维向量数组，<br />二维向量存储的信息为<br />x:x坐标<br />y:y坐标 |
| 整体速度   | 多个贝塞尔缓动的平均速度                                     |
| 名称       | 缓动数据的名称                                               |
| ID(只读)   | 缓动数据的ID                                                 |



**BezierByComplexCell**组件在勾选正在编辑时会使用super-gizmo插件渲染gizmo，在视图界面能够直观的编辑路径信息和控制点信息。

![image-20201108133529124](https://raw.githubusercontent.com/chichinohaha/Tweener/gh-pages/docs/Sources/bezierByExample.png)

#### 操作说明（就像钢笔工具一样）

请确保安装了[super-gizmo](https://store.cocos.com/#/resources/detail/2513)插件，

依次选中编辑器选项中的扩展/超级gizmo/打开Gizmo配置界面

![image-20201108150734178](https://raw.githubusercontent.com/chichinohaha/Tweener/gh-pages/docs/Sources/super-gizmo.png)

在该界面设置矩形的显示宽高以及触控区域的宽高。

在super-gizmo的触控矩形区域内点击即可生成路径，
可鼠标左键拖拽点，按着ctrl点击路径点可删除路径点。
按着alt拖拽路径点可同时调整两个控制点。
按着alt拖拽控制点可修改单个控制点。

## 演示

![image-20201108150734178](https://raw.githubusercontent.com/chichinohaha/Tweener/gh-pages/docs/Sources/tweener-bezierBy.gif)