# mysql加强



# 第1章 字符串的函数

| Name                                     | 描述                                       |
| ---------------------------------------- | ---------------------------------------- |
| [`ASCII()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ascii) | 返回最左侧字符的数值 SELECT ASCII('a')             |
| [`BIN()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_bin) | 返回包含数字的二进制表示的字符串 SELECT BIN('11')        |
| [`BIT_LENGTH()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_bit-length) | 以位为单位返回参数长度 SELECT BIT_LENGTH('11')      |
| [`CHAR()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_char) | 返回传递的每个整数的字符 SELECT CHAR('123')          |
| [`CHAR_LENGTH()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_char-length) | 返回参数中的字符数  SELECT CHAR_LENGTH(1234)      |
| [`CHARACTER_LENGTH()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_character-length) | CHAR_LENGTH（）的同义词                        |
| [`CONCAT()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_concat) | 返回连接字符串 SELECT CONCAT("a" , "b" , "c");  |
| [`CONCAT_WS()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_concat-ws) | 返回与分隔符连接  SELECT CONCAT_WS('-','a','c')  |
| [`ELT()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_elt) | 返回索引号处的字符串  SELECT ELT(2,'a','a-c','abcd') |
| [`FIELD()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_field) | 返回后续参数中第一个参数的索引（位置）                                                               SELECT FIELD('ej', 'Hej', 'ej', 'Heja', 'hej', 'foo'); |
| [`FIND_IN_SET()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_find-in-set) | 返回第二个参数中第一个参数的索引位置 SELECT FIND_IN_SET('b','a,b,c,d'); |
| [`FORMAT()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_format) | 返回格式化为指定小数位数的数字 SELECT FORMAT("123.123",2) |
| [`INSERT()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_insert) | 在指定位置插入一个子字符串，直到指定的字符数                                               SELECT INSERT('Quadratic', 3, 1, 'What'); |
| [`INSTR()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_instr) | 返回第一次出现的子串的位置 SELECT INSTR('foobarbar', 'bar'); |
| [`LCASE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_lcase) | LOWER（）的同义词 SELECT LCASE('FOOT');        |
| [`LENGTH()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_length) | 以字节为单位返回字符串的长度  SELECT LENGTH('ab')      |
| [`LIKE`](http://dev.mysql.com/doc/refman/5.7/en/string-comparison-functions.html#operator_like) | 简单的模式匹配                                  |
| [`LOAD_FILE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_load-file) | 加载指定的文件                                  |
| [`LOCATE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_locate) | 返回第一次出现的子串的位置 SELECT LOCATE('a' , 'xxxxabbbbaa') |
| [`LOWER()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_lower) | 以小写形式返回参数                                |
| [`LPAD()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_lpad) | 返回字符串参数，使用指定的字符串进行左填充 SELECT LPAD('hi',4,'?!'); |
| [`LTRIM()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ltrim) | 删除前导空格 SELECT LTRIM('  barbar');         |
| [`MAKE_SET()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_make-set) | 返回一组以逗号分隔的字符串，这些字符串具有相应的位设置位                              SELECT MAKE_SET(2,'a','b','c'); |
| [`MATCH`](http://dev.mysql.com/doc/refman/5.7/en/fulltext-search.html#function_match) | 执行全文搜索                                   |
| [`MID()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_mid) | 返回从指定位置开始的子字符串  MID(*str*,*pos*,*len*) 是  SUBSTRING(*str*,*pos*,*len*)               SELECT MID('abcdef' , 1 , 3 ) |
| [`NOT LIKE`](http://dev.mysql.com/doc/refman/5.7/en/string-comparison-functions.html#operator_not-like) | 简单模式匹配的否定                                |
| [`OCT()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_oct) | 返回包含数字的八进制表示的字符串 SELECT OCT(123)         |
| [`OCTET_LENGTH()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_octet-length) | LENGTH（）的同义词 SELECT  OCTET_LENGTH('abc') |
| [`ORD()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ord) | 返回参数最左侧字符的字符代码 SELECT ORD('abc');        |
| [`QUOTE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_quote) | 转义参数以在SQL语句中使用 SELECT QUOTE('Don\'t!')   |
| [`REGEXP`](http://dev.mysql.com/doc/refman/5.7/en/regexp.html#operator_regexp) | 使用正则表达式匹配模式  SELECT 'abc' REGEXP 'a'     |
| [`REPEAT()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_repeat) | 重复指定次数的字符串  SELECT REPEAT('MySQL', 3);   |
| [`REPLACE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_replace) | 替换指定字符串的出现次数   SELECT REPLACE('www.mysql.com', 'w', 'Ww'); |
| [`REVERSE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_reverse) | 反转字符串中的字符 SELECT REVERSE('abc')          |
| [`RIGHT()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_right) | 返回指定的最右边的字符数  SELECT RIGHT('foobarbar', 4); |
| [`RLIKE`](http://dev.mysql.com/doc/refman/5.7/en/regexp.html#operator_regexp) | REGEXP的同义词                               |
| [`RPAD()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_rpad) | 追加指定次数的字符串 SELECT RPAD('hi',5,'?!');     |
| [`RTRIM()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_rtrim) | 删除尾随空格 SELECT RTRIM('barbar   ');        |
| [`SPACE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_space) | 返回指定数量的空格的字符串 SELECT SPACE(6);           |
| [`STRCMP()`](http://dev.mysql.com/doc/refman/5.7/en/string-comparison-functions.html#function_strcmp) | 比较两个字符串 SELECT STRCMP('text2', 'text');  若所有的字符串均相同，则返回STRCMP()，若根据当前分类次序，第一个参数小于第二个，则返回   -1，其它情况返回 1 。 |
| [`SUBSTR()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_substr) | 返回指定的子字符串 SELECT SUBSTR('abcd',2);       |
| [`SUBSTRING()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_substring) | 返回指定的子字符串 SELECT SUBSTRING('abcd',2,2);  |
| [`SUBSTRING_INDEX()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_substring-index) | 在指定的分隔符出现次数之前从字符串返回子字符串                                                 SELECT SUBSTRING_INDEX('www.mysql.com', '.', 2); |
| [`TRIM()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_trim) | 删除前导和尾随空格  SELECT TRIM('  abc  ')        |
| [`UCASE()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ucase) | UPPER（）的同义词 SELECT UCASE('abc')          |
| [`UPPER()`](http://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_upper) | 转换为大写 SELECT UPPER('abc')                |
| convert()                                | 转换字符串                                                                                                                         SELECT  CONVERT(NOW(),CHAR) FROM DUAL;                                                    SELECT  CAST(NOW() AS CHAR) FROM DUAL; |

常用函数:

- 合并字符串函数：concat(str1,str2,str3…)  concat_ws('分隔符' , str1 , str2 ,str3)
- 获取字符串字节数函数：length(str)
- 获取字符串字符数函数：char_length(str)
- 字母大小写转换函数：大写：upper(x),ucase(x)；小写lower(x),lcase(x)
- 字符串查找函数 find_in_set( findStr  , str)
- 获取指定位置的子串  locate( findStr, str)
- 字符串去空格函数 trim( str )   ltrim( str )   rtrim( str )
- 字符串替换函数 ： replace(未被替换前的字符 ,  指定需要被替换的字符 ,  如果匹配成功替换的字符 );
- 字符串截取函数 ： substr(完整字符 , 截取的长度)  substring(完整字符 , 从哪开始截取, 截取的长度 )

# 第2章 日期函数

| 名称                                       | 描述                                       |
| ---------------------------------------- | ---------------------------------------- |
| [`ADDDATE()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_adddate) | 将时间值（间隔）添加到日期值  SELECT ADDDATE(NOW() ,2 ) |
| [`ADDTIME()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_addtime) | 添加时间  SELECT ADDTIME(NOW() ,60*2)        |
| [`CURDATE()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_curdate) | 返回当前日期不携带时分秒 SELECT CURDATE()            |
| [`CURRENT_DATE()`， `CURRENT_DATE`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-date) | CURDATE（）的同义词                            |
| [`CURRENT_TIME()`， `CURRENT_TIME`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-time) | CURTIME（）的同义词                            |
| [`CURRENT_TIMESTAMP()`， `CURRENT_TIMESTAMP`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-timestamp) | 同义词NOW（）                                 |
| [`CURTIME()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_curtime) | 返回当前时间 只返回时间  SELECT  CURTIME()          |
| [`DATE()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date) | 提取日期或日期时间表达式的日期部分 SELECT DATE( NOW() )   |
| [`DATE_ADD()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date-add) | 将时间值（间隔）添加到日期值                              select DATE_ADD(CURDATE(), INTERVAL 24 HOUR) |
| [`DATE_FORMAT()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date-format) | 格式化日期指定 SELECT DATE_FORMAT(NOW() , "%Y")  表达式查阅课外文档 |
| [`DATE_SUB()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date-sub) | 从日期中减去时间值（间隔）                                                                                 select DATE_SUB(CURDATE(), INTERVAL 2 HOUR) |
| [`DATEDIFF()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_datediff) | 减去两个日期     SELECT DATEDIFF("2019-08-01",CURDATE()) |
| [`DAY()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_day) | DAYOFMONTH（）的同义词  SELECT DAY( NOW() )  时间减去两天 |
| [`DAYNAME()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayname) | 返回工作日的名称  SELECT DAYNAME(NOW())          |
| [`DAYOFMONTH()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayofmonth) | SELECT DAYOFMONTH(NOW()) 时间减去两天          |
| [`DAYOFWEEK()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayofweek) | 返回参数的工作日索引 SELECT DAYOFWEEK(NOW())       |
| [`DAYOFYEAR()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayofyear) | 返回一年中的某一天（1-366） SELECT DAYOFYEAR(NOW()) |
| [`EXTRACT()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_extract) | 提取部分日期 SELECT EXTRACT(MONTH FROM '1999-07-02') |
| [`FROM_DAYS()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_from-days) | 给定一个天数  *N*, 返回一个DATE值。 SELECT FROM_DAYS('729669') |
| [`HOUR()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_hour) | 提取小时 SELECT HOUR(NOW())                  |
| [`LAST_DAY`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_last-day) | 返回参数的月份的最后一天 SELECT LAST_DAY(NOW())      |
| [`LOCALTIME()`， `LOCALTIME`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtime) | NOW（）的同义词                                |
| [`LOCALTIMESTAMP`， `LOCALTIMESTAMP()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtimestamp) | NOW（）的同义词                                |
| [`MINUTE()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_minute) | 从论证中返回分钟 SELECT MINUTE(NOW())            |
| [`MONTH()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_month) | 从过去的日期返回月份 SELECT MONTH(NOW())           |
| [`MONTHNAME()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_monthname) | 返回月份名称  SELECT MONTHNAME(NOW())          |
| [`NOW()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_now) | 返回当前日期和时间                                |
| [`QUARTER()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_quarter) | 从日期参数返回季度  SELECT QUARTER(NOW())         |
| [`SEC_TO_TIME()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_sec-to-time) | 将秒转换为'hh：mm：ss'格式 SELECT SEC_TO_TIME(111) |
| [`SECOND()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_second) | 返回秒（0-59）  SELECT SECOND(NOW())          |
| [`STR_TO_DATE()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_str-to-date) | 将字符串转换为日期 SELECT STR_TO_DATE('04/31/2004', '%m/%d/%Y'); |
| [`SUBDATE()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_subdate) | 使用三个参数调用时DATE_SUB（）的同义词                                                 SELECT SUBDATE(NOW(),INTERVAL 22 HOUR) |
| [`TIME()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_time) | 提取传递的表达式的时间部分 SELECT TIME(NOW())         |
| [`TO_DAYS()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_to-days) | 返回转换为days的日期参数 SELECT TO_DAYS(NOW())     |
| [`TO_SECONDS()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_to-seconds) | 返回自0年以来转换为秒的日期或日期时间参数                    |
| [`WEEK()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_week) | 返回周数 SELECT WEEK('2018-01-08')           |
| [`WEEKDAY()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_weekday) | 返回工作日索引  SELECT WEEKDAY(NOW())           |
| [`WEEKOFYEAR()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_weekofyear) | 返回日期的日历周（1-53） SELECT WEEKOFYEAR(NOW())  |
| [`YEAR()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_year) | 返回年份  SELECT YEAR(NOW())                 |
| [`YEARWEEK()`](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_yearweek) | 返回年份和星期  SELECT YEARWEEK(NOW())          |
| SYSDATE()                                | 当前时间 等效now()                             |

常用函数

- 当前日期函数: now()
- 返回参数的月份的最后一天 : last_day( date )
- 从日期参数返回季度  : quarter( date )
- 返回两个日期之间的天数 : datediff(date1 ,date2)
- 根据传入的日期格式返回需要的日期: date_format( date , 日期格式 )  参考扩展文档

# 第3章 数字函数(了解)

- 绝对值函数：abs(x)
- 向上取整函数：ceil(x)
- 向下取整函数:floor(x)
- 取模函数：mod( x,y)
- 随机数函数：rand()
- 四舍五入函数：round(x,y)
- 数值截取函数：truncate(x,y) : 返回数字X，截断到D小数位。 如果D为0，结果没有小数点或小数部分。 D是负数，导致值X的小数点左边的D数字变为零。 

# 第4章 特殊函数

## 4.1 流程判断函数

### 4.1.1 case when then

在查询代码的过程中，可能我们需要对查询的结果进行判断，例如java中的if判断，此时我们可以使用case when ten else的条件判断

```sql
语法: 
	SELECT 
		CASE [字段,值] WHEN 判断条件 THEN  希望的到的值
		WHEN 判断条件 THEN 希望的到的值 
		ELSE 前面条件都没有满足情况下得到的值 END; 
	SELECT 
		CASE 11 WHEN 1 THEN 'one' 
		WHEN 2 THEN 'two' 
		ELSE 'more' END; 
	SELECT 
		CASE WHEN 1>0 THEN 'true' 
	ELSE 'false' END; 
```

### 4.1.2 if

如果 expr1 是TRUE (expr1 <> 0 and expr1 <> NULL)，则 IF()的返回值为expr2; 否则返回值则为 expr3。IF() 的返回值为数字值或字符串值，具体情况视其所在语境而定。SELECT IF(1<2,'yes ','no'); 

```sql
	函数: 
		IF(条件 ,条件成立的值,条件不成立的值)  
	语法: 
		select IF(条件 , 条件成立的值 , 条件不成立的值)  
		SELECT IF(1>2,2,3); 
```

### 4.1.3 ifnull

我们在数据库中难免碰到为null的字段，此时我们需要进行特定的转换而不是直接修改数据库的值，那么可以采用

ifnull函数进行转换。其主要目的就是将null值转换成我们自己想要的值

```
	函数: 
		ifnull( 需要判断的值或字段 , 如果为null转换后的值 )
	使用:
		SELECT IFNULL(NULL , '这是将null转换后的值')
```

## 4.2 加密函数

### 4.2.1 password(str)

加密函数是MySQL中用来对数据进行加密的函数。因为数据库中有些很敏感的信息不希望被其他人看到，就应该通过加密方式来使这些数据变成看似乱码的数据。例如用户的密码，就应该经过加密。
PASSWORD(str)函数可以对字符串str进行加密。一般情况下，PASSWORD(str)函数主要是用来给用户的密码加密的。下面使用PASSWORD(str)函数为字符串“123456”加密。

```sql
 语法 : 
	 password(str)
	 select password('123456')
```

### 4.2.2 MD5(str)

MD5(str)函数可以对字符串str进行加密。MD5(str)函数主要对普通的数据进行加密。下面使用MD5(str)函数为字符串“123456”加密

```sql
 语法:
	MD5(str)
	select MD5('123456')
```

# 第5章 案例

### 5.1 获取某个时间范围内的数据

```mysql

# 1、利用to_days函数查询今天的数据：
select * from 表名 where to_days(时间字段名) = to_days(now());
# to_days函数：返回从0000年（公元1年）至当前日期的总天数。

# 2、昨天
SELECT * FROM 表名 WHERE TO_DAYS( NOW( ) ) – TO_DAYS( 时间字段名) <= 1
# 3.7天
SELECT * FROM 表名 where DATE_SUB(CURDATE(), INTERVAL 7 DAY) <= date(时间字段名)
# 4.近30天
SELECT * FROM 表名 where DATE_SUB(CURDATE(), INTERVAL 30 DAY) <= date(时间字段名)
# 5.本月
SELECT * FROM 表名 WHERE DATE_FORMAT( 时间字段名, ‘%Y%m' ) = DATE_FORMAT( CURDATE( ) , ‘%Y%m' )
# 6.上一月
SELECT * FROM 表名 WHERE PERIOD_DIFF( date_format( now( ) , ‘%Y%m' ) , date_format( 时间字段名, ‘%Y%m' ) ) =1
#查询本季度数据
select * from `ht_invoice_information` where QUARTER(create_date)=QUARTER(now());
#查询上季度数据
select * from `ht_invoice_information` where QUARTER(create_date)=QUARTER(DATE_SUB(now(),interval 1 QUARTER));
#查询本年数据
select * from `ht_invoice_information` where YEAR(create_date)=YEAR(NOW());
#查询上年数据
select * from `ht_invoice_information` where year(create_date)=year(date_sub(now(),interval 1 year));

# 查询当前这周的数据
SELECT name,submittime FROM enterprise WHERE YEARWEEK(date_format(submittime,'%Y-%m-%d')) = YEARWEEK(now());
# 查询上周的数据
SELECT name,submittime FROM enterprise WHERE YEARWEEK(date_format(submittime,'%Y-%m-%d')) = YEARWEEK(now())-1;
# 查询当前月份的数据
select name,submittime from enterprise where date_format(submittime,'%Y-%m')=date_format(now(),'%Y-%m')
# 查询距离当前现在6个月的数据
select name,submittime from enterprise where submittime between date_sub(now(),interval 6 month) and now();
# 查询上个月的数据
select name,submittime from enterprise where date_format(submittime,'%Y-%m')=date_format(DATE_SUB(curdate(), INTERVAL 1 MONTH),'%Y-%m')
select * from ` user ` where DATE_FORMAT(pudate, ‘ %Y%m ‘ ) = DATE_FORMAT(CURDATE(), ‘ %Y%m ‘ ) ;
# 
select * from user where WEEKOFYEAR(FROM_UNIXTIME(pudate,'%y-%m-%d')) = WEEKOFYEAR(now())
select *
from user
where MONTH (FROM_UNIXTIME(pudate, ‘ %y-%m-%d ‘ )) = MONTH (now())
# 
select *
from [ user ]
where YEAR (FROM_UNIXTIME(pudate, ‘ %y-%m-%d ‘ )) = YEAR (now())
and MONTH (FROM_UNIXTIME(pudate, ‘ %y-%m-%d ‘ )) = MONTH (now())
# 
select *
from [ user ]
where pudate between 上月最后一天
and 下月第一天
where date(regdate) = curdate();
# 
select * from test where year(regdate)=year(now()) and month(regdate)=month(now()) and day(regdate)=day(now())
# 
SELECT date( c_instime ) ,curdate( )
FROM `t_score`
WHERE 1
LIMIT 0 , 30
```

