#### 回收站重命名后无法再通过修改`LocalizedString`修改回收站的名称

原因是重命名后优先使用重命名后的文本当作回收站的名称而不是`LocalizedString`规定的值。

解决方法：

注册表编辑器中查找重命名后的回收站的名称。找到后把它清空。然后重新修改`LocalizedString`的值就行了。