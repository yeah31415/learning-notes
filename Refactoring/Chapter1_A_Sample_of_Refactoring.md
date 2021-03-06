## 重构例子小结

* 将原函数分解成一组嵌套的函数
  
* 应用*拆分阶段*分离计算逻辑与输出格式化逻辑（拆分功能）
  
* 引入*多态性*来处理计算逻辑

## 重构的过程建议

* 需要在所有可做的重构与添加新特性之间寻找平衡。但至少要遵循营地法则。

*  **营地法则**：保证你离开时的代码库一定比来时更健康。

* **好代码的检验标准**：人们能否轻而易举地修改它。最大限度地提升生产力，支持更快、更低成本地为用户添加新特性。
  
* 如果给程序添加新特性，但发现代码因缺乏良好结构而不易于进行更改，那就先重构那个程序，使其比较容易添加这个特性，然后再添加该新特性。
  
* 重构前，先检查自己是否有一套可靠的测试集。这些测试必须具有自我检验的能力，指的是可以自动校验期望值与实际值。
  
* 每当看到很长的函数，总是下意识想从函数中分出不同的关注点。
  
* 小步修改，每次修改后运行测试
  
* 代码推送到远端仓库前，会把零碎的修改压缩成一个更有意义的提交(rebase)

* 对于重构过程中的性能问题，建议是大多数情况可以忽略它。如果重构引入了性能损耗，先完成重构，再做性能优化。

* 每次修改都伴随着一次编译、测试、以及向本地代码库的提交。

* 保持一致的编码风格

* 总是尽量保持数据不可变

* 更喜欢显示地传入函数参数（反例：全局变量传入）

* 设计时的决策多考虑实际的使用者如何调用

## 重构例子中使用的方法

1. 提炼函数（可自动完成的重构）
2. 变量重命名（通常你需要几秒钟通读更多代码，才能发现最好的名称是什么）
3. 查询取代临时变量
4. 内联变量
5. 改变函数声明
6. 拆分循环
7. 移动语句
8. 以管道取代循环（map, fliter)
9. 以多态取代条件表达式（面向对象）
10. 改变函数声明
11. 以工厂函数取代构造函数（面向对象）
