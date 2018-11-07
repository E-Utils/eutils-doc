## get

```
  功能简介：获取对象中路径所指定的属性
  函数名：get
  入参：obj (Object) 对象
  path	(String) 路径
  defaultValue (Any) 当属性不存在时返回的默认值
  返回值：Any
  实现逻辑：将路径根据.分割成数组，对该数组遍历，使用hasOwnProperty递归判断
```