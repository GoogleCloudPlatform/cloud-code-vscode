# Cloud Code for Visual Studio Code Release Notes

This page documents production updates to Cloud Code for Visual Studio Code. You can check this page for announcements about new or updated features, bug fixes, known issues, and deprecated functionality.

## Version 1.8.0 (January 26, 2021)

### New Features
* **Custom templates:** You can now create applications from custom templates! Cloud Code offers the option of importing a Git template repository so that teams can get started quickly from a standard set of starter applications, services, and infrastructure configuration best suited to teams’ organizational policies. To read more about templates and how to get started, head over to [setting up a template repository](https://cloud.google.com/code/docs/vscode/set-up-template-repo) guide.

![custom templates](https://www.gstatic.com/cloudssh/cloudcode/contextual-status-bar.png)

* **Cloud Code Status Bar options:** Discover more about your currently active sessions with these additions to the Cloud Code status bar.
  * **Open Service URL:** Instead of scrolling through the logs to find the service URL, you can now open the application service URL in a web browser directly from the status bar.
  * **Open Deployment Logs:** Open the application logs with the Cloud Code Logs Viewer. This populates the necessary filters in the Logs Viewer for the selected deployment.
  * **Turn on/off Watch Mode:** Toggle watch mode (not available for debug session currently). This allows you to turn on/off watch mode for the current active run session without stopping, changing the launch.json `watch` field, and redeploying. Note that this toggle only affects the current session and not subsequent ones.

![status bar options](https://www.gstatic.com/cloudssh/cloudcode/custom-templates.png)

* **New sample application READMEs:** When you create a new sample application with Cloud Code, the new README gives updated guidance on next steps to help you get more out of Cloud Code.

![new sample application READMEs](https://www.gstatic.com/cloudssh/cloudcode/vscode-readme.png)

### Updates
* **.NET launch debugging support:** In addition to the attach configuration, Cloud Code now supports a launch configuration for .NET. You can now deploy and attach to a .NET application with a single configuration.
* **New home for Cloud Run properties:** Cloud Run properties no longer show up in a separate view. They can be found conveniently in the Cloud Run Explorer under **Properties**.

![new sample application READMEs](https://www.gstatic.com/cloudssh/cloudcode/cr-explorer-properties.png)

### Bug Fixes
* Fixed Cloud SDK auto dependency installation corruption issue on Windows. [#346](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/346)
* Fixed Python enabling to debug external sources. [#328](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/328)
* Fixed YAML outline to handle arrays of objects. [#339](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/339)
* Fixed available cluster listing when faced with restricted project permissions. [#318](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/318)
* Fixed docs for Cloud Run service config, discovering logs, stopping the emulator. [#298](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/298)
* Fixed an issue where installation of minikube is not required for deploying to Kubernetes cluster. [#280](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/280)
* Fixed an issue to display deployment progress failures on the right side status bar.
* Fixed an issue that allows users to switch accounts without running into permission requests on older accounts.

## Version 1.7.2 (January 15, 2021)

### Bug Fixes 
* Fix an issue where dependencies path gets invalidated on Windows. [#362](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/362) 
* Fix an issue where Cloud SDK in the path gets corrupted on Windows since there is reentry while installing dependencies. [#347](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/347)

## Version 1.7.1 (December 09, 2020)

### New Features 

* **Project Selection Flows:** The project selector has been refreshed to deliver an improved UX, faster load times, and recent projects listed first. The project selection/login/logout should sync between all webviews and explorers.

![project selection flows](https://www.gstatic.com/cloudssh/cloudcode/mru-project-selection.gif)

* **Refresh GKE Explorer:** The look and feel of the GKE Explorer is now consistent with the Secret Manager Explorer and the Cloud Run Explorer.
* **YAML Editing Support:** YAML editing support can now accurately be limited to a subdirectory under the working directory by setting `cloudcode.yaml.yamlFileMatcher`. [Learn more](https://cloud.google.com/code/docs/vscode/yaml-editing)

### Updates
* Replace general icons with VSCode Codicons for commands.
* Improved Cloud Run (fully managed) support:
* Allocate up to 4 vCPUs to container instances with the increased limit.

### Bug Fixes 
* Fix .NET debugging fails to open a source file when the breakpoint is hit. [#292](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/292) 
* Refresh AKS cluster UI after modifying the active subscription. [#239](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/239)

## Version 1.7.0 (October 30, 2020)

* **Secret Manager Support:** Many applications require credentials to connect to a database, API keys to invoke a service, or certificates for authentication. Cloud Code now integrates with Google Cloud's Secret Manager to make it easy to create, view, update, and use secrets from within your IDE so you can keep this sensitive data out of your codebase and keep your applications secure.  Get started today by viewing secrets, creating a new secret, or add secret manager API support to your code.   You can learn more about Secret Manager support from [the Cloud Code Secret Manager documentation](https://cloud.google.com/code/docs/vscode/secret-manager).

  * View secrets, their versions, permissions, and properties in the Secret Manager view.
    ![Secret manager explorer view](https://www.gstatic.com/cloudssh/cloudcode/secret-manager-explorer.png)

* **Minikube Credentials Support:** When running or debugging on Cloud Run Emulator or minikube, Cloud Code will automatically set up the [minikube gcp-auth](https://minikube.sigs.k8s.io/docs/handbook/addons/gcp-auth/) addon. This will enable you to use your Google developer credentials to authenticate Google API client libraries in your apps when running in these environments with zero configuration required. Cloud Code also has a new login flow to ensure you have developer credentials installed when you login.

* **Managed Dependencies in Integrated Terminal:** You can now use Cloud Code managed dependency CLIs, such as minikube and gcloud, through VSCode Integrated Terminals.
  ![Managed dependencies in integrated terminal](https://www.gstatic.com/cloudssh/cloudcode/integrated-terminal.png)

### Updates

* **Improved Cloud Run (fully managed) support:**

  * Deploy Cloud Run services from your IDE to these newly added regions. View the full supported list [here](https://cloud.google.com/run/docs/locations).

  * Allocate up to 4GiB of memory to your services with the increased quota.

### Bug Fixes

* Minikube status checks are aggressive and lead to generating more log files that can slow down other build tools. The change is to remove the live status bar but use minikube status bar to monitor status of different profiles and is less invasive. [#286](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/286) [#313](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/313) 

* Cloud run emulator didn’t bootstrap itself on windows since it chose the hyper-v that got blocked on the need for special permissions, Cloud code now defaults to using docker driver for the emulator.

* Regions are not available when I use "Deploy to Cloud Run". [#314](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/314)

## Version 1.6.0 (Septemeber 29, 2020)

### New Features

* **Improved performance:** Reduced load times for populating the GKE explorer (from  about a 12 second load time to under 5 seconds!); logging out or switching accounts is now a much faster experience.

* **Kubernetes run/debug bootstrapping improvements:** Cloud Code now helps you set an active context at the start of a run or debug session to help you get your Kubernetes application deployed quickly. If you don’t have any contexts, Cloud Code helps you create one.

  ![Kubernetes run/debug bootstrapping improvements](images/run-debug-no-contexts_1_6_0.gif "Kubernetes run/debug bootstrapping improvements")

* **Auto-start minikube:** Cloud Code now manages minikube more proactively. When running/debugging on a minikube cluster that is paused or stopped, Cloud Code automatically starts the cluster at the beginning of the session and pauses it when you’re done.

  ![Auto-start minikube](images/auto-start-minikube_1_6_0.gif "Auto-start minikube")

## Version 1.5.0 (August 18, 2020)

### New Features

* **Cloud Run local development:** Develop Cloud Run applications locally using Minikube clusters with the newly added
Run and Debug on Cloud Run Emulator commands.

  ![Cloud Run Local Development](images/cloud-run-local-dev_1_5_0.gif "Cloud Run Local Development")

* **Expanded CRD support:** Cloud Code has been expanded to support validation, hover documentation, and code
completions for hundreds of popular Kubernetes Custom Resources.

  ![Expanded CRD Support](images/popular-crd-support_1_5_0.gif "Expanded CRD Support")

* **Buildpacks support:** In addition to Docker, you can now build your images with Google Cloud buildpacks.

  ![Buildpacks Support](images/buildpacks_1_5_0.gif "Buildpacks Support")

* **Auto generate configuration experience for existing K8s apps:** The UI that helps auto generate configuration for
an existing app moving in to using Cloud Code extensions now supports specifying all available build and
configuration settings.

  ![Generate Kubernetes Configuration](images/bootstrap_kubernetes_1_5_0.gif "Generate Kubernetes Configuration")

* **Improved New Application UI:** Creating a new application now uses the system file picker to help you quickly place the new files in a familiar way. You can rename the new application folder through your system file manager.

  ![Generate App With System File Picker](images/create_k8s_app_1_5_0.gif "Generate App With System File Picker")

## Version 1.4.0 (May 29, 2020)

### New features

* **Kubernetes Context Management:** Contexts are now accessible from the Kubernetes Explorer!
You can now browse and switch between Kubernetes contexts as you would during your development workflow with Cloud Code. With the updated Kubernetes Explorer, it's easier to understand
the active context associated with your current cluster and move to another if you need.

  ![Managing Kubernetes Context](images/kubecontext_1_4_0.JPG "Managing Kubernetes Context")

* **PersistentVolumeClaim support:** The Kubernetes Explorer will now show your cluster's PersistentVolumeClaim (PVC) resources and each PVC's status and key details.

  ![PersistentVolumeClaim support](images/pvc_1_4_0.JPG "PersistentVolumeClaim support")

### Bug Fixes

* Cloud Code will now allow you to browse and switch between Kubernetes contexts. [#131](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/131) 
* You can now browse PersistentVolumeClaim in the Kubernetes Explorer. [#193](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/193)

## Version 1.3.0 (May 8, 2020)

We are pleased to announce [Cloud Run](https://cloud.google.com/run) support in Cloud Code for VS Code!

### New Features

* **Cloud Run support in VS Code:** Cloud Code now makes it easy to develop and deploy your services to Cloud Run (fully managed) or Cloud Run for Anthos on GKE directly from within Visual Studio Code.  You can get started with our starter templates for Java, Node.js, Go, or Python.
  * Browse your Cloud Run services directly from the IDE using the Cloud Run explorer. Easily see details of deployed services as well as revisions and status.
  * Follow the [Cloud Run quickstart guide](https://cloud.google.com/code/docs/vscode/quickstart-cloud-run) to get started!

  ![Cloud Run service browser and deployment flow](images/cloud-run-support_1_3_0.gif "Cloud Run service browser and deployment flow")

* **Improved dependency management:** Better experience when Cloud Cloud is managing dependencies.
  * Improved performance when installing managed dependencies.
  * Stay up to date with the latest versions of dependencies.

* **Cloud Code: Debug on Kubernetes:**  New command to debug applications with the same configuration used to [run the application](https://cloud.google.com/code/docs/vscode/running-an-application).
  * Invoking this command will launch the application and debugs all the containers in the app.
  * Refer to the [documentation](https://cloud.google.com/code/docs/vscode/debug) for more on this feature.

  ![Debug on Kubernetes command](images/debug-on-kubernetes.gif "Debug on Kubernetes command")

* **Separate views for Kubernetes, Cloud Run and APIs:** Reorganized UI to focus on the flows that matter.

  ![Separate views](images/action-bar-changes_1_3_0.gif "Separate views")

### Other Changes

* **Dependency management:** Previously offered "On," "Off," and "Ask" as choices for managing dependency with "Ask" as the default. In the latest release we've removed the "Ask" choice with "On" as the default. Anyone who has picked "Ask" will be defaulted to "On."
* **Deprecation of Kubernetes deploy commands:** The deprecated ‘Cloud Code: Deploy’ and ‘Cloud Code: Continuous Deploy’ have been removed. Use ‘Cloud Code: Run on Kubernetes’ command.

### Bug Fixes

* Add support for Google Cloud Run. [#231](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/231)
* Hanging while installing dependencies. [#227](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/227) 
* Cannot start debugger for .NetCore project. [#225](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/225) 
* GKE Explorer does not work in windows 10. [#224](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/224)
* Add Configuration to Existing Project is broken. [#223](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/223)
* Add a guidance message in case no Kubernetes manifest are present. [#203](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/203) 

## Version 1.2.1 (March 25, 2020)

Updated the extension to be compatible with the latest version of Visual Studio code. Fixed an issue introduced by the latest update that caused specific terminal commands to hang.


## Version 1.2.0 (March 02, 2020)

### New features

* **Flexible Kubernetes YAML editing:** Edit your Kubernetes YAML with additional support for multiple Kubernetes versions.
* **Streamlined remote development flow:** Work with Cloud Code [using a remote development environment](https://cloud.google.com/code/docs/vscode/quickstart-remote-dev), taking advantage of newly added support:
  * Start development with just Visual Studio Code installed.
  * Receive direct reporting on the progress of ‘Open with Cloud Code’ throughout its flow.
  * Cancel the open any time during the operation.
  * If an error does occur, know that it will come with actionable guidance.

    ![alt_text](images/cloud-shell-new-flow_1_2_0.gif "Working with Cloud Shell")

* **Cloud Code: Deploy deprecation:** ‘Cloud Code: Deploy’ and ‘Cloud Code: Continuous Deploy’ commands are [deprecated](https://cloud.google.com/code/docs/vscode/troubleshooting#how_is_the_cloud_code_run_on_kubernetes_command_different_from_cloud_code_deploy_application). While these commands continue to work, they will be removed in the next release (v1.3), targeted for the end of March.

    Use ‘Cloud Code: Run on Kubernetes’ command instead.

* **Improved Logs Viewer:** Make the most out of your log viewing with the following new filters:
  * Log Type: switch between kubectl, Cloud Logging and Cloud Run logs.
  * Cluster: switch between different clusters when viewing Cloud Logging logs. This allows you to query logs from specific clusters instead of from all of them.  For kubectl logs, this will only show the current active cluster.

    ![alt_text](images/improved-logs-viewer_1_2_0.gif "Improved logs viewer")

### Bug Fixes

* Cloud Code will no longer continually switch user context to the output window. [#176](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/176) 
* Fixed an issue where the Logs Viewer hangs when you don’t have permission to list all namespaces. [#201](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/201) 
* Fixed an issue where Open with Cloud Code would not clone a repository in some cases.
* Fixed an issue where Cloud Shell would fail to create an SSH configuration when the gcloud command-line tool prompted for survey participation.

## Version 1.1.2 (Feb 27, 2020)

### Notable Fixes

* Fixed an issue in the "Open in Cloud Code" feature
* Fixed an issue where logs in "Cloud Code Yaml Support" output channel will grab focus
* Minor bug fixes

## Version 1.1.1 (February 27, 2020)

### New Features

* Enable the deprecated `Cloud Code: Deploy` and `Cloud Code: Continuous Deploy` commands along side with the new and recommended command `Cloud Code: Run on Kubernetes`. You can now continue with your existing workflow while taking the time to make a switch!

### Bug Fixes

* Run in Kubernetes: Cant disable the watch (#198)

## Version 1.1.0 (January 30, 2020)

### New Features

* **Client Library Browser:** Manage your Google Cloud APIs with Cloud Code’s freshest new feature: the Client Library Browser. View all available Google Cloud APIs, enable an API, view API status (enabled or disabled), and install client libraries to consume an API, all from within your IDE.

    ![alt_text](images/client-library-browser_1_1_0.gif "Client library browser")

* **Cloud Code: Run on Kubernetes:**

    A new command, ‘Cloud Code: Run on Kubernetes,’ has been added that lets you run your kubernetes application and view it live. 'Cloud Code: Deploy' and 'Cloud Code: Continuous Deploy' commands have been deprecated in favor of this command. For more details on this change, please refer to this [link](https://cloud.google.com/code/docs/vscode/troubleshooting).

    ![alt_text](images/deployment-flow_1_1_0.gif "New deployment flow")

* In addition to the above features, this release also includes some bug fixes. You can view the full list [here](https://github.com/GoogleCloudPlatform/cloud-code-vscode/milestone/3).

## Version 1.0.0 (November 21, 2019)

We are pleased to announce that Cloud Code is now GA!

### New Features

* **Cloud Shell Integration** Use the ‘Open with Cloud Code’ feature to quickly get started using Google Cloud Platform. It uses a remote development environment in [Cloud Shell](https://cloud.google.com/shell/docs) which means you’ll get to skip setup and start developing with Cloud Code with the click of a button. 

    With ‘Open with Cloud Code’, you can edit, run, and debug code; as well as utilize all of Cloud Code's features directly from inside Cloud Shell. Visual Studio Code's integrated terminal allows direct interaction with command line utilities running in Cloud Shell, such as the gcloud command-line tool, skaffold, and kubectl.

    ![alt_text](images/cloudshell_1_0_0.gif "Opening in Cloud Shell")

* **YAML editing** Get started with Cloud Build with Cloud Code’s built-in snippets for Cloud Build and Cloud Build trigger YAML files.

    ![alt_text](images/cloudbuild-yaml_1_0_0.gif "Cloud Build YAML editing")

### Bug Fixes

* Added ability to view and edit yaml of Ingress resource. [#158](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/158)

## Version 0.0.13 (November 7, 2019)

### New Features

* **Logs Viewer**  Browse through and filter Kubernetes cluster logs easily using the new Logs Viewer. For clusters that do not support Stackdriver logging cluster logs will now be colorized.

    ![alt_text](images/logs_viewer_0_0_13.gif "Stackdriver logs viewer")

* **Dependency Installer** Cloud Code will manage kubectl and Skaffold CLI dependencies automatically.  This can be controlled using the `cloudcode.auto-install` setting.

    ![alt_text](images/dependency_installer_0_0_13.png "Dependency installer")

* **YAML Editing** Create and modify YAML with Cloud Code’s richer YAML editing experience for these configuration types:
  * Anthos Config Management ([link](https://cloud.google.com/anthos-config-management/docs/how-to/configs))
  * Config Connector ([link](https://cloud.google.com/config-connector/docs/overview))
  * Migrate for Anthos ([link](https://cloud.google.com/migrate/anthos/docs/yaml-reference))

    ![alt_text](images/migrate_for_anthos_0_0_13.gif "Migrate for Anthos YAML editing")

* **Colorized Streams** Deployment and Continuous Deployment output streams will be colorized to highlight key events.

    ![alt_text](images/colorized_streams_0_0_13.gif "Colorized logs view")

### Notable Fixes

* Improved extension activation time by removing dependency on language server activation. ([#140](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/140))
* Reduced the memory footprint of Kubernetes Cluster Explorer to allow handling large clusters.
* Included various stability fixes. ([#147](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/147)) ([#101](https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/101))
