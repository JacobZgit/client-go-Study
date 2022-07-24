https://zhuanlan.zhihu.com/p/425135444

当需要在节点上创建或销毁容器时，kubelet 会向运行在节点 CRI 实例上的 gRPC服务器发送消息以执行操作，然后 CRI 与安装在工作节点上的容器运行时引擎交互以执行操作

为什么要使用gRPC(快的原因)？
https://zhuanlan.zhihu.com/p/99740971?ivk_sa=1024320u

https://blog.csdn.net/weixin_40580582/article/details/118661409