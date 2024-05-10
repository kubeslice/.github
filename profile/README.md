![KubeSlice](https://user-images.githubusercontent.com/99885802/169118120-1636d01b-b9d9-474c-9d08-ff54c8be0d2a.png)

# What is KubeSlice

- KubeSlice enables [Kubernetes](https://kubernetes.io) pods and services to communicate seamlessly across clusters, clouds, edges, and data centers by creating logical application boundaries known as **Slices**. 
- It combines network, application, and deployment services in a framework to accelerate application deployment in a multi-cluster, multi-tenant environment. 

# Why would I want that?

Today Kubernetes is mainly known as a container orchestration platform. However, as enterprises expand application architectures to span multiple clusters located in data centers or cloud provider regions, or across cloud providers, Kubernetes clusters need the ability to fully integrate connectivity and pod-to-pod communications with namespace propagation across clusters.

Imagine enabling communication between clusters regardless of their physical location and without having to worry about IP addressing overlap. That's what KubeSlice achieves along with ensuring that your existing intra-cluster communication remains local. 

How do we do it? With the help of an overlay network that creates network isolation. Let KubeSlice worry about the responsibility of allocating subnets that are configurable based on the number of pods allocated to have inter-cluster reachability.

# Getting Started

There are several ways to get started with KubeSlice.

 - 💽🫀: Try our [Sandbox](https://kubeslice.io/documentation/open-source/1.3.0/playground/sandbox) environment for four-hour free access. 
 - 📓🔖 Try our [kubeslice-cli tutorials](https://kubeslice.io/documentation/open-source/1.3.0/category/kubeslice-cli-tutorials/).
 - :books: Read our [documentation](https://kubeslice.io).
 - :computer: :construction: View the [Getting Started with KubeSlice](https://www.youtube.com/watch?v=HNicEasUns0) video on YouTube.
 - :technologist: Get your hands dirty by trying out some [examples](https://github.com/kubeslice/examples).
 
# Can I start using KubeSlice?

Yes! We have several organizations currently running KubeSlice in their test & lab environments. We would love for you to try it out and [provide feedback](#woman_technologist-this-sounds-awesome-and-i-want-to-help). 

:notebook:
An enterprise edition of KubeSlice is also available. Please feel free to contact sales@avesha.io for more information on the enterprise edition. 

# Architecture

KubeSlice is a framework that brings both multi-tenancy and multi-cluster capabilities to Kubernetes by creating a flat overlay network to connect clusters. 

The overlay network can be described as an application slice that provides a slice of connectivity between the pods of an application running in multiple clusters. 

For more information, see [KubeSlice architecture](https://kubeslice.io/documentation/open-source/1.3.0/overview/architecture). 

![Architecture](https://cdn.avesha.io/cms-assets-local/Architecture_OS_f4ebbbda38.png)

The core components of KubeSlice are detailed below with links to their respective GitHub repos.

* [kubeslice-controller](https://github.com/kubeslice/kubeslice-controller) -  The KubeSlice Controller orchestrates the creation and management of slices on worker clusters. The KubeSlice Controller components and the worker cluster components can coexist on a cluster. Hence, the cluster running the KubeSlice controller can also be used as a worker cluster.
* [gateway-certs-generator](https://github.com/kubeslice/gateway-certs-generator) - This is an opinionated single-file OpenVPN TLS certificate configuration generator for slice gateways. it is an enhancement to easy-rsa (typically bundled with OpenVPN).
* [worker-operator](https://github.com/kubeslice/worker-operator) - the KubeSlice Worker Operator is a Kubernetes operator that manages the lifecycle of KubeSlice worker clusters.
* [charts](https://github.com/kubeslice/kubeslice) - It contains charts provided by Avesha Systems that are ready to launch on Kubernetes using the Kubernetes Helm.
* [netops](https://github.com/kubeslice/netops) - The NetOp Pods enforce the QoS Profile for a Slice. It uses Linux TC (Traffic Control) for Slice traffic classification.
* [gateway-sidecar](https://github.com/kubeslice/gateway-sidecar) - The slice VPN Gateway is a slice network service component that provides a secure VPN tunnel between any two clusters that are a part of the slice.
* [router-sidecar](https://github.com/kubeslice/router-sidecar) - The slice router is a network service component that provides a virtual L3 IP routing functionality within a cluster for the slice overlay network.
* [apis](https://github.com/kubeslice/apis) - The kubeslice API is a part of the Kubeslice Controller, and this repository contains the scaffolding of all Custom Resource Definitions (CRDs).


# :woman_technologist: This sounds awesome and I want to help!!

Welcome, we're so glad you're onboard!

Check our :construction: [Project Contribution Guide](https://github.com/kubeslice/docs/blob/master/CONTRIBUTING.md) if there's any feedback/issue you want to flag with the codebase.

We also have a :construction: [Documentation Contribution Guide](https://github.com/kubeslice/docs/blob/master/developer_guide.md) for those looking to help better the documentation. 

You can also reach us here, on GitHub, via [discussions](https://github.com/orgs/kubeslice/discussions) or join our [bi-weekly developer meetings](https://calendar.google.com/calendar/event?action=TEMPLATE&tmeid=M2psOWMzcmdxcjJrdWxoZWJ0cHI1cG5rMGVfMjAyNDA1MTZUMTQwMDAwWiBlcmljQGF2ZXNoYXN5c3RlbXMuY29t&tmsrc=eric%40aveshasystems.com&scp=ALL) or

1. Join our mailing lists
 - [kubeslice-dev](https://groups.google.com/g/kubeslice-dev/) for development discussions
 - [kubeslice-users](https://groups.google.com/g/kubeslice-users/) for discussions among users & potential users.
2. Join the **#kubeslice** channel on the [Kubernetes Slack](https://slack.k8s.io)
3. Follow us on [Twitter](https://twitter.com/kube_slice) & [Reddit](https://www.reddit.com/user/kubeslice/) for the latest updates!
4. Please consider supporting further development of this project by [starring the repo](https://github.com/kubeslice/kubeslice) ⭐ 
