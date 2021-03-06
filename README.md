＃


```
Serverless
 根据CNCF的定义，Serverless是指构建和运行不需要服务器管理的运行服务的概念
 Serverless = FaaS + BaaS。
 FaaS（Function as a Service） 就是一些运行函数的平台，比如阿里云的函数计算、AWS 的 Lambda 等
 BaaS（Backend as a Service）则是一些后端云服务，比如云数据库、对象存储、消息队列等。利用 BaaS，可以极大简化我们的应用开发难度。
Serverless的主要特点：
 事件驱动
  函数在 FaaS 平台中，需要通过一系列的事件来驱动函数执行。
 无状态
  因为每次函数执行，可能使用的都是不同的容器，无法进行内存或数据共享。如果要共享数据，则只能通过第三方服务，比如 Redis 等。
 无运维
  使用 Serverless 我们不需要关心服务器，不需要关心运维。这也是 Serverless 思想的核心。
 低成本
  使用 Serverless 成本很低，因为我们只需要为每次函数的运行付费。函数不运行，则不花钱，也不会浪费服务器资源
 BFF：服务于前端的后端

 视频背景透明的方法：
  将视频背景色设置为黑色，同时设置如下css：
  video{
     mix-blend-mode：screen;
  }
  该方法在所有不需要兼容IE浏览器的项目中都可以使用

```

```
::before和::after下特有的content，用于在css渲染中向元素逻辑上的头部或尾部添加内容。

```

```
  不管什么程序语言，内存的生命周期基本都是一样的：
   1.分配你所需要的内存
   2.使用分配到的内存（读, 写）
   3.不需要时将其释放/归还

 垃圾回收算法主要依赖于引用的概念. 在内存管理的环境中, 一个对象如果有访问另一个对象的权限（隐式或者显式）, 叫做一个对象引用另一个对象.
 例如: 一个Javascript对象具有对它原型的引用（隐式引用）和对它属性的引用（显式引用）。

 普通网页开发渲染线程和脚本线程是互斥的，这也是为什么长时间的脚本运行可能会导致页面失去响应，而在小程序中，二者是分开的，分别运行在不同的线程中。
 小程序的渲染层和逻辑层分别由 2 个线程管理：视图层的界面使用了 WebView 进行渲染，逻辑层采用 JsCore 线程运行 JS脚本。
 事件表格（Event Table）:用来存储JavaScript 中的异步事件 (request, setTimeout, IO等) 及其对应的回调函数的列表
 事件队列 (Event Queue) :回调函数队列,当 Event Table 中的事件被触发，事件对应的 回调函数 就会被 push 进这个 Event Queue，然后等待被执行
 ![Image text](https://raw.githubusercontent.com/yin-chong/Study--notes/master/img/454794347-5cec9e1971f69_articlex.jpg)

 ECMAScript标准规定了7种数据类型，其把这7种数据类型又分为两种：原始类型和对象类型。

原始类型
   Null：只包含一个值：null
   Undefined：只包含一个值：undefined
   Boolean：包含两个值：true和false
   Number：整数或浮点数，还有一些特殊值（-Infinity、+Infinity、NaN）
   String：一串表示文本值的字符序列
   Symbol：一种实例是唯一且不可改变的数据类型
(在es10中加入了第七种原始类型BigInt，现已被最新Chrome支持)
对象类型
   Object：自己分一类丝毫不过分，除了常用的Object，Array、Function等都属于特殊的对象
   JavaScript中的原始类型的值被直接存储在栈中，在变量定义时，栈就为其分配好了内存空间。
   pop() 删除数组最后一个元素，如果数组为空，则不改变数组，返回undefined，改变原数组，返回被删除的元素
   push()向数组末尾添加一个或多个元素，改变原数组，返回新数组的长度
   shift()把数组的第一个元素删除，若空数组，不进行任何操作，返回undefined,改变原数组，返回第一个元素的值
   unshift()向数组的开头添加一个或多个元素，改变原数组，返回新数组的长度
   reverse()颠倒数组中元素的顺序，改变原数组，返回该数组
   sort()对数组元素进行排序，改变原数组，返回该数组
   splice()从数组中添加/删除项目，改变原数组，返回被删除的元素

```
