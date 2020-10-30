# Cloud Code for Visual Studio Code

Cloud Code for VS Code brings the power and convenience of Google Cloud to Visual Studio Code. Our extension works
with Google’s command-line [container tools][1] like [`skaffold`][2] and [`kubectl`][3] under the hood, providing
local, continuous feedback on your project as you build, edit, and run your applications on your workstation or in
the cloud. You can easily find and manage Google Cloud APIs to use. Cloud Code for VS Code even helps you connect to
Google Cloud resources while running on Kubernetes and emulated Cloud Run locally.

## App, Deploy and Debug

With Cloud Code, you can create a new Kubernetes or Cloud Run application, deploy it to a locally or remotely in
seconds with live updates as you write code. Or you can seamlessly debug Cloud Run applications locally as well as
Kubernetes applications both locally and remotely.

![New App, Deploy and Debug][12]

## Google Cloud API library browser

Cloud Code allows you to find Google Cloud APIs without leaving your IDE and breaking your development flow. Easily
add these APIs to your project and discover more with our API library browser.

![Client Library Explorer][14]

## Manage your secrets with Secrets Manager

With Cloud Code get the convenience of managing your application secrets directly in VS Code. Quickly connect to
Google Cloud when running in your IDE locally even while debugging or testing your Kubernetes and Cloud Run
applications.

![Secret Manager][15]

## Use Google Cloud buildpacks

With Cloud Code you can focus on building your application, not containerizing it by using Google Cloud buildpacks.
Easily deploy your code directly to GKE or Cloud Run without worrying about a Dockerfile.

## Key Features

- Support for Go, Node, Java, and Python
- Integrated Debugging and Log Viewing/Streaming
- Cluster and service inspection with the Kubernetes and Cloud Run explorers
- Cluster creation supporting Google GKE, Amazon EKS and Azure AKS
- Rapid Edit, Package, Deploy loop to your Kubernetes and Cloud Run projects
- Snippets, completions, and linting for K8s artifacts
- Support for Custom Resources (CRDs) e.g. Istio, Knative
- Automatically uses your Google Cloud SDK credentials even when using Kubernetes and Cloud Run locally
- Easily find and manage Google Cloud APIs using the Library Explorer
- Manage your secrets using Secret Manager
- Integrated with Google Cloud buildpacks

## Resources

- [Learn More][9]: Learn more about the Cloud Code project and what it has to offer.
- [Documentation][5]: We have a lot of features to explore head over to our documentation to find out.
- [FAQ][11]: A list of frequently asked questions you may run into.
- [Talk to us][13]: Connect to the Cloud Code development team by joining our #cloud-code Slack channel
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
[13]: https://join.slack.com/t/googlecloud-community/shared_invite/zt-erdf4ity-8ZMUQ18DYV~5hkbZ~gCswg
[14]: https://www.gstatic.com/cloudssh/cloudcode/client-library-browser.gif
[15]: https://www.gstatic.com/cloudssh/cloudcode/secret-manager-explorer.png
