TOPIC: Asynchronous

# 异步

**异步**这个概念指同一时间不止一个事件发生（**并发**），或者说是多个相关事件不等待前一事件完成就发生（**不阻塞**）。计算机技术中，异步一词用于两大背景。

## 网络与通信

异步通信用来在双方或多方之间交流信息。当接收和处理信息不难或可以进行时，各方才会接收和处理信息，而非接收信息后立马执行。此外，信息可能发送后不等待确认通知，因为其明白如果有问题出现，那么接受者会请求修正，要不就处理情况。

对人类来说，电子邮件就是一种异步通信方式；发送者发送一封邮件，接着接收者方便时读取和回复该邮件，而非立马这样做。双方可以继续随意发送和接收信息，而非必须安排何时进行。

软件异步通信时，程序可能会向另一软件（如服务器）请求信息，在等待回复的同时会进行其它行为。例如，[[AJAX]](Asynchronous JavaScript and XML)编程技术利用HTTP向服务器请求较少数据，结果不立即返回，而是在易于获得时返回。（现在通常简写为"*Ajax*"，不过现在的应用不常用[[XML]]，而是用[[JSON]]）。

## 软件设计

异步程序设计更为详细地阐释该概念，其编写的代码使程序能够要求一项任务和原先任务一起运行，不需停止任务去等待另一任务完成。第二项任务完成时，原先的任务利用一个约定好的机制得到通知，这样得知任务完成，可以的话就返回结果。
