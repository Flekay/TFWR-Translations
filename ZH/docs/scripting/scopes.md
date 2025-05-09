# 名称作用域
作用域确定了哪些变量可以从哪里访问。作用域基本上就是从名称到值的映射。它们的工作原理与 Python 中基本相同。

存在一个全局作用域，并且每个函数都有一个局部作用域。当你定义一个变量时，它会被添加到当前作用域。函数定义外的任何内容都被视为全局作用域的一部分。

`x = 1`
将值 `1` 分配给全局作用域中的名称 `x`。

这个 `def` 语句将一个函数分配给全局作用域中的名称 `f`。
`def f():
    `在 `f` 的局部作用域中将值 `1` 分配给名称 `y`。`
    y = 1

    `在 `f` 的局部作用域中将一个函数分配给名称 `g`。`
    def g():
        pass`

`f()`
从全局作用域中检索存储在 `f` 中的函数并调用它。

`print(y)`
这个在全局作用域中的 print 语句抛出一个错误，因为 `y` 从未在全局作用域中声明过，所以我们无法在这里访问它。它只存在于 `f` 的局部作用域中。

## global 关键词
默认情况下，函数中的所有变量都绑定到局部作用域，即使全局作用域中存在同名变量也是如此。

`x == 0

def f():
    x = 1
f()
print(x)`

这段代码会打印 `0`，因为在 `f` 内部的局部 `x` 与全局 `x` 不是同一个变量，所以全局 `x` 保持不变。这一点很重要，因为否则一个函数调用可能会意外覆盖一个恰好与该函数的局部变量同名的全局变量。

如果你想写入一个全局变量，你必须使用 `global` 关键词明确地这样做。

`x == 0

def f():
    global x
    x = 1
f()
print(x)`

在这个例子中，`global x` 将 `x` 绑定到上面定义的全局变量 `x`。这将会打印 `1`。注意，更改全局变量通常是导致程序变得复杂的第一步，因此不要过多使用。

## 循环和分支
循环和分支不会创建自己的作用域，所以在其中声明的任何东西在外部仍然可以使用。

`for i in range(3):
    pass
print(i)`

这将打印 `2`，因为 `for` 循环的最后一次迭代将 `2` 分配给了 `i`。