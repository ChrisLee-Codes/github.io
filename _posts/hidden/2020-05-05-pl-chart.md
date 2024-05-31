---
title: "Python Programming"
subtitle: "Python语法"
layout: post
author: "ChrisLee"
header-style: text
hidden: true
plchart: true
tags:
  - Python
  - programming
---

<iframe 
  id="chart"
  src="https://chrislee-codes.github.io/"
  frameborder="0" 
  scrolling="no" 
  style="width: 100%">
</iframe>



## Python 基本语法：
* 程序的格式框架:
	* Python的程序就像是一个故事，从上到下讲述。
	* 可以把一些常用的操作放到`函数`里，像个小工具箱。
* 缩进:
	* 在Python中，我们使用`空格`（通常是4个空格）来表示代码的层次。
	* 像是写作文的时候，新的一段会缩进开始。
* 注释:
	* 使用 `#` 来写一些解释或者提示。
	* Python 不会读这部分，是写给人看的。
```python
# 这是一个提示，Python不会读它
```
* 变量:
	* 变量就像是一个小盒子，可以放东西（数字、文字等）。
	* 你给每个盒子起一个名字，这样就可以找到它。
```python
my_number = 5
my_name = "ChrisLee"
```
* 命名:
	* 给变量起名字的时候，名字要有意义。
	* 比如叫 `number` 比叫 `a` 好理解。
* 保留字:
	* Python有一些特殊的词，我们不能用它们当作变量名。
	* 这些词有：`and`, `as`, `assert`, `break`, `class`, `continue`, `def`, `del`, `elif`, `else`, `except`, `False`, `finally`, `for`, `from`, `global`, `if`, `import`, `in`, `is`, `lambda`, `None`, `nonlocal`, `not`, `or`, `pass`, `raise`, `return`, `True`, `try`, `while`, 和 `with`。
* 数据类型:
	* Python有不同的“材料”或类型来存放信息。
		* `int`: 整数，比如 1, 2, 3。
		* `float`: 小数，比如 1.5, 2.6。
		* `str`: 文字，比如 "apple", "hello"。
		* `list`: 一个清单，可以放很多东西，比如 [1, 2, 3] 或 ["apple", "banana"]。
* 赋值语句:
	* 使用 `=` 来给变量放入一个值。
```python
my_favorite_number = 9
my_english_name = "ChrisLee"
```
* 引用:
	* 当我们给变量放东西时，实际上是给了一个地址或位置。
	* 就像告诉你去书架的第3层找一本书。
* 基本输入输出:
	* `input()`: 可以让用户告诉Python一些信息。
	* `print()`: 可以让Python告诉用户一些信息。
```python
your_name = input()             # 输入：ChrisLee
print("你好,", your_name, "!")  # 输出：你好,ChrisLee!
```

## 基本数据类型及其操作：
* 基本数据类型:
	- `int`:
	表示整数，例如：1, 2, 100, -50。
	- `float`:
	表示小数或浮点数，例如：1.23, 4.56, -7.89。
	- `str`:
	表示字符串或文字，例如："hello", 'world', "123"。
	- `bool`:
	表示布尔值，只有两个值：True 和 False。
* 数据类型的运算:
	- 对于 `int` 和 `float`:
		* `+`: 加法
		* `-`: 减法
		* `*`: 乘法
		* `/`: 除法
		* `//`: 整除（结果为整数）
		* `%`: 取余数
		* `**`: 乘方
	- 对于 `str`:
		* `+`: 连接两个字符串
		* `*`: 重复字符串
```python
name = "Chris" + "Lee"  # 结果: "ChrisLee"
repeat = "chris" * 3  # 结果: "chrischrischris"
```
* 类型判断:
使用 `type()` 函数来检查一个值的数据类型。
```python
x = 5
print(type(x))  # 输出: <class 'int'>
```
* 类型间转换:
	- `int()`:
	将其他数据类型转换为整数。
	- `float()`:
	将其他数据类型转换为浮点数。
	- `str()`:
	将其他数据类型转换为字符串。
	- `bool()`:
	将其他数据类型转换为布尔值。通常0、空字符串等为`False`，其他为`True`。
```python
number = int("123")  # 结果: 123
decimal = float("123.45")  # 结果: 123.45
text = str(123)  # 结果: "123"
boolean = bool(1) # 结果：True
```
## 程序的控制结构：
* 顺序结构:
	* 程序从上到下，一步一步执行，就像阅读故事书一样。
* 分支结构:
	- `if` 语句:
	判断一个条件，如果为真，就执行一部分代码。
	- `if-else` 语句:
	如果条件为真，执行if下的代码；否则，执行else下的代码。
	- `if-elif-else` 语句:
	可以判断多个条件，并执行匹配条件的代码块。
```python
age = 12
if age < 18:
    print("你还是个孩子。")
```
```python
age = 20
if age < 18:
    print("你还是个孩子。")
else:
    print("你已经是个大人了。")
```
```python
score = 85
if score >= 90:
    print("A级")
elif score >= 80:
    print("B级")
elif score >= 70:
    print("C级")
else:
    print("D级")
```
* 循环结构:
	- `for` 循环:
	对一个序列（如列表或字符串）中的每个元素都执行一遍循环。
	- `while` 循环:
	只要条件为真，就不断重复执行循环。
	- 循环控制语句:
		* `break`: 用于中断循环。
		* `continue`: 用于跳过当前循环的剩余部分，开始下一次循环。
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```
```python
count = 0
while count < 5:
    print(count)
    count += 1  # 这表示 count = count + 1
```
```python
# 使用break
for i in range(5):
	if i == 3:
		break
	print(i)  # 输出: 0, 1, 2

# 使用continue
for i in range(5):
	if i == 3:
		continue
	print(i)  # 输出: 0, 1, 2, 4
```

## 组合数据类型：
* 基本概念:
组合数据类型允许我们在一个结构中存储多个数据项。Python中的主要组合数据类型包括：列表、元组、字典和集合。

* 列表 (List):
	* **定义**: 列表是有序的元素集合，可以包含任何数据类型，且元素可以重复。
	* **创建**:
	* 常见操作:
		* **访问元素**: 使用索引访问，例如 `my_list[0]` 返回 `1`。
		* **添加元素**: 使用 `append()` 或 `insert()`。
		* **移除元素**: 使用 `remove()` 或 `pop()`。
		* **长度**: 使用 `len()` 函数。
		* **切片**: 使用 `:`，例如 `my_list[1:4]`。
		* **其他**: 如排序 (`sort()`)，逆序 (`reverse()`) 等。
```python
my_list = [1, 2, 3, 'apple', 'ChrisLee']
```
* 字典 (Dictionary):
	* **定义**: 字典是无序的键值对集合。每个键必须唯一。
	* **创建**:
	* 常见操作:
		* **访问元素**: 使用键访问，例如 `my_dict['name']` 返回 `ChrisLee`。
		* **添加元素**: 直接赋值，例如 `my_dict['job'] = 'Engineer'`。
		* **移除元素**: 使用 `del`，例如 `del my_dict['age']`。
		* **长度**: 使用 `len()` 函数。
		* **键和值**: 使用 `keys()` 获取所有键，使用 `values()` 获取所有值，使用 `items()` 获取所有键值对。
```python
my_dict = {'name': 'ChrisLee', 'age': 27, 'city': 'Beijing'}
```


## 函数和代码复用：
* 函数简介:
	* 函数就像是一个小工具箱，可以完成特定的任务。
	* 当你需要多次完成同样的任务时，可以创建一个函数，然后多次调用它。
* 定义函数:
使用 `def` 关键字来定义函数。例如，我们定义一个函数，用于两个数相加：
```python
def add_two_numbers(a, b):
    return a + b
```
* 调用函数:
调用函数就像是使用那个小工具箱：
```python
result = add_two_numbers(5, 3)  # 调用函数并传入5和3作为参数
print(result)  # 输出: 8
```
* 参数和返回值:
	* **参数**: 是传递给函数的值，可以想象成是工具箱需要的材料。
	* **返回值**: 函数完成工作后给你的结果。

	在上面的 `add_two_numbers` 函数中，`a` 和 `b` 是参数，`return a + b` 是返回值。

* 默认参数:
你可以为函数参数设置默认值。这样，如果在调用函数时没有提供 `name` 参数的值，它会使用默认的 "Limio"：
```python
def greet(name="Limio"):
    return "Hello, " + name + "!"

print(greet())          # 输出: Hello, Limio!
print(greet("ChrisLee"))   # 输出: Hello, ChrisLee!
```
* 代码复用:
函数的一个主要目的就是允许代码复用。当你发现自己多次编写同样的代码时，考虑将它放入一个函数中。

* 局部与全局变量:
	* **局部变量**: 在函数内部创建的变量。只能在该函数内部使用。
	* **全局变量**: 在函数外部创建，可以在整个程序中使用。
```python
global_variable = "I am global"

def check_scope():
    local_variable = "I am local"
    print(global_variable)  # 可以访问全局变量
    print(local_variable)   # 可以访问局部变量

check_scope()
# print(local_variable)   # 错误！因为它是局部变量
```

* 函数参数详解：
	* 必须参数:
		* 必须参数是调用函数时必须提供的参数，没有默认值。
		* 如果在调用函数时没有为必须参数提供值，Python会报错。
	* 默认参数（可选参数）:
		* 默认参数是在定义函数时为参数提供的默认值。
		* 如果在调用函数时没有为该参数提供值，它将使用默认值。
```python
def print_age(age):
    print("Your age is:", age)

print_age(25)  # 正确
# print_age()   # 错误! 因为没有提供必须的 age 参数
```

```python
def greet(name="Limio"):
    print("Hello,", name)

greet("ChrisLee")  # 输出: Hello, ChrisLee
greet()        # 输出: Hello, Limio
```
**比较**:
* 必须性:
	* 必须参数：在函数调用时必须提供。
	* 默认参数：在函数调用时可以省略，如果省略则使用默认值。
* 定义方法:
	* 必须参数：直接在函数定义中列出。
	* 默认参数：在函数定义时使用 = 给参数赋予一个默认值。
* 函数调用的灵活性:
	* 必须参数：提供的参数值的顺序与定义时的顺序应一致。
	* 默认参数：可以使用参数名在函数调用时传递值，这样可以跳过某些默认参数。
	```python
	def example_func(a, b=5, c=10):
		print(a, b, c)

	example_func(1)              # 输出: 1 5 10
	example_func(1, 2)           # 输出: 1 2 10
	example_func(1, 2, 3)        # 输出: 1 2 3
	example_func(1, c=3)         # 输出: 1 5 3，只更改 c 的值
	```

## 面向对象编程（OOP）：
* 基本概念:
面向对象编程是一种编程范式，它使用“对象”来组织代码，从而更好地模拟现实世界中的事物和情境。

* 类和对象:
	* **类 (Class)**: 是对象的蓝图或模板。可以想象成是建筑的设计图纸。
	* **对象 (Object)**: 是类的实例。基于类的蓝图创建的实体。类似于根据设计图纸建造的建筑。
```python
# 定义一个类
class Car:
    color = "white"

    def drive(self):
        print("ChrisLee, The car is driving.")

# 创建一个对象
my_car = Car()
my_car.drive()  # 输出: ChrisLee, The car is driving.
```
* 构造方法和 `self`:
	* 构造方法 `__init__`: 用于初始化对象。当创建类的新对象时，该方法会自动执行。
	* `self`: 在类的方法中，表示对象本身。它是所有方法的第一个参数。
```python
class Car:
    def __init__(self, color):
        self.color = color

    def describe(self):
        print("ChrisLee, The car is", self.color)

red_car = Car("red")
red_car.describe()  # 输出: ChrisLee, The car is red
```
* 类的继承:
	* 继承允许我们定义一个类，该类继承另一个类的属性和方法。
	* 新类被称为子类，被继承的类称为父类。
```python
# 父类
class Vehicle:
    def move(self):
        print("ChrisLee, The vehicle is moving.")

# 子类
class Bike(Vehicle):
    def ring_bell(self):
        print("Ring ring!")

my_bike = Bike()
my_bike.move()       # 输出: ChrisLee, The vehicle is moving.
my_bike.ring_bell()  # 输出: Ring ring!
```
* 多态:
	* 多态意味着不同的对象可以为同一方法提供不同的实现。
	* 它允许我们在子类中定义父类中已存在的方法。
```python
class Bird:
    def sound(self):
        print("Some sound")

class Sparrow(Bird):
    def sound(self):
        print("Chirp chirp")

class Crow(Bird):
    def sound(self):
        print("Caw caw")

sparrow = Sparrow()
crow = Crow()

sparrow.sound()  # 输出: Chirp chirp
crow.sound()     # 输出: Caw caw
```


## 文件操作:
* 文件打开与关闭:
```python
f = open("ChrisLee.txt", "r")  # 打开文件进行读取
content = f.read()            # 读取文件内容
f.close()                     # 关闭文件
```
* 文件读写操作:
	* `read(): 读取文件的全部内容。
	* `readline()`: 读取文件的一行。
	* `readlines()`: 读取文件的所有行并返回一个列表。
	* `write()`: 将字符串写入文件。
* 文件模式:
	* `r`: 读取模式。
	* `w`: 写入模式（如果文件存在，则清除内容）。
	* `a`: 追加模式。
	* `b`: 二进制模式。


## Python库：
* 标准库:
Python有一个广泛的标准库，这些库包含了很多有用的模块和函数，它们支持各种应用开发，如Web开发、数据处理、操作系统管理等。
	* 示例模块:
		* `random`：随机数库。
		* `math`: 提供数学运算函数。
		* `datetime`: 日期和时间处理功能。
* Python内置函数:
Python提供了许多内置函数，这些函数可以直接在Python程序中使用。
	* 示例函数:
		* `print()`: 打印输出。
		* `len()`: 返回对象的长度。
		* `type()`: 返回对象的类型。
		* `input()`: 从用户获取输入。
		* `int()`, `float()`, `str()`: 进行类型转换。
* 第三方库：
	* 示例模块:
		* `jieba`：中文分词库。
