困难的事情不要做，做了一定会出问题。

不知道大家在项目开发工作中有没有遇到过类似的问题：从A页面跳到B页面再跳到C页面，返回时直接从C页面返回到A页面。

如果我们的页面是一路Push过去的，从C页面返回到A页面时，就不能简单地使用Pop。因为C页面Pop后，只能回到B页面。

要实现C页面Pop到A页面有很多方法。比如通过页面类型或指定层数Pop到指定的页面。比如通过代理实现连Pop。

虽然能做到，但代码并不漂亮，逻辑上也容易有意外。

Navigation里的VC栈层次，一旦发生意外，很容易导致应用崩溃。

善用Present将有助于避免引起Navigation的VC栈混乱。

那什么时候通过Present来代替Push呢？

简而言之：如果一个页面，以返回时可能会被跳过，那么这个页面就应该通过Present进行跳转，使它独立于已有的Navigation VC栈。

比如常见的充值页面、登录页面、编辑页面等等。

后记(下面有聊家常为主，没时间没兴趣的朋友请直接忽略)：

100字的标准果然很容易做到，虽然每天写对我来说还是比较困难，但还是能看到这种把难度降低带来的明显好处。

教育制度的错误和高考行为，使人们很容易去给自己定一个过高过难的目标，从而使人们特别容易放弃，因为实在太难，人生不看到一点点希望。

做一件困难的事情，成功了当然很帅。但是，在做的过程，容易让人处于一种不健康的心理状态。只要出现一点点意外，原有计划就会很容易变得无可挽回。

最要命的是，如果你非常困难地做一件事，往往是你用错了方法。

所以，当我们觉得事情特别难做到的时候，不妨停下来想想，是不是自己做事的方式错了。