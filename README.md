# kubernetes-best-practices
A curated list of best practices learned the hard way by operating multiple kubernetes cluster at different customers at large scale

### Max Number of Pods per Node

It is recommended: No more than 110 pods per node

[Building Large Cluster](https://kubernetes.io/docs/admin/cluster-large/)

### kube-reserved & system-reserved

To provide more reliable scheduling and minimize node resource overcommitment, each node can reserve a portion of its resources for use by all underlying node components (e.g., kubelet, kube-proxy, Docker) and the remaining system components (e.g., sshd, NetworkManager) on the host. Once specified, the scheduler has more information about the resources (e.g., memory, CPU) a node has allocated for pods.

[Allocating Node Resources](https://docs.openshift.org/latest/admin_guide/allocating_node_resources.html)

