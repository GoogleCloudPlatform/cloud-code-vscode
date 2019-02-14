# Minikube support
You can use this wizard to start/stop and get status of a Minikube cluster. It would take ~5 minutes to bring up the local cluster.

## Prerequisites
1. All the prerequisites mentioned [here](https://kubernetes.io/docs/tasks/tools/install-minikube/#before-you-begin) are met.
2. Minikube binary is added to PATH variable or to `"cloudcode.minikubePath"` VSCode setting.

## Dashboard
![Dashboard](images/minikube/dashboard.png)

## Starting minikube cluster
You need to choose the VM driver that will be used to create the Minikube cluster. The current list of supported VM drivers are:
    `['virtualbox', 'vmwarefusion', 'kvm', 'xhyve', 'hyperv', 'hyperkit', 'kvm2', 'none']`

You can pass additional flags to the `minikube start` command using the 'Additional Flags' field.

![Starting cluster](images/minikube/starting.gif)

## Stopping minikube cluster
![Stopping cluster](images/minikube/stopping.gif)

## Status of minikube cluster
![Cluster status](images/minikube/status.gif)