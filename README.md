# Cloud Code for Visual Studio Code

Cloud Code for VS Code brings the power and convenience of IDEs to cloud-native Kubernetes and Cloud Run application development. Cloud Code works with Google’s command-line [container tools](https://github.com/GoogleContainerTools) like [`skaffold`](https://skaffold.dev/) and [`kubectl`](https://kubernetes.io/docs/tasks/tools/install-kubectl/) under the hood, providing local, continuous feedback on your project as you build, edit, and run your applications locally or in the cloud.

![E2E workflow](https://github.com/GoogleCloudPlatform/cloud-code-vscode/raw/master/images/cloud-code-quick-deploy.gif)

# Key Features

## Supporting your development workflow

Get run-ready samples, out-of-the-box configuration snippets, support for key Google services like Google Cloud APIs and Cloud Build, one click deployment, a tailored debugging experience, and much more with Cloud Code — making developing with Kubernetes and Cloud Run a whole lot easier!

<details>
  <summary>Read more</summary>

  ### Highlights:
  - Pick your preferred language with Cloud Code’s support for Go, Java, Node.js, Python, .NET Core app development.
  - Get straight to developing with Cloud Code’s simplified authentication workflow that uses your Google Cloud credentials.
  - Monitor your app with streaming logs and customize the output with additional filters to produce results meaningful to you.
</details>

## Kubernetes development

Create and run a new app in minutes with Cloud Code’s Kubernetes support. Or work on an existing application, customize its YAML with Cloud Code’s intelligent authoring support, debug it relentlessly with the setup-free debugger, and run it on any of your Kubernetes clusters. Whatever your workflow is, Cloud Code helps you spend less time on configuration and context-switching, so you can focus on developing your app.

<details>
  <summary>Read more</summary>

  ### Highlights:
  - Get started with built-in ready-to-run starter Kubernetes apps for your favorite languages and frameworks. [Read the docs](https://cloud.google.com/code/docs/vscode/creating-an-application)
  - Maintain an efficient development workflow with Cloud Code’s rapid edit, package, and deploy to cluster loop; see your edits reflected in your app in real-time! [Read the docs](https://cloud.google.com/code/docs/vscode/running-an-application)
  - Browse and manage your  Kubernetes resources from within your IDE with the Kubernetes Explorer. Just right-click and select an available action for your resource, no complex CLI commands necessary. [Read the docs](https://cloud.google.com/code/docs/vscode/using-the-kubernetes-explorer)
  - Create a remote Kubernetes cluster with Google Kubernetes Engine, EKS, or AKS, or work with a local cluster, either the integrated minikube cluster or a Docker Desktop local cluster, to run your app. [Read the docs](https://cloud.google.com/code/docs/vscode/adding-a-cluster)
  - Set breakpoints, inspect variables, and perform other debugging tasks with integrated debugging support and without having to manually set up configuration. [Read the docs](https://cloud.google.com/code/docs/vscode/debug)
  - Make easy work of setting up and customizing Kubernetes configuration files with Cloud Code’s YAML authoring assistance with out-of-the-box solutions for common schema, support for Custom Resources (CRDs) like Istio and Knative, smart completions, syntax coloring, documentation on hover, and linting support. [Read the docs](https://cloud.google.com/code/docs/vscode/yaml-editing)
</details>

## Cloud Run development

Create and deploy a new service in minutes with Cloud Code’s equally robust Cloud Run support, monitoring your service’s progress with the Cloud Run Explorer and service logs accessible in the Log Viewer. If you’d prefer a local development workflow, you can also develop and debug a service locally with the built-in Cloud Run emulator .

<details>
  <summary>Read more</summary>

  ### Highlights:
  - Deploy a service to Cloud Run, customizing your deployment platform and build settings along the way, from within your IDE. [Read the docs](https://cloud.google.com/code/docs/vscode/deploying-a-cloud-run-app)
  - Locally debug your service via the Cloud Run emulator and perform tasks you normally do when debugging local code as you develop your app. With Cloud Code’s fast iterative development, you can automatically redeploy changes to the emulator as you make them. [Read the docs](https://cloud.google.com/code/docs/vscode/debugging-a-cloud-run-app)
  - Monitor the status of your Cloud Run services as well as their revisions and essential properties with the Cloud Run Explorer. [Read the docs](https://cloud.google.com/code/docs/vscode/cloud-run-explorer)
</details>

## Containerization made easy
Create secure, production-ready container images from source code without having to worry about a Dockerfile with Cloud Code’s built-in support for Google Cloud Buildpacks. You get to focus on building your application, not containerizing it. 

## Built-in Secret Manager support
Protect sensitive information and keep your app secure with Cloud Code’s integrated Secret Manager support. You can create, view, update, and use secrets in the Secret Manager view without having them in your codebase. [Read the docs](https://cloud.google.com/code/docs/vscode/secret-manager)

## Google Cloud APIs at your fingertip
Browse available Cloud APIs, enable services, and install and learn how to integrate client libraries in your app without leaving your IDE and breaking your development flow, all with the API library browser. [Read the docs](https://cloud.google.com/code/docs/vscode/client-libraries)

# Resources

- [Learn more](https://cloud.google.com/code): Learn more about Cloud Code and what it has to offer.
- [Documentation](https://cloud.google.com/code/docs/vscode): We have a lot of features to explore. Head over to our documentation to discover more.
- [Talk to us](https://join.slack.com/t/googlecloud-community/shared_invite/zt-erdf4ity-8ZMUQ18DYV~5hkbZ~gCswg): Connect to the Cloud Code development team by joining our #cloud-code Slack channel
- [File an issue](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/new?assignees=&labels=&template=bug_report.md&title=): If you discover an issue, file a bug and we’ll fix it as soon as possible.
- [Request a feature](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=): If you have any feature requests, ideas for improvement, and general feedback, submit a feature request.
