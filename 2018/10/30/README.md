## 掌握RxJS系列(01)：介绍响应式编程

最近一直在研究`RxJS`的知识，同时也不断地在了解响应式编程；随着逐步的深入，越发觉得这一部分知识很重要；无论是前端还是后端，如果能够很好地运用这一部分知识，对于开发一些复杂功能的应用真的可以起到事半功倍的效果。
关于`RxJS`我准备写一个系列的文章（如果我能够坚持下去的话😂），来跟大家一起探讨如何学习使用`RxJS`；之所以有这个想法是因为我在学习的过程中看到了[30天精通RxJS](https://ithelp.ithome.com.tw/users/20103367/ironman/1199)这一系列的文章，感觉受益匪浅；这里也对这一系列的文章的作者[JerryHong](https://github.com/Jerry-Hong)表示感谢。但是这一系列的文章都是繁体字，而且里面使用的`RxJS`的版本不是最新的版本（截止现在为止，`RxJS`最新的版本是`v6`），`v6`版本的API变化还是比较大的，所以我才萌生了新出一个系列文章的想法，这一个系列的文章都是在`v6`的基础上进行实践的，所以对读者来说会更好一些。
废话不多说，我们进入正题；首先什么是**响应式编程**？，其实我在学习`RxJS`之前也是没有一个明确的概念的；也查了很多的资料想弄明白到底什么是**响应式编程**，网上有各种说法，搞的我自己也很模糊；后来看了维基百科的解释，觉得还算是靠谱的，维基百科的解释如下：
> 在计算机中，响应式编程或反应式编程（英语：Reactive programming）是一种面向**数据流**和**变化传播**的编程范式。这意味着可以在编程语言中很方便地表达**静态**或**动态**的数据流，而相关的**计算模型**会自动将变化的值通过数据流进行传播。

大家看了上面的解释可能还是一头雾水，不知道上面的内容在说什么；没关系，我第一次看的时候也不知道说的啥，没有什么好沮丧的；我先给大家解释一下一些关键词：
- **数据流**：这是一个很重要的概念，需要我们换一种思路来看待我们平常习以为常的那些词语，比如变量，函数，对象，按钮点击，页面滚动，网络请求等等都可以看作是一个数据流。 *如果还不够明白的话，你还可以简单的理解为在一段时间内，应用程序里发生的一些变化*。
- **变化传播**：可以理解为， **数据流**的流动所带来的程序的内部的变化。
- **静态或者动态的数据流**：静态的数据流指的是同步的运算操作，动态的数据流指的是异步的操作运算。
- **计算模型**：指的是我们所使用的框架或者库。
上面的解释也都是我个人的一些见解，不一定很准确；希望可以帮助你更好地理解响应式编程。
我们其实可以通过一个简单的例子，更直观的来说明响应式编程是什么；在命令式编程环境中：`a = b + c`表示将表达式的结果赋给`a`，而之后改变`b`或`c`的值不会影响 `a`；但在响应式编程中，`a`的值会随着`b`或`c`的更新而更新。
还有，我们经常会用到一些**MVC**的编程框架，比如`Angular`，这些框架可以让我们把视图和数据模型进行绑定，一旦视图发生了变化，就会同步到数据模型上；反之，如果数据模型发生了变化，那么视图部分也会相应的发生变化。**MVC**类型的编程框架就是响应式编程的一种实现。
如果上面关于`响应式编程`的解释你觉得不满意，那么你可能跟[André Staltz](https://github.com/staltz)当初的想法一样；他觉得网上关于`响应式编程`的解释都不好；他认为，所谓的响应式编程的定义应该是：
> Reactive programming is programming with asynchronous data streams.

就是说： *响应式编程就是使用异步数据流编程*
[André Staltz](https://github.com/staltz)是[The introduction to Reactive Programming you've been missing](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754)这篇文章的作者，非常建议大家看看他的这篇介绍响应式编程的文章，讲的很不错。
但是在我看来，我觉得响应式编程应该是**使用数据流编程**，因为在实际的开发过程中，我们并不仅仅只是使用异步的数据流，还会有同步的数据流。所以响应式编程解释为**使用数据流编程**会更贴切。
希望这篇文章对于响应式编程的这些解释能让大家对响应式编程有一个不错的理解，理解响应式编程的概念对以后学习`RxJS`也是有一定的帮助的。

参考资料：
[响应式编程](https://zh.wikipedia.org/zh-cn/%E5%93%8D%E5%BA%94%E5%BC%8F%E7%BC%96%E7%A8%8B)（维基百科）

版权声明：[![知识共享许可协议](https://i.creativecommons.org/l/by-nc-nd/3.0/80x15.png)](http://creativecommons.org/licenses/by-nc-nd/3.0/) [共享-保持署名-非商业性使用-禁止演绎](http://creativecommons.org/licenses/by-nc-nd/3.0/)
