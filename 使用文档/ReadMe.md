# Date
* ## dateFormat(date, format)</br>
  将日期按照指定格式格式化并返回格式化后的日期。</br>
  </br>
  <b>Since</b>
  
      1.0.0
  <b>Arguments</b>

      date(number | Date): 预格式化的日期。
      format(string): 日期格式。
  <b>Returns</b>

      (string): 返回格式化后的日期。
  <b>Example</b>

      EUtils.dateFormat(1531643785284, 'yyyy-MM-dd');
      // => '2018-07-15';
