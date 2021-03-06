## NIO
一种同步非阻塞的高效IO交互模型，比同步阻塞IO区别如下：

1. 通过缓冲区而非流的方式进行数据的交互，流是进行直接的传输的没有对数据操作的余地，缓冲区提供了灵活的数据处理方式。
2. NIO是非阻塞的，意味着每个socket连接可以让底层操作系统帮我们完成而不需要每次开个线程去保持连接，使用的是selector监听所有channel的状态实现。
3. NIO提供直接内存复制方式，消除了JVM与操作系统之间读写内存的损耗。

### 同步异步、阻塞非阻塞
同步和异步在于多个任务执行过程中，后发起的任务是否必须等先发起的任务完成之后再进行，是方法被调用的顺序。

阻塞和非阻塞在于请求的方法是否立即返回，是方法被执行的方式。
