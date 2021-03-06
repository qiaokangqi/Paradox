# 符号计算

> 什么是符号计算？

```
c = a + b
d = a - b
e = c - d
```

那么计算得到`e = (a + b) - (a - b)`，这就是符号计算。

看起来似乎什么计算都没有发生，事实确实如此，但不仅如此。

> 符号计算是没有发生“计算”，但又发生了“计算”。

* “没有发生计算“，指的是没有发生实质的数值计算，这里无论`a`和`b`值是多少都无关紧要。
* “但又发生计算”，指的是并非任何处理都没有做，因为切切实实`e = (a + b) - (a - b)`是计算出来的。

说到这里，应该不难理解，其实符号计算，就是“代数计算”。

Paradox主要功能就在于构建一个具有梯度计算功能的的符号计算系统。

## 系统实现

在Paradox中，所有符号计算的载体都是由Symbol（符号）和Operator（算子）构成。

> Symbol共有3个衍生类，分别是Variable、Constant和Placeholder。

* Variable，字面意义是变量，它的作用是告诉计算引擎该符号的值是可变的，其值不能用于计算优化。

