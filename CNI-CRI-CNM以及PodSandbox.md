k8s网络学习（3）——网络模型&&CNI&&CNM：http://niyanchun.com/k8s-network-3.html

从功能上说，CNI就是定义了创建网络（ADD）和删除网络（DEL）两个接口，各个插件来实现这两个接口。然后CRI在创建容器时创建网络，并调用ADD接口将容器加入该网络；在容器销毁时调用DEL将容器从网络中删除，必要时删除这个网络。

书籍《K8S网络权威指南》

PodSandbox：书籍《K8S权威指南》P95