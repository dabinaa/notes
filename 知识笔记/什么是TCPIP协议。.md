### 什么是TCP/IP协议。

为什么已经存在唯一的MAC地址，还需要IP地址？



#### 什么是TCP/IP协议？

TCP/IP协议中文名翻译为：传输控制协议/因特网互联协议，它不仅仅只是包含了TCP、IP这两个协议，它里面包含了很多其他的协议，如：HTTP、HTTPS、FTP等等。严格意义上来讲他是一个协议族。只是里面就TCP和IP最为核心的协议，所以我们称之为：TCP/IP协议。

​		打个比方：阿里系代表的不仅仅是阿里巴巴这一个公司，而是里面阿里巴巴最为核心，所以我们将他下面的所有公司统称为：阿里系。

#### TCP/IP协议的结构是什么样子的？

​		简单的分为：应用层、传输层、网络层、链路层。不知道多少人和我一样大学学的是七层传输协议，刚学的时候一直傻傻的分不清，折磨死我了。不过ISO/OSI的七层传输协议终于过时了。已经被淘汰了。挺开心的。

好的接下来我们简单讲讲这四层都是干嘛的：

##### 链路层：

​		我们知道单个的0/1无论是对于我们还是对与机器来讲都是没有意义的，而链路层就是以字节为单位将0和1进行分组，定义数据帧，写入源和目标机器的物理地址、数据、检验位来传输数据。简单的来讲：链路层就是将无意义的0/1变成有意义的数据帧，再通过广播的形式通过物理介质发送给对方。



##### 网络层：

​		这一层就要就是干了三件事：1、根据IP定义网络地址，区分网段。2、子网内根据地址解析协议，进行MAC地址寻址。3、子网外进行路由转发数据包，这个数据包就是IP数据包。





​		网络层的主要工作是**定义网络地址，区分网段，子网内MAC寻址，对于不同子网的数据包进行路由。**



##### 传输层:

​		数据包通过网络层发送到目标计算机后，应用程序在传输层定义逻辑端口，确认身份后，将数据包交给应用程序，实现端口到端口的通信。





​		传输层的主要工作是**定义端口，标识应用程序身份，实现端口到端口的通信，TCP协议可以保证数据传输的可靠性**



##### 应用层:

​		传输层的数据到达应用程序的时候，以某种统一规定的协议格式解读数据。







##### 总结就是：

​		应用层按照既定的协议进行打包数据，通过传输层加上双方的端口号，网络层加上双方的IP地址，链路层加上双方的MAC地址，并将数据拆分为数据帧，经过多个路由器以及网关后，到达目标机器。









