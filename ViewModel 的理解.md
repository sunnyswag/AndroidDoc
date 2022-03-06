1、一种数据存储和更新的方式，视图层负责接收数据更新的信息，然后改变展示即可，不用关注数据更新的具体逻辑。或者视图层更新更新数据其他地方可以
2、ViewModel 的作用范围，是根据传入的 Context 决定的。如果传入的是 Activity，那么 ViewModel 的数据作用域为其下所有的 Fragment。如果传入的是 Fragment，那么 ViewModel 的数据作用域为其下所有的 Fragment。传入的如果是同一个 context，那么获取的是同一个 ViewModel 对象（单例）

```Java
// ViewModelProvider 中可以传入 Activity 也可以是 Fragment，参数为 ViewModelStoreOwner，可以很好的理解了，ViewModel的所有者
viewModel = new ViewModelProvider(this).get(ListViewModel.class);

// 一般直接传入 viewLifecycleOwner 就好了，只在当前 view 可用的生命周期下观察
viewModel.referenceSelected.observe(viewLifecycleOwner)
```