# CompositeTweener组合缓动

继承于  [`Tweener`](Tweener缓动组件.md)

**组合缓动**通常可以拥有一个或更多的**子缓动**，**子缓动**依附的节点必须是当前节点或当前节点的子节点。

**组合缓动**将会根据属性 子缓动标签 `subTweenerTag` 来识别**子缓动**。

这些**子缓动**会根据属性 播放模式  `playmode` 按照次序执行或是间隔一段时间地执行。
**组合缓动**支持调试功能，在编辑器中调试时会以当前节点为原型生成**预览节点**，
**预览节点**会在组合缓动生命周期中的onLoad时或勾选预览结束后自动关闭的情况下在预览结束自动被删除，用户可以手动点击暂停按钮关闭调试，不需要手动删除预览节点。

是抽象类。

### 索引

##### 属性（properties）

- `tweenerTag` `String` 缓动组件的标签。
- `playOnLoad` `Boolean`是否在加载后直接播放缓动。
- `subTweeners` `Tweener[]` 子缓动数组。
- `autoClosePreview` `Boolean` 是否在预览结束时自动关闭预览节点。
- `isPreviewing` `Boolean` 是否正在预览。
- `subTweenTag` `String` 子缓动标签。
- `playMode` `PlayMode` 播放模式,sequence或interval。
- `playInterval` `Number`  播放模式为interval时的播放间隔时间
- `loop` `Boolean` 是否循环
- `block` `Boolean` 是否阻塞，阻塞将占用时间

##### 抽象属性

- `classOfSubTweener` `typeof Tweener`子缓动的类型。


##### 方法

- `play` `(...any):void` 播放缓动
- `stop` `():void` 停止当前的缓动
- `onLoad` `():void` 当附加到一个激活的节点上或者其节点第一次激活时候调用。
- `getSubTweeners` `(tweenerTag?: string): Tweener[]` 从`subTweeners`获取子缓动组件、默认获取符合子缓动标签的子缓动，也可以获取指定标签的子缓动。
- `getTween` `(...any):cc.Tween` 外部获取缓动。
- `_getTween` `():cc.Tween` 获取内部的缓动。
- `getConsumptionTime` `():number` 获得缓动消耗的时间。

