
# kubeslice

### Introduction
KubeSlice combines network, application, Kubernetes, and deployment services in a framework to accelerate application deployment in a multi-cluster, multi-tenant environment. KubeSlice achieves this by creating logical application “slice” boundaries which allow pods and services to communicate seamlessly across clusters, clouds, edges, and data centers.

### KubeSlice Features

* Namespace Sameness
* Service Exports and Service Imports
* Micro-Segmentation
* East-West cluster communication
* North-South Ingress Traffic
* Remove IP Addressing Complexity
* QoS Profiling
* Cross cluster Layer 3 secure connectivity
* Network Policy Management
* Multi-Tenancy

### Repositories

* [kubeslice-controller](https://github.com/kubeslice/kubeslice-controller), The KubeSlice Controller orchestrates the creation and management of slices on worker clusters. The KubeSlice Controller components and the worker cluster components can coexist on a cluster. Hence, the cluster running the KubeSlice controller can also be used as a worker cluster.
* [gateway-certs-generator](https://github.com/kubeslice/gateway-certs-generator), This is an opinionated single-file OpenVPN TLS certificate configuration generator for slice gateways. it is an enhancement to easy-rsa (typically bundled with OpenVPN).
* [worker-operator](https://github.com/kubeslice/worker-operator), The KubeSlice Worker Operator is a Kubernetes operator that manages the lifecycle of KubeSlice worker clusters.