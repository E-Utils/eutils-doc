## isElement

```
  函数名：isElement
  入参： element(Element): 节点；
  返回值：true/false
  实现逻辑：首先判断是否为unll,undefined,false,0等，如果都不是，则判断nodeType是否等于1，都满足则返回true，否则返回false；
```