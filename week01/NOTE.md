学习笔记

**1 Null与undefined的区别？**

   答：null表示“没有对象”，即该处不应该有值，典型用法是：

​           a .作为函数的参数，表示该函数不是对象

​           b. 作为原型链的终点

​           undefined表示“缺少值”，表示次数应该有个值，但是还没有定义。典型用法：

​           a. 变量被声明了，但没有赋值

​           b. 调用函数时，应该提供的参数没有提供

​           c .对象没有赋值

​            d.函数没有返回值

**2.为什么有的编码更规范要求用void 0代替undefined？****

作用一：undefined不是关键字而是变量，它随时可能被篡改成其他值，void运算符不论该表达式原来是否有自己    的返回值，其返回值都为undefined，可以有效地避免篡改。

**3.为什么在JavaScript中，0.1+0.2不能=0.3?**

​    浮点数运算地精度问题导致结果不是严格相等，而是相差了个微小的值。

 **4.关于Symbol的补充**：Symbol表示独一无二的值。

**5 es6中有三类结构生来就具有Iterator接口**：数组、类数组对象、Map和Set结构

**5.for...in与for...of的区别**

   for...in遍历结果是key，数组下标；for...of遍历结果是value，按上述数组值推广开来，for...in遍历键名，  for...of遍历键值

  `for...in` 语句以原始插入顺序迭代对象的可枚举属性。

   for...of`语句遍历可迭代对象定义要迭代的数据。

   可枚举属性：“可枚举”标志设置为true的属性。js中基本包装类型是不可枚举的，如Object，Array,Number等

   可枚举的属性可以通过[for...in](https://links.jianshu.com/go?to=https%3A%2F%2Flink.zhihu.com%2F%3Ftarget%3Dhttps%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FJavaScript%2FReference%2FStatements%2Ffor...in)循环进行遍历（除非该属性名是一个[Symbol](https://links.jianshu.com/go?to=https%3A%2F%2Flink.zhihu.com%2F%3Ftarget%3Dhttps%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FJavaScript%2FReference%2FGlobal_Objects%2FSymbol)），或者通过Object.keys()方法返回一个可枚举属性的数组

   在ECMAScript6中，所有的集合对象（数组，Set集合以及Map集合）和字符串都是可迭代的对象