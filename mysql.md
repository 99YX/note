# mysql学习

## 第一章 查询指令

### 1.1 基础语法

1 +号 :如果是字符+数字，"123"+1=124 这种是能转换的，如果"ajfa"+1=1,不能转换就将"ajfa"变成0，在进行转换。

如果null+任何数,则结果一定是null

2 拼接函数:

```
SELECT CONCAT(last_name,job_id) as"address" FROM `employees`
```

3 显示表的结构:

```
DESC 表名
```

4 判断字段是否为空 ：

```mysql
IFNULL(字段,如果为空，返回的字符信息)
```

5 指定转义字符:默认\

```mysql
select *  from 表 where like '自己指定转义字符' ESCAPE '自己指定字符'
```

5 安全等于:

```mysql
<=>
```

6 计算长度：

```
	LENGTH(str) 计算字节个数
```

7 查看字符：

```
show VARIABLES ：查看字段字符集  utf-8:中文三个字节 gbk:中文两个字节
```

8 字符大小写转换:

```
upper( str ):大写                                    LOWER(str):小写
```

8 字符串截取:

```mysql
SUBSTR("字符串"，开始索引,结束索引):索引从1开始,截取
```

9 字符串匹配：找到字符串的起始位置，没有就是0

```mysql
SELECT
	INstr( 'abc', 'a' ) AS '结果'
```

10 去空格：trim

```
trim
```

11 去除指定字符前后的字符

```mysql
select trim('字符' from '字符')
```

12
