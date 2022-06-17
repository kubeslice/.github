![KubeSlice](https://user-images.githubusercontent.com/99885802/169118120-1636d01b-b9d9-474c-9d08-ff54c8be0d2a.png)
# KubeSlice  
KubeSlice combines network, application, Kubernetes, and deployment services in a framework to accelerate application deployment in a multi-cluster, multi-tenant environment. KubeSlice achieves this by creating logical application _slice_ boundaries which allow pods and services to communicate seamlessly across clusters, clouds, edges, and data centers.


# Overview

KubeSlice is a framework to bring both multi-tenancy and multi-cluster capabilities to Kubernetes. For more information, see [overview](https://docs.avesha.io/documentation/open-source/0.2.0/kubeslice-overview).

# Architecture
KubeSlice provides network services to applications that need secure and highly available connectivity between multiple clusters. KubeSlice creates a flat overlay network to connect the clusters. The overlay network can be described as an application slice that provides a slice of connectivity between the pods of an application running in multiple clusters. For more information, see [KubeSlice architecture](https://docs.avesha.io/documentation/open-source/0.2.0/kubeslice-architecture). 

# Repositories
* [kubeslice-controller](https://github.com/kubeslice/kubeslice-controller) -  The KubeSlice Controller orchestrates the creation and management of slices on worker clusters. The KubeSlice Controller components and the worker cluster components can coexist on a cluster. Hence, the cluster running the KubeSlice controller can also be used as a worker cluster.
* [gateway-certs-generator](https://github.com/kubeslice/gateway-certs-generator) - This is an opinionated single-file OpenVPN TLS certificate configuration generator for slice gateways. it is an enhancement to easy-rsa (typically bundled with OpenVPN).
* [worker-operator](https://github.com/kubeslice/worker-operator) - the KubeSlice Worker Operator is a Kubernetes operator that manages the lifecycle of KubeSlice worker clusters.
* [charts](https://github.com/kubeslice/charts) - It contains applications provided by Avesha Systems that are ready to launch on Kubernetes using the Kubernetes Helm.
* [netops](https://github.com/kubeslice/netops) - The NetOp Pods enforce the QoS Profile for a Slice. It uses Linux TC (Traffic Control) for Slice traffic classification.
* [gateway-sidecar](https://github.com/kubeslice/gateway-sidecar) - The slice VPN Gateway is a slice network service component that provides a secure VPN tunnel between any two clusters that are a part of the slice.
* [router-sidecar](https://github.com/kubeslice/router-sidecar) - The slice Router is a network service component that provides a virtual L3 IP routing functionality within a cluster for the Slice overla network.
* [apis](https://github.com/kubeslice/apis) - The kubeslice API is a part of the Kubeslice Controller, and this repository contains the scaffolding of all Custom Resource Definitions (CRDs).
* [examples](https://github.com/kubeslice/examples) - KubeSlice usage example scripts and tools


# Quick Start

A quick and easy way to explore KubeSlice is to install it on _kind_ clusters.  
For more information, see [getting started with kind clusters](https://docs.avesha.io/documentation/open-source/0.2.0/getting-started-with-kind-clusters)... or try out the example script in [kind-based example](https://github.com/kubeslice/examples/tree/master/kind).

For information on installing KubeSlice on cloud clusters, see [getting started with cloud clusters](https://docs.avesha.io/documentation/open-source/0.2.0/getting-started-with-cloud-clusters).

# Community 
Join the KubeSlice community to learn and post your questions to get them answered. Learn more about the [community](https://docs.avesha.io/documentation/open-source/0.2.0/community).

# Enterprise Edition
For details on purchasing an enterprise edition of KubeSlice, reach us at sales@avesha.io.
