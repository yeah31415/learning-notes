这里对重构名录的内容进行大致汇总，具体手法、例子见书中对应章节。

每个重构逻辑上都有一个反向的重构。<——> 表示互为反向。

## 最常见的重构手法（chapter 6)
* 提炼函数 <——> 内联函数
* 提炼变量（运算变成局部变量） <——> 内联变量（变量变成表达式）
* 改变函数声明
* 封装变量（get/set接口进行读取和更新）
* 变量改名
* 引入参数对象（一组数据变成结构/类，进行打包）
* 函数组合成类
* 函数组合成变换（函数）
* 拆分阶段（先后次序等）

## 面向对象的封装（chapter 7)
* 封装记录（dict/struct）
* 封装集合（list）
* 以对象取代基本类型
* 以查询取代临时变量
* 提炼类  <——> 内联类
* 隐藏委托关系 <——> 移除中间人
* 替换算法（优化算法，减少重复）

## 搬移特性（chapter 8)
* 搬移函数
* 搬移字段
* 搬移语句到函数  <——> 搬移语句到调用者
* 以函数调用取代内联代码 
* 移动语句
* 拆分循环（拆分成多个循环函数）
* 以管道取代循环（map, filter）
* 移除死代码

## 组织数据（chapter 9)
*  拆分变量（单一职责）
*  字段改名（函数名，类中字段）
*  以查询取代派生变量（实时计算）
*  将引用对象改为值对象（同一变量 -> 副本）

## 简化条件逻辑（chapter 10)
* 分解条件表达式（提炼成多个函数if/else） <——> 合并条件表达式（提炼成函数）
* 以卫语句取代嵌套表达式（优先判断，失败则return；如指针为空判断）
* 以多态取代条件表达式
* 引入特例（如：NULL对象）
* 引入断言

## 重构API（chapter 11)
* 将查询函数和修改函数分离（明确副作用）
* 函数参数化（引入参数，去除多次调用的重复）
* 移除标记参数
* 保持对象完整（传入整个对象，尽管暂时用不全）
* 以查询取代参数（参数的重复，计算与传入同样容易） <——> 以参数取代查询
* 移除设置函数（只在起初的对象创建过程中调用）
* 以工厂函数取代构造函数
* 以命令对象取代函数  <——> 以函数取代命令对象

## 处理继承关系（chapter 12)(待深入)
* 函数上移 <——> 函数下移
* 字段上移 <——> 字段下移
* 构造函数本体上移
* 以子类取代类型码
* 移除子类
* 提炼超类
* 折叠继承体系
* 以委托取代子类
* 以委托取代超类

## 一些原则（待补充）