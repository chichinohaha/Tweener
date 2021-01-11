# 组合缓动组件参考

**组合缓动**通常可以拥有一个或更多的**子缓动**，**子缓动**依附的节点必须是当前节点或当前节点的子节点。

**组合缓动**将会根据属性 子缓动标签 `subTweenerTag` 来识别**子缓动**。
不同级别的**组合缓动**的属性 子缓动类型 `classOfSubTweener` 不一样，笔者按照生物学的概念命名，目前内置以下组合缓动：

- 组织组合缓动：子缓动类型为细胞缓动。
- 器官组合缓动：子缓动类型为组织组合缓动。
- 系统组合缓动：子缓动类型为器官组合缓动。
- 生命组合缓动：子缓动类型为系统组合缓动。
- 种群组合缓动：子缓动类型为生命组合缓动。

这些**子缓动**会根据属性 播放模式  `playmode` 按照次序执行或是间隔一段时间地执行。
**组合缓动**支持调试功能，在编辑器中调试时会以当前节点为原型生成**预览节点**，
**预览节点**会在组合生命缓动周期中的onLoad时或勾选预览结束后自动关闭的情况下在预览结束自动被删除，用户可以手动点击暂停按钮关闭调试，不需要手动删除预览节点。

你将会了解以下组合缓动组件：

- [组织组合缓动组件参考](./组织组合缓动组件.md)
- [器官组合缓动组件参考](./器官组合缓动组件.md)
- [系统组合缓动组件参考](./系统组合缓动组件.md)
- [生命组合缓动组件参考](./生命组合缓动组件.md)
- [种群组合缓动组件参考](./种群组合缓动组件.md)
