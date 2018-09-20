## has

```
  功能简介：判断对象中是否包含路径所指定的属性
  函数名：has
  入参：obj (Object) 对象
  path	(String) 路径
  返回值：布尔值，包含返回true，反之返回false
  实现逻辑：将路径根据.分割成数组，对该数组遍历，使用hasOwnProperty递归判断
```