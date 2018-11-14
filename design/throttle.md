## throttle

```
  功能简介：函数节流
  函数名：throttle
  入参：func (Function) 函数
  wait	(Number) 等待的毫秒数
  返回值：Function对象，可以调用该对象的cancel方法取消延时调用
  实现逻辑：在debounce方法的实现基础上添加定时，定时满时主动执行入参函数
```