# CompolexCell复杂细胞

继承于 [CellTweener](CellTweener细胞缓动.md)

复杂细胞缓动组件。可以获取缓动。

是抽象类。
**细胞缓动**是最低层的缓动，它们不会拥有子缓动。**细胞缓动**是最强大的缓动类型，它们是真正让你的动作做具体事情的基础元素。
**复杂缓动细胞**最主要的一个属性就是 **当前的缓动数据**`currentTweenInfo`其根据**当前的缓动数据**`currentTweenInfo`生成缓动。可将**缓动数据**（[`TweenInfo`](TweenInfo缓动数据.md) ）存储在属性**数据集** `tweenInfos`中。可在**属性检查器**对**数据集**进行<u>搜索</u>和<u>删除</u>的操作。**复杂缓动细胞**拥有对**数据集** <u>本地存储</u>和<u>读取</u>的能力。

### 索引

##### 属性（properties）

- `tweenerTag` `String` 缓动组件的标签。
- `playOnLoad` `Boolean`是否在加载后直接播放缓动。
- `currentTweenInfo` [`TweenInfo`](TweenInfo缓动数据.md) 当前缓动数据。
- `tweenInfos` [`TweenInfo`](TweenInfo缓动数据.md) []` 缓动数据集。
- `showTweenInfos` `Boolean` 是否在**属性检查器**显示缓动数据集。
- `search` `String` 搜索数据集的关键词。
- `spliceTweenInfo` `String` 删除数据集的关键词。
- `asset` [`cc.JsonAsset`](https://docs.cocos.com/creator/api/zh/classes/JsonAsset.html?h=json) 存储数据集的json资源。

**抽象属性**

- `classOfInfo`:`typeof TweenInfo`缓动数据的类型

##### 方法

- `play` `(...any):void` 播放缓动
- `stop` `():void` 停止当前的缓动
- `onLoad` `():void` 当附加到一个激活的节点上或者其节点第一次激活时候调用。
- `getTween` `(...any):cc.Tween` 外部获取缓动的方法。
- `getConsumptionTime` `():number` 获得缓动消耗的时间。
- `checkDataValidity` `():boolean` 校验json资源是否合法。
- `checkTweenInfoValidity` `():boolean` 校验当前缓动数据是否合法。
- `getDefaultWarnTween` `():cc.Tween` 获取默认提示错误的缓动。
- `loadAsset` `():void` 读取属性`asset`的数据集到属性 `tweenInfos`。
- `saveAsset` `():void` 将属性`tweenInfos`本地存储成json资源。
- `getSerializedData` `():any[]` 获取属性`tweenInfos`序列化后的数据。
- `parseSerializedData` `():void` 将数据反序列化并赋值给属性 `tweenInfos`。
- `findTweenInfo` `(searchKey: string | number,copy:boolean=true): TweenInfo` 根据id或者名称搜索数据集的信息，并根据参数`copy`返回数据本身或者数据的拷贝。
- `setTweenInfo` `(searchKey: string | number): TweenInfo`  根据id或者名称搜索数据集的信息，若搜索成功则替换当前数据 `currentTweenInfo` 。

##### 抽象方法

- `_getTween``():cc.Tween` 获取内部的缓动。