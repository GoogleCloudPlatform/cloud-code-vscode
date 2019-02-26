# Getting Started

Before you can start using Cloud Code for VS Code you need to be sure your machine
is properly set up.

## Hard Prerequisites

* [Visual Studio Code](https://code.visualstudio.com/) should be installed and set-up on your machine.
* Language support installed and configured.  Our extension works best with these four languages:
    * NodeJS (built in to VS Code)
    * [Go](https://marketplace.visualstudio.com/items?itemName=ms-vscode.Go)
    * [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    * [Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)
* Basic knowledge of VS Code and k8s are highly recommended.


## Installing the Extensions
1. Download the most up to date extensions from the [releases page](https://github.com/GoogleCloudPlatform/vscode-extensions-docs/releases)

1. From within VS Code's extension view:

    ![Extension Viewlet](images/extensionView.png)

1. Click `Install from VSIX...` and browse to the extensions on your disk and install.

    ![Install from VSIX](images/installFromVSIX.png)

## Kubernetes Extension Prerequisites
The following should be installed and on the `PATH` for your machine.

* [Docker Client](https://docs.docker.com/install/)
    * You will also need to be authenticated with your docker registry.
* [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
* [Skaffold](https://github.com/GoogleContainerTools/skaffold#installation)

## Google Cloud Platform and Google Kubernetes Engine Prerequisites
* [gcloud](https://cloud.google.com/sdk/gcloud/) should be installed and on the `PATH`
* You will need to have a GCP account set up with billing.
