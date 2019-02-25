# Kubernetes Explorer

Our extension contributes an explorer to the VS Code activity bar.  This is powered by `kubectl` under the covers and will work on any supported cluster.

To navigate there click on this icon:

![K8s explorer icon](images/explorerIcon.png)

From here, you can access your K8s clusters and run a variety of commands, allowing you to interact with K8s resources in a unique and simple way.

![K8s explorer](images/clusterExplorer.png)

Most resources have three basic functions (on top of others listed below):
- Copy Resource Name - Copy the name to the clipboard for easy use
- Describe - Do a `kubectl describe` of the resource.
- Delete - Delete the resource.

![Basic Commands](images/k8s-basic.png)

## Clusters

Set as Active Cluster - Enable you too easily interact with them in the Kubernetes explorer.

![Set as Active Cluster ](images/kubernetes-explorer/k8s-set.png)

Open Dashboard - Open the kubernetes dashboard for that cluster.

![Open Dashboard](images/kubernetes-explorer/k8s-open-dashboard.png)

## Deployments

Add Secret as Environment Variable - Add an existing Kubernetes (secret)[https://kubernetes.io/docs/concepts/configuration/secret/] to the deployment as an environment variable.

![Add Secret as Environment Variable](images/kubernetes-explorer/addSecretAsEnv.gif)

Mount Secret as Volume - Mount an existing Kubernetes (secret)[https://kubernetes.io/docs/concepts/configuration/secret/] as a volume in the deployment's container.

![Mount Secret as Volume](images/kubernetes-explorer/mountSecretAsVolume.gif)

## Pods

Stream Logs - Stream logs from a pod. If there are multiple containers in the pod, you will be asked to select one.

![Stream Logs from Pod](images/kubernetes-explorer/streamLogsFromPod.gif)

View Logs - View logs from a pod. If there are multiple containers in the pod, you will be asked to select one.

![View Logs from Pod](images/kubernetes-explorer/viewLogsFromPod.gif)

## Containers

Stream Logs - Same as above

View Logs - Same as above

Get Terminal - Open an interactive terminal to the container.

![Get Terminal from Container](images/kubernetes-explorer/getTerminalFromContainer.gif)

## Services

For `External IP` object, you can click on a button to open the address in a web browser.

![Open External IP Address](images/kubernetes-explorer/openExternalIP.gif)

## Secrets

Clicking on secret object will display the decoded secret as a file.
