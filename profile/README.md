![KubeSlice](https://user-images.githubusercontent.com/99885802/169118120-1636d01b-b9d9-474c-9d08-ff54c8be0d2a.png)

# What is KubeSlice

- KubeSlice enables [Kubernetes](https://kubernetes.io) pods and services to communicate seamlessly across clusters, clouds, edges, and data centers by creating logical application boundaries known as **Slices**. 
- It combines network, application, and deployment services in a framework to accelerate application deployment in a multi-cluster, multi-tenant environment. 

# Getting Started

There are several ways to get started with KubeSlice.

 - :books: Read our [documentation]().
 - :computer: View the [Getting Started with KubeSlice]() on YouTube.
 - [![](https://gitpod.io/button/open-in-gitpod.svg)]()


# Architecture

KubeSlice creates a flat overlay network to connect Kubernetes clusters. The overlay network can be described as an application slice that provides a slice of connectivity between the pods of an application running in multiple clusters.  

![Architecture](https://cdn.avesha.io/cms-assets-local/Architecture_OS_f4ebbbda38.png)

The core components of KubeSlice are detailed below with links to their respective GitHub repos.

* [kubeslice-controller](https://github.com/kubeslice/kubeslice-controller) -  The KubeSlice Controller orchestrates the creation and management of slices on worker clusters. The KubeSlice Controller components and the worker cluster components can coexist on a cluster. Hence, the cluster running the KubeSlice controller can also be used as a worker cluster.
* [gateway-certs-generator](https://github.com/kubeslice/gateway-certs-generator) - This is an opinionated single-file OpenVPN TLS certificate configuration generator for slice gateways. it is an enhancement to easy-rsa (typically bundled with OpenVPN).
* [worker-operator](https://github.com/kubeslice/worker-operator) - the KubeSlice Worker Operator is a Kubernetes operator that manages the lifecycle of KubeSlice worker clusters.
* [charts](https://github.com/kubeslice/charts) - It contains applications provided by Avesha Systems that are ready to launch on Kubernetes using the Kubernetes Helm.
* [netops](https://github.com/kubeslice/netops) - The NetOp Pods enforce the QoS Profile for a Slice. It uses Linux TC (Traffic Control) for Slice traffic classification.
* [gateway-sidecar](https://github.com/kubeslice/gateway-sidecar) - The slice VPN Gateway is a slice network service component that provides a secure VPN tunnel between any two clusters that are a part of the slice.
* [router-sidecar](https://github.com/kubeslice/router-sidecar) - The slice Router is a network service component that provides a virtual L3 IP routing functionality within a cluster for the Slice overla network.
* [apis](https://github.com/kubeslice/apis) - The kubeslice API is a part of the Kubeslice Controller, and this repository contains the scaffolding of all Custom Resource Definitions (CRDs).


# :woman_technologist: Contribute!

We welcome contributions of any kind (pun fully intended). To start contributing to our documentation, check out the [Documentation contribution guide](). For contributing to the codebase, check out the [Project contribution guide](). If you have any questions, please feel free to reach out to us on the [KubeSlice Slack channel]().

# Community

Come hang out with us on the [KubeSlice channel]() in the [Kubernetes Slack](). Follow us on [Twitter]() and [Reddit]().


# 🙏 Support

Don't forget to leave a star ⭐️ or fork the 
