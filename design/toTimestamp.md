## toTimestamp

```
  函数名：toTimestamp
  入参： date(date | string | number): 要转换的时间；
  返回值：时间戳
  实现逻辑：将参数转换成Date对象后格式化成
  eg:
    toTimestamp(new Date());
    // => 1536659540425;

    toTimestamp('2018-09-09');
    // => 1536451200000;

    toTimestamp(1536422400000);
    // => 1536422400000
```