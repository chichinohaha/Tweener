# TweenInfo缓动数据

**缓动数据**（TweenInfo）能够获取创造复杂缓动所需要的所有信息，如持续时间、变化曲线(easing)等。
是抽象类。

### 索引

##### 属性（properties）

- `id` `Number` 缓动数据的id。
- `Name` `String`缓动数据的名称。


##### 方法

- `getConsumptionTime` `():number` 获取消耗的时间
- `parseSerializedData` `(data:any):void` 解析数据并且应用数据到自身。

##### 抽象方法

- `copy` `(serialize?: boolean): TweenInfo` 深拷贝并根据参数判断是否序列化。

