# Kubernetes (K8s)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/569/badge)](https://bestpractices.coreinfrastructure.org/projects/569) [![Go Report Card](https://goreportcard.com/badge/github.com/kubernetes/kubernetes)](https://goreportcard.com/report/github.com/kubernetes/kubernetes) ![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/kubernetes/kubernetes?sort=semver)

<img src="https://github.com/kubernetes/kubernetes/raw/master/logo/logo.png" width="100">

----

## 项目介绍

Kubernetes (简称 K8s) 是一个开源的容器编排平台，用于自动化部署、扩展和管理容器化应用程序。它构建于 Google 十五年大规模生产环境容器化工作负载管理经验之上，结合了社区的最佳实践和创新理念。

### 核心特性：

* **自动化部署与回滚**：支持声明式配置，轻松部署应用，支持滚动更新和自动回滚失败的部署

* **服务发现与负载均衡**：内置 DNS 和负载均衡，无需修改应用即可实现服务间通信

* **存储编排**：自动挂载各种存储系统，包括本地存储、云存储、网络存储等

* **自动扩缩容**：根据 CPU 使用率或自定义指标自动调整应用副本数

* **自我修复**：自动重启失败的容器，替换和重新调度节点故障的 Pods，杀死健康检查失败的容器

* **密钥与配置管理**：部署和更新密码、OAuth token 和 SSH key 等敏感信息

* **批量执行**：支持一次性任务和批处理工作负载

### 核心架构

Kubernetes 由以下核心组件组成：

* **控制平面（Control Plane）
  * kube-apiserver：集群的统一入口，提供 REST API
  * etcd：集群的键值数据库，存储集群状态
  * kube-scheduler：Pod 调度器，决定 Pod 在哪个节点运行
  * kube-controller-manager：运行控制器，维护集群状态

* **节点组件（Node Components）
  * kubelet：运行在每个节点上的代理，管理容器生命周期
  * kube-proxy：网络代理，维护网络规则
  * 容器运行时：如 Docker、containerd、CRI-O

Kubernetes 由云原生计算基金会 ([CNCF]) 托管。如果贵公司希望参与推动容器打包、动态调度和微服务技术的发展，欢迎加入 CNCF。
详情请参阅 CNCF [公告]。

----

## To start using K8s

See our documentation on [kubernetes.io].

Take a free course on [Scalable Microservices with Kubernetes].

To use Kubernetes code as a library in other applications, see the [list of published components](https://git.k8s.io/kubernetes/staging/README.md).
Use of the `k8s.io/kubernetes` module or `k8s.io/kubernetes/...` packages as libraries is not supported.

## To start developing K8s

The [community repository] hosts all information about
building Kubernetes from source, how to contribute code
and documentation, who to contact about what, etc.

If you want to build Kubernetes right away there are two options:

##### You have a working [Go environment].

```
git clone https://github.com/kubernetes/kubernetes
cd kubernetes
make
```

##### You have a working [Docker environment].

```
git clone https://github.com/kubernetes/kubernetes
cd kubernetes
make quick-release
```

For the full story, head over to the [developer's documentation].

## Support

If you need support, start with the [troubleshooting guide],
and work your way through the process that we've outlined.

That said, if you have questions, reach out to us
[one way or another][communication].

[announcement]: https://cncf.io/news/announcement/2015/07/new-cloud-native-computing-foundation-drive-alignment-among-container
[Borg]: https://research.google.com/pubs/pub43438.html?authuser=1
[CNCF]: https://www.cncf.io/about
[communication]: https://git.k8s.io/community/communication
[community repository]: https://git.k8s.io/community
[containerized applications]: https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/
[developer's documentation]: https://git.k8s.io/community/contributors/devel#readme
[Docker environment]: https://docs.docker.com/engine
[Go environment]: https://go.dev/doc/install
[kubernetes.io]: https://kubernetes.io
[Scalable Microservices with Kubernetes]: https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615
[troubleshooting guide]: https://kubernetes.io/docs/tasks/debug/

## Community Meetings 

The [Calendar](https://www.kubernetes.dev/resources/calendar/) has the list of all the meetings in the Kubernetes community in a single location.

## Adopters

The [User Case Studies](https://kubernetes.io/case-studies/) website has real-world use cases of organizations across industries that are deploying/migrating to Kubernetes.

## Governance 

Kubernetes project is governed by a framework of principles, values, policies and processes to help our community and constituents towards our shared goals.

The [Kubernetes Community](https://github.com/kubernetes/community/blob/master/governance.md) is the launching point for learning about how we organize ourselves.

The [Kubernetes Steering community repo](https://github.com/kubernetes/steering) is used by the Kubernetes Steering Committee, which oversees governance of the Kubernetes project.

## Roadmap 

The [Kubernetes Enhancements repo](https://github.com/kubernetes/enhancements) provides information about Kubernetes releases, as well as feature tracking and backlogs.
