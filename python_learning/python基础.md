# python中的一些基本概念

* python中整数和浮点数都没有大小限制

* **动态语言**:变量本身类型不固定
  * python是动态语言

```python
a = 1 # a 是整数
print(a)
a = 'a' # a 是字符串
print(a)

1
a
```

* **静态语言**:静态语言在定义变量时必须指定变量类型，如果赋值的时候类型不匹配，就会报错
  * C, C++, java都是静态语言

```java
int a = 123; // a是整数类型变量
a = "ABC"; // 错误：不能把字符串赋给整型变量
```


## 字符编码

我们已经讲过了，字符串也是一种数据类型，但是，字符串比较特殊的是还有一个编码问题。

因为计算机只能处理数字，如果要处理文本，就必须先把文本转换为数字才能处理。最早的计算机在设计时采用**8个比特（bit）作为一个字节（byte）**，所以，**一个字节能表示的最大的整数就是255**(二进制11111111=十进制255)

由于计算机是美国人发明的，因此，最早只有127个字符被编码到计算机里，也就是大小写英文字母、数字和一些符号，这个编码表被称为ASCII编码，比如大写字母A的编码是65，小写字母z的编码是122。