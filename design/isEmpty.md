## isEmpty

```
  功能简介：判断目标是否为空，包括null/undefined/0/''/空迭代器对象/{}/[]
  函数名：isEmpty
  入参：target (Any) 目标
  path	(String) 路径
  返回值：布尔值，空返回true，反之返回false
  实现逻辑：先将target转为布尔值判断，若为false直接返回；然后依次判断是否为空数组/空迭代器对象/空对象，若都不是返回false
```