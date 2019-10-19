# Some question for ref
  ## 1-5
  * 1.列出所有pod，以name字段排序（请使用kubectl原生方法）
  * 2.找出指定pod中的错误日志（会给关键字) 把错误所在行的内容输出到文件中
  * 3.列出所有可调度的节点的个数（不含taint标记）
  * 4.创建一个名为nginx的pod ，并调度到某个节点xx上
  * 5.提供一个pod，添加init container ,在container中添加一个空文件，启动的时候。在另一个containre中检测如果有这个文件，则sleep，否则退出

  ## 6-10
  * 6.在一个pod中创建2个容器，redis+nginx，题目是让你从4个镜像中随意选1-4个
  * 7.pod中挂载 volume
  * 8.找到指定service下的pod中，cpu利用率按高到底排序
  * 9.创建 nginx的pod，再创建一个service node port类型
  * 10.创建nginx为镜像的daemonset

  ## 11-15
  * 11.deployment的副本数 1-4 ，scale命令
  * 12.先将nginx:1.11的deployment，升级到nginx:1.11.3，记录下来(—record)，然后回滚到1.11
  * 13.创建nginx的pod，和service，使用ns lookup 查看service 和pod的dns
  * 14.创建secret，有一个paasword字段（手动base64加密或from-file命令），创建两个pod引用该secret，一个用env ,一个用volume来调用
  * 15.node节点异常，排查一下：kubelet没启动

  ## 16-20
  * 16.etcdctl 来 备份etcd
  * 17.static pod的使用
  * 18.pv 类型hostpath 位置在/data ， 大小为1G , readonly模式
  * 19.排查apiserver连接不上问题：用的kubeadmin安装的，因此不用去master机器的systemctl去找，是kubelet的配置中目录地址有问题，修改正确目录后等待一下就好了（4分）
  * 20.在一个新的namespace创建pod

  ## 21-25
  * 21.把一个node弄成unavailable 并且把上边的pod重新调度去新的node上
  * 22.给pod创建service
  * 23.使用nodeselector，选择disk为ssd的机器调度
  * 24.tls bootstrap加入节点（题目写的像论文，时间不够直接放弃了，这题8分）





