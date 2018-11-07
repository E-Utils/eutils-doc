## getStylePrefix

```
  函数名：getStylePrefix
  入参： propertyKey(String): 需要获取前缀的样式，如 'transform'
        isConcat(Boolean): 前缀和样式是否拼接，默认为true
  返回值：样式前缀/样式前缀+样式值 如：-ms-transform
  实现逻辑：使用document.body.style检测当前环境是否支持原生支持参数样式，如若支持，并且isConcat为true，则返回原始参数，如果不支持，则返回空字符春
```