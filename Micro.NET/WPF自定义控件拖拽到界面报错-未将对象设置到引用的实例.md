#### WPF自定义控件拖拽到界面报错-未将对象设置到引用的实例

若给自定义控件注册了许多属性，那么在拖拽使用这个控件时可能会引起这个错误。原因是控件初始化时，各个属性未被显式赋值。

解决办法，给控件向外暴漏一初始化的方法，类似于这样

```
public void XXX()
{
    属性1=xxxxx;
    ...
}
```

这样，就可以正常拖拽控件使用控件了。