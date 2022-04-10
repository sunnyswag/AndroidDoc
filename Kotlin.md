### 变量的初始化
* Kotlin 变量的初始化会放在构造函数中
* 父类的 public 方法无法直接引用到，必须放在转译后的方法里面，如：放在 init 代码块中（其实自己想想，这也非常合乎逻辑）




### 关键字
* init：该部分的代码会放在主构造函数中执行



### 构造函数

正常的写法：

```kotlin
// 此时 context 变量只能在构造函数(init 代码块)中使用

class TestImageView(context: Context): AppCompatImageView(context) {}
```

将变量声明为 val 或 var 的写法：

```kotlin
// 此时 size 变量可以在其他地方使用到，而 context 只能通过父类的 get 方法获取到(如果有的话)

class TestImageView(context: Context, val size: Int): AppCompatImageView(context) {}
```

实现父类的多个构造函数(在自定义 View 的时候要用到)：

```kotlin
// 这个时候使用 super 关键字，而且没办法在 SquareImageView 处构建主构造函数

class SquareImageView: AppCompatImageView {

    constructor(context: Context) : super(context) {}

    constructor(context: Context, attrs : AttributeSet) : super(context, attrs) {}

    constructor(context: Context, attrs: AttributeSet, defStyleAttr: Int): super(context, attrs, defStyleAttr) {}
```

使用 this 关键字：



#### Kotlin 入门教程

https://www.jianshu.com/p/2e0746c7d4f3

