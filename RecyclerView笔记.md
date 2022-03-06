### 如何创建一个 RecyclerView
1. [官方教程](https://developer.android.com/guide/topics/ui/layout/recyclerview)写的非常棒，可以参照这个来
2. 值得注意的是，需要加上 `recyclerView.layoutManager = LinearLayoutManager(this)`，不然不会调用 `Adapter` 中的 `onBindViewHolder()` 方法，也就不会有数据塞进去