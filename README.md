`#` 表示注释

`''' '''` 或者 `""" """` 表示区间注释，在三引号之间的所有内容被注释

| `//` | 整除（地板除） | `3 // 4` |
| ---- | -------------- | :------- |
| **   | 幂             | 2 ** 3   |

| `not` | 非   | `not (2 > 1)` |
| ----- | ---- | ------------- |
|       |      |               |

位运算理解（知乎）：https://blog.csdn.net/Trishia/article/details/108779065?ops_request_misc=%25257B%252522request%25255Fid%252522%25253A%252522161206226016780261916689%252522%25252C%252522scm%252522%25253A%25252220140713.130102334..%252522%25257D&request_id=161206226016780261916689&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_click~default-2-108779065.pc_search_result_before_js&utm_term=%25E4%25BD%258D%25E8%25BF%2590%25E7%25AE%2597

| 操作符 | 名称     | 示例     |
| ------ | -------- | -------- |
| `~`    | 按位取反 | `~4`     |
| `&`    | 按位与   | `4 & 5`  |
| `      | `        | 按位或   |
| `^`    | 按位异或 | `4 ^ 5`  |
| `<<`   | 左移     | `4 << 2` |
| `>>`   | 右移     | `4 >> 2` |

三元运算符：**条件表达式?表达式1:表达式2**。

说明：问号前面的位置是判断的条件，判断结果为[bool](https://baike.baidu.com/item/bool)型，为true时调用表达式1，为false时调用表达式2。

**其他运算符**

| 操作符   | 名称   | 示例                         |
| -------- | ------ | ---------------------------- |
| `in`     | 存在   | `'A' in ['A', 'B', 'C']`     |
| `not in` | 不存在 | `'h' not in ['A', 'B', 'C']` |
| `is`     | 是     | `"hello" is "hello"`         |
| `is not` | 不是   | `"hello" is not "hello"`     |

- 变量名可以包括字母、数字、下划线、但变量名不能以数字开头。

| 类型  | 名称                    | 示例           |
| ----- | ----------------------- | -------------- |
| int   | 整型 `<class 'int'>`    | `-876, 10`     |
| float | 浮点型`<class 'float'>` | `3.149, 11.11` |
| bool  | 布尔型`<class 'bool'>`  | `True, False`  |

**获取类型信息**

- `type(object)` 获取类型信息

**类型转换**

- 转换为整型 `int(x, base=10)`
- 转换为字符串 `str(object='')`
- 转换为浮点型 `float(x)`

## 5. print() 函数

```
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
```

- 将对象以字符串表示的方式格式化输出到流文件对象file里。其中所有非关键字参数都按`str()`方式进行转换为字符串输出；
- 关键字参数`sep`是实现分隔符，比如多个参数输出时想要输出中间的分隔字符；
- 关键字参数`end`是输出结束时的字符，默认是换行符`\n`；
- 关键字参数`file`是定义流输出的文件，可以是标准的系统输出`sys.stdout`，也可以重定义为别的文件；
- 关键字参数`flush`是立即把内容输出到流文件，不作缓存。

【例子】没有参数时，每次输出后都会换行。

```
shoplist = ['apple', 'mango', 'carrot', 'banana']
print("This is printed without 'end'and 'sep'.")
for item in shoplist:
    print(item)

# This is printed without 'end'and 'sep'.
# apple
# mango
# carrot
# banana
```

【例子】每次输出结束都用`end`设置的参数`&`结尾，并没有默认换行。

```
shoplist = ['apple', 'mango', 'carrot', 'banana']
print("This is printed with 'end='&''.")
for item in shoplist:
    print(item, end='&')
print('hello world')

# This is printed with 'end='&''.
# apple&mango&carrot&banana&hello world
```



练习题

1.`#` 表示单行注释

`''' '''` 或者 `""" """` 表示区间注释，在三引号之间的所有内容被注释

2.顺序是由高到低依次是：算术运算符、移位运算符、位运算符优先级、关系运算符、逻辑运算符、赋值运算符

3.is,is not比较的是两个对象的内存地址

   ==,!=比较的是两个对象的值

4.int(x [,base ])     将x转换为一个整数

long(x [,base ])     将x转换为一个长整数   

float(x )        将x转换到一个浮点数   

complex(real [,imag ])  创建一个复数   

str(x )         将对象 x 转换为字符串   

repr(x )         将对象 x 转换为表达式字符串   

eval(str )        用来计算在字符串中的有效 [Python](http://www.2cto.com/kf/web/Python/)表达式,并返回一个对象   

tuple(s )        将序列 s 转换为一个元组   

list(s )         将序列 s 转换为一个列表   

chr(x )         将一个整数转换为一个字符   

unichr(x )        将一个整数转换为Unicode字符   

ord(x )         将一个字符转换为它的整数值   

hex(x )         将一个整数转换为一个十六进制字符串   

oct(x )         将一个整数转换为一个八进制字符串 
