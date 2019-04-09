# Cloud Code for Visual Studio Code

Cloud Code for VS Code extends VS Code to bring all the power and convenience
of IDEs to developing cloud-native Kubernetes applications. With Google’s
command-line [container tools][1] like [`skaffold`][2] and [`kubectl`][3]
under the hood, Cloud Code gives you local, continuous feedback on your project
as you build it, extending this local edit-compile-debug loop to create
cloud-native Kubernetes environments, on your workstation or in the cloud.
Support for [deployment profiles][4] lets you define different environments,
like local development, shared development, test, or production, so you can
easily test and debug on your workstation or in the cloud.

## New App, Deploy and Debug
Create a new application, deploy it to a remote Kubernetes cluster
and live debug in seconds!

![New App, Deploy and Debug][12]

## Key Features
- Support for Go, Node, Java, and Python
- Rapid Edit, Package, Deploy loop to your K8s cluster
- Integrated Debugging and Log Viewing/Streaming
- Snippets, completions, and linting for K8s artifacts
- Profile support for dev, test and production environments
- Cluster management, resource browsing and inspection of K8s clusters
- Cluster creation supporting Google GKE, Amazon EKS and Azure AKS 
- Support for Custom Resources (CRDs) e.g. Istio, KNative

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
[11]: FAQ.md
[12]: https://github.com/GoogleCloudPlatform/cloud-code-vscode/raw/master/images/app_deploy_debug.gif
