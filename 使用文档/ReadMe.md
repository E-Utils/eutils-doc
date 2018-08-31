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
    trim(' abbb ')
    // => 'abbb'
  ```

* ## generateUUID()<br />
  生成唯一的通用标识符（UUID），可用于生成react的列表渲染时所需的key

  <b>Since</b>
  ```
    1.1.0
  ```
  <b>Returns</b>
  ```
    (string)：返回唯一的UUID
  ```
  <b>Example</b>
  ```
    generateUUID()

    // => 'af22-3fa8-4028-8dea-30a2'
  ```
* ## indexOf()<br />
  数组中查找指定字符

  <b>Since</b>
  ```
    1.1.0
  ```
  <b>Returns</b>
  ```
    (number)：指定字符再数组中索引
  ```
  <b>Example</b>
  ```
    indexOf([1, 2, 1, 2], 2)
    // => 1

    indexOf([1, 2, 1, 2], 2, 2)
    // => 3
  ```

# Array
* ## includes(collection, value, fromIndex)<br />
  从fromIndex索引开始查找collection集合中是否存在value，惰性匹配，匹配到一个就不会匹配后面的，返回Boolean类型值
  注意：fromIndex不支持负数，出现问题后果自负
  <br />
  <br />
  <b>Since</b>

        1.1.0
  <b>Arguments</b>

      collection： 集合|字符串|字面量对象,
      value：要查找的值,
      fromIndex：从指定索引开始查找

  <b>Returns</b>

      (boolean)：返回布尔值true|false
  <b>Example</b>

      includes('abccdd', 'cc')
      // => true
      includes({cc: 222}, 'cc')
      // => true
      includes(true, 'cc')
      // => false
      includes([1, 3, [1,2], {1:3}], {1:3})
      // => true
      includes([1, 3, [1,2], {1:3}], {1:3}, 4)
      // => false

* ## unique(arr, iterator)<br />
  将arr中重复元素过滤，返回唯一元素新数组，支持对象的判断
  <br />
  <br />
  <b>Since</b>

        1.1.0
  <b>Arguments</b>

      arr： 数组,
      iterator：过滤器方法,

  <b>Returns</b>

      (array)：返回不重复元素的数组
  <b>Example</b>

      unique([1, 3, 5, 6, 8, 8, 6, 3, [1,2], [1,2], {item: 1, 2: 3}, {item: 1, 2: 3}])
      // => [1, 3, 5, 6, 8, [1,2], {item: 1, 2: 3}]

* ## union(firstArr, secondArr)<br />
  将firstArr和secondArr数组合并，并过滤重复的元素，返回一个新的数组。
  <br />
  <br />
  <b>Since</b>

        1.1.0
  <b>Arguments</b>

      firstArr: 第一个数组
      secondArr: 第二个数组

  <b>Returns</b>

      (array)：返回一个新的数组
  <b>Example</b>

      union([1, 3, 5],  [6, 8, 8, 6, 3])
      // => [1, 3, 5, 6, 8]

* ## minus(firstArr, secondArr)<br />
  将firstArr与secondArr数组做差集，返回一个差集后的数组
  <br />
  <br />
  <b>Since</b>

        1.1.0
  <b>Arguments</b>

      firstArr: 第一个数组
      secondArr: 第二个数组

  <b>Returns</b>

      (array)：返回一个新的数组
  <b>Example</b>

      minus([1, 3, 5, 6], [8, 8, 6, 3, 2])
      // => [1, 5]

* ## intersection(firstArr, secondArr)<br />
  将firstArr与secondArr数组做交集，返回一个交集后的数组
  <br />
  <br />
  <b>Since</b>

        1.1.0
  <b>Arguments</b>

      firstArr: 第一个数组
      secondArr: 第二个数组

  <b>Returns</b>

      (array)：返回一个新的数组
  <b>Example</b>

      intersection([1, 3, 5, 6], [8, 8, 6, 3])
      // => [3, 6]