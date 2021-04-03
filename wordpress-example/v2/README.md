# wordpres
此版本为v2

环境：Kubernetes 1.8.3

## 高可用

现在我们将 Pod 中的两个容器进行拆分，将 Wordpress 和 MySQL 分别部署，然后 Wordpress 用多个副本进行部署就可以实现应用的高可用了，由于 MySQL 是有状态应用，一般来说需要用 StatefulSet 来进行管理，但是我们这里部署的 MySQL 并不是集群模式，而是单副本的，所以用 Deployment 也是没有问题的，当然如果要真正用于生产环境还是需要集群模式的

