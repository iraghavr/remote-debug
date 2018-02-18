# remote-debug
调试是开发过程很重要的过程，而随着移动端的普及，移动开发也越来越多，并且由于移动端的诸多限制，使得调试相对PC复杂很多。因此远程调试就显得非常重要了。本文主要介绍远程调试是什么，基本原理是什么，有哪些情况，以及如何根据不同的情况选择恰当优雅的调试方式。

## 本地调试
远程调试是相对于本地调试来讲的，那么理解本地调试对于理解远程调试是很重要的。
本地调试指的是直接调试运行在本地的APP。比如我在本地运行了一个webpack-dev-server，端口号为8080.
那么访问8080，并且打开浏览器的开发者工具，就可以在本地进行调试了。再比如我要调试google的官网，那么我只需要
访问www.google.com， 同样打开开发者工具就可以进行本地调试了。
## 远程调试
那么远程调试就是调试运行在远程的APP。比如手机上访问google，我需要在PC上调试手机上运行的google APP。
这个就叫做远程调试。

将spy-debugger加入到对比列表

调试：
1. 调试本地PC（很简单）
2. 调试远程PC（本质上是一个debug server 和 一个debug target，其实下面两种也是这种模型，ios中间会多一个协议转化而已）
3. 调试android webview（很多方式，但是本质都是Chrome DevTools Protocol的扩展）
4. 调试ios webview（iOS WebKit Debug Proxy）

参考：
https://www.jianshu.com/p/19c18c924f91
https://aotu.io/notes/2017/02/24/Mobile-debug/index.html
