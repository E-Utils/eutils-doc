## position

```
  函数名：position
  入参： elem: 需要获取指定DOM元素对象
        type: 需要获取的left|top
  返回值： 默认返回{top, left}, 根据type，确定返回left|top
  实现逻辑：通过元素自身属性offsetTop|offsetLeft
```