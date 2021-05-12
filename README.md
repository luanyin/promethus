# promethus

# 介绍

kube-metrics用于[`client-go`](https://github.com/kubernetes/client-go)与Kubernetes集群通信。支持的Kubernetes集群版本由决定`client-go`。可以在[此处](https://github.com/kubernetes/client-go#compatibility-matrix)找到client-go和Kubernetes集群的兼容性矩阵 。

#### 相容性矩阵

最多将在下面记录5个kube-metrics和5个[kubernetes版本](https://github.com/kubernetes/kubernetes/releases)。.

| kube-metrics | **Kubernetes 1.17** | **Kubernetes 1.18** | **Kubernetes 1.19** | **Kubernetes 1.20** | **Kubernetes 1.21** |
| ------------ | ------------------- | ------------------- | ------------------- | ------------------- | ------------------- |
| **v1.8.0**   | -                   | -                   | -                   | -                   | -                   |
| **v1.9.8**   | -                   | -                   | -                   | -                   | -                   |
| **v2.0.0**   | -/✓                 | -/✓                 | ✓                   | ✓                   | -/✓                 |
| **master**   | -/✓                 | -/✓                 | ✓                   | ✓                   | ✓                   |

- `✓` 完全支持的版本范围。
- `-` Kubernetes群集具有客户端库无法使用的功能（其他API对象，已弃用的API等）。

**注意：** kube-metrics的`v2.0.0-alpha.2+`和`master`版本在Kubernetes v1.17和v1.18上有效，但不包括Ingress或CertificateSigningRequest资源指标。如果您需要这些指标并且使用的是较早的Kubernetes版本，请使用v2.0.0-alpha.1或v1.9.8 kube-metrics版本。

# 用法

```
cd kubernetes/examples/kube-metrics
kubectl apply -f .

```



# 用法

安装插件kube-metrics

```
cd kubernetes/examples/kube-metrics
kubectl apply -f .
```

安装完kube-metrics之后，安装promethus

```
cd kubernetes/examples/promethus
kubectl apply -f .
```

