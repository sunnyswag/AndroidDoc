目前看来，只存在一种方式，那就是：
```Kotlin
LayoutInflater.from(parent.context).inflate(R.layout.references_list_item, parent, false)
```
其他的都是在此包裹了一层，如：`Activity` 的 `setContentView()`
```Java
@Override
public void setContentView(int resId) {
    ensureSubDecor();
    ViewGroup contentParent = mSubDecor.findViewById(android.R.id.content);
    contentParent.removeAllViews();
    LayoutInflater.from(mContext).inflate(resId, contentParent);
    mAppCompatWindowCallback.getWrapped().onContentChanged();
}
```