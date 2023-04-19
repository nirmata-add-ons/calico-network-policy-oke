# calico-network-policy-oke

This README documents the calico network policy for oke integration as Nirmata add-on on Kubernetes clusters.

### What is Calico?
Calico is an open source networking and network security solution for containers, virtual machines, and native host-based workloads. For more information about Calico, see the Calico documentation [here](https://projectcalico.docs.tigera.io/about/about-calico).

### Installing Calico alongside the OCI VCN-Native Pod Networking CNI plugin
Having created a cluster using Container Engine for Kubernetes (using either the Console or the API) and selected VCN-native pod networking as the Network type, you can subsequently install Calico on the cluster alongside the OCI VCN-Native Pod Networking CNI plugin to support network policies.

### How do I get set up?
1. Clone this repository or add its contents to your own private Git repository.
2. Create a Nirmata catalog application with a Git upstream and select the calico-network-policy-oke repository. You can optionally select the kustomization.
3. Edit the catalog application and select an add-on category (e.g. Networking). This is required to select the application as a add-on.
4. Update a Cluster Type, or create a new one, and select the Calico add-on application in the "Add-Ons" section. Ensure that the namespace you use is "**kube-system**" and environment is "kube-system-< cluster-name >"
5. Create clusters using the cluster type.
6. If addon is to be added to a running cluster, It will be added to "**kube-system**" namespace.
7. Verify that the application is running.

### Who do I talk to?
For issues, contact support@nirmata.com
