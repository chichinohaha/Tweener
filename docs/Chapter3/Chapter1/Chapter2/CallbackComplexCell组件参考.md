# CallbackComplexCell组件参考

**CallbackComplexCell**组件能够获取目标为当前节点的**间隔地调用回调**的缓动。

![image-20201108195502627](https://raw.githubusercontent.com/chichinohaha/Tweener/gh-pages/docs/Sources/callbackComplexCell.png)

## 组件的选项

| 选项           | 说明                         |
| -------------- | ---------------------------- |
| 加载完成后播放 | 生命周期onLoad时自动播放缓动 |

## 组件的属性

| 属性         | 说明             |
| ------------ | ---------------- |
| 缓动组件标签 | 用于标识的标签   |
| Asset        | 数据集的json资源 |

## 回调缓动数据的属性

| 属性     | 说明               |
| -------- | ------------------ |
| 名称     | 缓动数据的名称     |
| ID(只读) | 缓动数据的ID       |
| 回调数组 | 回调的数组         |
| 回调间隔 | 每个回调的间隔时间 |

