## 在 UI 线程中执行

`View.post()` 和 `Activity.runOnUiThread` 都是放在 UI 线程中执行，只不过前者会放在消息队列中，等 View 真正初始化之后执行，而后者会立即执行



https://stackoverflow.com/questions/13840007/what-exactly-does-the-post-method-do

https://stackoverflow.com/questions/10558208/android-whats-the-difference-between-activity-runonuithread-and-view-post

