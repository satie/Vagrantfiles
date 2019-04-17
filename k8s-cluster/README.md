# k8s-cluster
Vagrantfile to create a Kubernetes cluster.

## Prerequisites

* [Virtualbox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)

## Usage
The `Vagrantfile` creates a three node cluster with one master and two nodes. To setup the cluster, simply run

```console
$ vagrant up
```

This will create `k8s-master`, `k8s-node-1` and `k8s-node-2` machines.

Once vagrant is done creating the machines, you can `ssh` into the master to verify.

```console
$ vagrant ssh k8s-master
```
```console
vagrant@k8s-master:~$ kubectl get nodes
NAME         STATUS   ROLES    AGE     VERSION
k8s-master   Ready    master   10m     v1.14.1
k8s-node-1   Ready    <none>   8m      v1.14.1
k8s-node-2   Ready    <none>   6m12s   v1.14.1
```
