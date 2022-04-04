1、更改 drawable 的颜色

```java
leftDrawable.setColorFilter(leftDrawableColor, PorterDuff.Mode.SRC_ATOP);
```

2、设置 drawale 的绘制区域（调用 setCompoundDrawables 时需要设置）

```java
leftDrawable.setBounds(0, 0, leftDrawable.getIntrinsicWidth(), leftDrawable.getIntrinsicHeight());
```

3、代码设置 TextView 的 style 失效，直接设置单个 style，如单独设置背景等等