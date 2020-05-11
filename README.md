# Cloud Code for Visual Studio Code

Cloud Code for VS Code brings the power and convenience
of IDEs to developing cloud-native Kubernetes and Cloud Run applications.
Cloud Code works with Google’s command-line [container tools][1] like [`skaffold`][2]
and [`kubectl`][3] under the hood, providing local, continuous feedback on your project
as you build, edit, and run your applications on your workstation or in the cloud.
Additionally, its support for [deployment profiles][4] lets you define different
environments, like local development, shared development, test, and production, to
easily test and debug your app with, locally or in the cloud.

## New App, Deploy and Debug

With Cloud Code, you can create a new application, deploy it to a remote Kubernetes
cluster, and debug your running app in seconds!

![New App, Deploy and Debug][12]

## Key Features

- Support for Go, Node, Java, and Python
- Integrated Debugging and Log Viewing/Streaming
- Profile support for dev, test, and production environments
- Cluster and service inspection with the Kubernetes and Cloud Run explorers
- Cluster creation supporting Google GKE, Amazon EKS and Azure AKS
- Rapid Edit, Package, Deploy loop to your K8s cluster
- Snippets, completions, and linting for K8s artifacts
- Support for Custom Resources (CRDs) e.g. Istio, Knative
- Automatically uses your Google Cloud SDK credentials

## Resources

- [Learn More][9]: Learn more about the Cloud Code project and what it has to offer.
- [Documentation][5]: We have a lot of features to explore head over to our documentation to find out.
- [FAQ][11]: A list of frequently asked questions you may run into.
- [Prerequisites][10]: A list of prerequisites to use the Cloud Code for VS Code.
- [Sample Applications][6]: We have starter applications for Node, Python, Go, C# and Java.
- [File an Issue][7]: If you discover an issue please file a bug and we will fix it as soon as possible.
- [Request a Feature][8]: If you have any feature requests, ideas for improvement and general feedback please submit a feature request.

[1]: https://github.com/GoogleContainerTools
[2]: https://skaffold.dev/
[3]: https://kubernetes.io/docs/tasks/tools/install-kubectl/
[4]: https://skaffold.dev/docs/how-tos/profiles/
[5]: https://cloud.google.com/code/docs/vscode
[6]: https://github.com/GoogleCloudPlatform/cloud-code-samples
[7]: https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/new?assignees=&labels=&template=bug_report.md&title=
[8]: https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=
[9]: https://cloud.google.com/code
[10]: https://cloud.google.com/code/docs/vscode/install
[11]: https://cloud.google.com/code/docs/vscode/troubleshooting
[12]: https://github.com/GoogleCloudPlatform/cloud-code-vscode/raw/master/images/app_deploy_debug.gif
