# Kube Code - Start Here

This doc will be shorted over time but it's the 'set-up' and pre-req doc.  Our best experience today will be for:

1. Node
2. Go
3. Python
4. Java

In that order as VS Code itself is best for those.


# Hard Pre-reqs

You won't get far without these - we can help but these will be base assumptions...

- [VS Code installed](https://code.visualstudio.com/) and set-up for your OS e.g. on PATH
- Language support installed and configured for VS code i.e. [Go](https://marketplace.visualstudio.com/items?itemName=ms-vscode.Go), Node (built in), [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) or [Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)
- Basic knowledge of VS Code and K8's we are not attempting to cover that


# Installing the extensions
Download the most up to date extensions from the [releases page](https://github.com/GoogleCloudPlatform/vscode-extensions-docs/releases)

From within VS Code's extension view:

![Extension Viewlet](images/extensionView.png)

Click install from VSIX and browse to the extensions on your disk.  Install each separately and then reload VS Code.

![Install from VSIX](images/installFromVSIX.png)

## Kubernetes Extension Pre-reqs 

- Docker client should be [`installed`](https://docs.docker.com/install/), added to the path and logged into a docker registry.
- Kubectl should be [`installed`](https://kubernetes.io/docs/tasks/tools/install-kubectl/), added to the path and connected to a cluster.
- Skaffold client should be [`installed`](https://github.com/GoogleContainerTools/skaffold#installation) and added to the path.

# GCP Pre-reqs

- An account
- Billing enabled
- Kubernetes enabled (kubectl installed)

## Welcome Experience

This is the leap off point for several of the getting started and update features.  

Specifically:
- New Project
- Start from sample
- Add additional cloud support
- Jump to docs
- File an issue
- See whats new

![KubeCode welcome](images/help.png)

> TODO: Missing content and code...
