# Date
* ## dateFormat(date, format)</br>
  将日期按照指定格式格式化并返回格式化后的日期。

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    date(number | Date): 预格式化的日期。
    format(string): 日期格式。
  ```
  <b>Returns</b>
  ```
    (string): 返回格式化后的日期。
  ```
  <b>Example</b>
  ```
    EUtils.dateFormat(1531643785284, 'yyyy-MM-dd');
    // => '2018-07-15';
  ```

# Url
* ## setUrlParam(params, originUrl)<br />
  向当前Url或目标Url添加参数，originUrl不传则默认使用当前Url

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    params(object)：需要添加的参数对象，如果key值再url中已存在，则会进行替换
    originUrl(string)：被操作的Url地址，不传则默认使用window.location.href
  ```
  <b>Returns</b>
  ```
    (string)：返回拼接好后的字符串
  ```
  <b>Example</b>
  ```
    EUtils.setUrlParam({
        id: 2,
        name: 3
    }, 'http://www.ewt360.com?id=1');
    // => http://www.ewt360.com?id=2&name=3
  ```
      
* ## getUrlParam(key, originUrl)<br />
  从当前Url或目标Url获取参数，originUrl不传则默认使用当前Url

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    key(string)：需要获取的参数key
    originUrl(string)：被操作的Url地址，不传则默认使用window.location.href
  ```
  <b>Returns</b>
  ```
    (string)：返回查找到的参数值value,如果未找到则返回空字符串
  ```
  <b>Example</b>
  ```
    EUtils.getUrlParam('id', 'http://www.ewt360.com?id=1');
    // => 1
  ```

# String
* ## repalce(str, pattern, replacement)<br />
  将str字符串中指定的pattern字符替换成replacement字符，惰性匹配，匹配到一个就不会匹配后面的

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    str： 原始串,
    pattern：要替换的字符串或正则,
    replacement：替换的目标字符串
  ```
  <b>Returns</b>
  ```
    (string)：返回替换后的字符串
  ```
  <b>Example</b>
  ```
    replace('hello world', /o/, 'hi')
    // => 'hellhi world'
  ```

* ## repalceAll(str, sourcement, replacement)<br />
  将str字符串中指定的sourcement字符全都替换成replacement字符

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    str： 原始串,
    sourcement：要替换的字符串或正则,
    replacement：替换的目标字符串
  ```
  <b>Returns</b>
  ```
    (string)：返回替换后的字符串
  ```
  <b>Example</b>
  ```
    replaceAll('hello wOrld', /o/i, 'hi')
    // => 'hellhi whirld'
  ```

* ## toLower(str)<br />
  将str字符串大写全部转成小写

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    str： 原始串
  ```
  <b>Returns</b>
  ```
    (string)：返回小写后的字符串
  ```
  <b>Example</b>
  ```
    toLower('hellO-wOrld')
    // => 'hello-world'
  ```

* ## toUpper(str)<br />
  将str字符串小写全部转成大写

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    str： 原始串
  ```
  <b>Returns</b>
  ```
    (string)：返回大写后的字符串
  ```
  <b>Example</b>
  ```
    toUpper('hello-world')
    // => 'HELLO-WORLD'
  ```

* ## trim(str, chars)<br />
  将str字符串前后空格

  <b>Since</b>
  ```
    1.0.0
  ```
  <b>Arguments</b>
  ```
    str： 原始串
    chars: 去除后的替换成字符（省略此参数，就空格）
  ```
  <b>Returns</b>
  ```
    (string)：返回去除后的字符串
  ```
  <b>Example</b>
  ```
    trim('𠮷abbb𠮷a', '𠮷a')
    // => 'bbb'
  ```
