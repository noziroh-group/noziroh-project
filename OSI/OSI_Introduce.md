# Open System Interconnection Model
> 开放式系统互联模型

该模型将操作系统中的数据流划分为七个层，每个中间层为其上一层提供功能，其自身功能则由其下一层提供。功能的类别通过标准的通信协议在软件中实现。

- [应用层（Application Layer）](ApplicationLayer.md) 提供为应用软件而设计的接口，网络通讯的最顶层层级。
- 表示层（Presentation Layer）把数据转换为能与接收者的系统格式兼容并适合传输的格式。
- 会话层（Session Layer）负责在数据传输中设置和维护计算机网络中两台计算机之间的通信连接。
- 传输层（Transport Layer）把传输表头（TH）加至数据以形成数据包。传输表头包含了所使用的协议等发送信息。
- 网络层（Network Layer）决定数据的路径选择和转寄，将网络表头（NH）加至数据包，以形成分组。网络表头包含了网络资料。
- 数据链路层（Data Link Layer）负责网络寻址、错误侦测和改错。
- 物理层（Physical Layer）在局部局域网上发送数据帧（Data Frame），它负责管理电脑通信设备和网络媒体之间的互通。

## 参考文献：
- [wikipedia: OSI](https://zh.wikipedia.org/wiki/OSI%E6%A8%A1%E5%9E%8B#%E7%AC%AC7%E5%B1%A4_%E6%87%89%E7%94%A8%E5%B1%A4)
- [wikipedia: IP协议族](https://zh.wikipedia.org/wiki/TCP/IP%E5%8D%8F%E8%AE%AE%E6%97%8F)