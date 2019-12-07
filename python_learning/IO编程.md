# IO编程

## 文件读写

### 读取文件

```python
# 只读模式打开文本文件
f = open('D:/datasets/1.txt', 'r') as f
# 只读打开二进制文件，如图片，视频等
f = open('D:/datasets/1.png', 'rb')
# 读取文件内容
f.read()
# 关闭文件
f.close()
# 打开后自动关闭文件
with open('D:/datasets/1.txt', 'r):
# 写入文本文件--w模型会直接覆盖文件生成新文件--a模式是在文件末尾写入
f = open('D:/datasets/1.txt', 'w')
f.write('hello,world')
```


## 操作文件和目录

```python
# 查看当前目录的绝对路径
os.path.abspath('.')

# 在某个目录下创建一个新目录，首先把新目录的完整路径表示出来：
# 该方法也可用于将两个路径合成一个(将两个路径合成一个时，最好不要用字符串拼接的方式)
os.path.join('D:/datasets', 'new_file')

# 然后创建一个目录
os.mkdir('D:/datasets/new_file')

# 删除一个目录
os.rmdir('D:/datasets/mew_file')

# 拆分路径
os.path.split('D:/datasets/1.txt')
('D:/datasets', '1.txt')

# 得到文件的扩展名
os.path.splitext('D:/datasets/1.txt')

# 列出当前目录下的所有目录
# os.path.isdir(x):判断x是不是目录
[x for x in os.path.listdir('.') if os.path.isdir(x)]

# 列出当前目录下所有的.py文件
# os.path.isfile(x):判断x是否为文件
[x for x in os.path.listdir('.') if os.path.isfile(x) and os.path.splitext(x)[1]== '.py']

# 对文件重命名
os.rename('test.txt', 'test.py')

# 删除文件
os.remove('test.py')