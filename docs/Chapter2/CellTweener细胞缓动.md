# CellTweener细胞缓动

继承于 [Tweener](Tweener缓动组件.md)

细胞缓动组件。可以获取缓动。

是抽象类。
**细胞缓动**是最低层的缓动，它们不会拥有子缓动。**细胞缓动**是最强大的缓动类型，它们是真正让你的动作做具体事情的基础元素。

### 索引

##### 属性（properties）

- `tweenerTag` `String` 缓动组件的标签。

- `playOnLoad` `Boolean`是否在加载后直接播放缓动。

  

##### 方法

- `play` `(...any):void` 播放缓动
- `stop` `():void` 停止当前的缓动
- `onLoad` `():void` 当附加到一个激活的节点上或者其节点第一次激活时候调用。
- `getTween` `(...any):cc.Tween` 外部获取缓动的方法。
- `getConsumptionTime` `():number` 获得缓动消耗的时间。

##### 抽象方法

- `_getTween` `():cc.Tween` 获取内部的缓动。