# Kubernetes Explorer

### Clusters

Set as Active Cluster - Enable you too easily interact with them in the Kubernetes explorer.

![Set as Active Cluster ](images/kubernetes-explorer/k8s-set.png)

Open Dashboard - Open the kubernetes dashboard for that cluster.

![Open Dashboard](images/kubernetes-explorer/k8s-open-dashboard.png)

### Deployments

Add Secret as Environment Variable - Add an existing Kubernetes (secret)[https://kubernetes.io/docs/concepts/configuration/secret/] to the deployment as an environment variable.

![Add Secret as Environment Variable](images/kubernetes-explorer/addSecretAsEnv.gif)

Mount Secret as Volume - Mount an existing Kubernetes (secret)[https://kubernetes.io/docs/concepts/configuration/secret/] as a volume in the deployment's container.

![Mount Secret as Volume](images/kubernetes-explorer/mountSecretAsVolume.gif)

### Pods

Stream Logs - Stream logs from a pod. If there are multiple containers in the pod, you will be asked to select one.

![Stream Logs from Pod](images/kubernetes-explorer/streamLogsFromPod.gif)

View Logs - View logs from a pod. If there are multiple containers in the pod, you will be asked to select one.

![View Logs from Pod](images/kubernetes-explorer/viewLogsFromPod.gif)

### Containers

Stream Logs - Same as above

View Logs - Same as above

Get Terminal - Open an interactive terminal to the container.

![Get Terminal from Container](images/kubernetes-explorer/getTerminalFromContainer.gif)

### Services

For `External IP` object, you can click on a button to open the address in a web browser.

![Open External IP Address](images/kubernetes-explorer/openExternalIP.gif)

### Secrets

Clicking on secret object will display the decoded secret as a file.
