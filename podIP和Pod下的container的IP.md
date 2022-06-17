https://coding.imooc.com/learn/questiondetail/96441.html

podIP和Pod下的container的IP是怎么什么关系？我用docker inspect 查看pod中的container的时候，并没有发现containerIP。是不是非静态（通过yaml文件创建，pod作为其上层概念）的container没有自己的IP，只有PodIP？好像静态（通过docker run创建）container是有自己的containerIP的

您好，关于这个podip和里面container ip的关系您可以这样理解，咱们抛开container，回到那个没有container的年代。

假如你现在在一台Linux机器上，这个机器有一个IP地址1.1.1.1， 然后我在这台机器上起了两个进程，一个MySQL，一个Python，你说这两个进程他们如果要对外连接，会用什么IP呢？  会用1.1.1.1，那对内连接呢，会用127.0.0.1。因为这是一台Linux，有一个默认的网络空间，所有的进程默认都会在这个网络空间里。