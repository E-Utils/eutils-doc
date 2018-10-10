## scrollTop

```
  函数名：scrollTop
  入参： elem: 需要获取指定DOM元素对象
        target: 滚动条滚动至目标位置
  返回值：默认返回滚动条所处位置（number）；若设置target值，将设置滚动条位置至target
  实现逻辑：元素和文档、窗口都具有scroll值，因获取方式不同，将文档、窗口为一类（window.pageYOffset），元素为一类（elem.scrollTop）获取具体值；
  滚动条滚动位置通过scrollTo方法达到移动滚动条
```