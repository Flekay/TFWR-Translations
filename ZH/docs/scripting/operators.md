# 运算符
算术运算符：`+, -, *, /, //, %, **`
比较运算符：`==, !=, <=, >=, <, >`
布尔运算符：`not, and, or`

注意：游戏中的所有数字都是浮点数。因此，所有算术运算符都是浮点运算符。
`//` 被定义为在除法后向下取整。

若要使用赋值运算符，你需要解锁“变量”功能。

## 介绍
运算符允许你比较、修改和组合数值。
算术运算符 `+, -, *, /, //, %, **` 用于对数字进行常见的数学运算。
比较运算符 `==, !=, <=, >=, <, >` 用于比较数值。结果总是 `True` 或 `False`。
逻辑运算符（也叫布尔运算符）`not, and, or` 用于组合真值。

## 算术运算符
`+` 和 `-` 用于加法和减法。

`2 + 3` 计算结果是 `5`
`3 - 2` 计算结果是 `1`

`*`, `/` 和 `//` 用于乘法和除法。

`2 * 3` 计算结果是 `6`
`5 / 2` 计算结果是 `2.5`

`//` 与 `/` 相同，但结果会向下取整（四舍五入到下一个整数）。

`5 // 2` 计算结果是 `2`

`%` 是取模运算符，也称为取余运算符。它基本上除两数，然后返回余数。你也可以把它想象成反复从左边的数中减去右边的数，直到余数小于右边的数。

`4 % 2` 计算结果是 `0`
`5 % 2` 计算结果是 `1`
`6 % 2` 计算结果是 `0`
`2 % 6` 计算结果是 `2`
`1.5 % 1` 计算结果是 `0.5`

`**` 是幂运算符。

`2**2` 计算结果是 `4`
`(-5)**3` 计算结果是 `-125`

## 比较运算符
`==` 和 `!=` 用于检查两个值是否相等 (`==`) 或不相等 (`!=`)。它们可以用于所有类型的值。

`2 == 2` 计算结果是 `True`
`Entities.Bush != Entities.Bush` 计算结果是 `False`
`3 != 3 + 1` 计算结果是 `True`

`<=, >=, <, >` 只能用于数字。它们检查左边的数字是否小于或等于 (`<=`)、大于或等于 (`>=`)、小于 (`<`) 或大于 (`>`) 右边的数字。

`1 <= 1` 计算结果是 `True`
`2 >= 3` 计算结果是 `False`
`-2 < -1` 计算结果是 `True`
`6 > 6` 计算结果是 `False`

## 逻辑运算符
`not` 简单地反转值：

`not False` 计算结果是 `True`
`not True` 计算结果是 `False`

`and` 仅当两个值都为 `True` 时，结果才是 `True`

`True and True` 计算结果是 `True`
`True and False` 计算结果是 `False`
`False and False` 计算结果是 `False`

`or` 如果至少一个值为 `True`，结果就是 `True`

`True or True` 计算结果是 `True`
`True or False` 计算结果是 `True`
`False or False` 计算结果是 `False`