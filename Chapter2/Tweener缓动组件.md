# `Tweener`类型

继承于 [`cc.Component`](https://docs.cocos.com/creator/api/zh/classes/Component.html)

缓动组件。可以获取缓动。
是抽象类。

### 索引

##### 属性（properties）

- `tweenerTag` `String` 缓动组件的标签。
- `playOnLoad` `Boolean`是否在加载后直接播放缓动。


##### 方法

- `play` `(...any):void` 播放缓动
- `stop``():void` 停止当前的缓动
- `onLoad``():void` 当附加到一个激活的节点上或者其节点第一次激活时候调用。

##### 抽象方法

- `getTween` `(...any):cc.Tween` 外部获取缓动。
- `_getTween` `():cc.Tween` 获取内部的缓动。
- `getConsumptionTime` `():number` 获得缓动消耗的时间。

