# Command Reference

| Command                                                              | Purpose                                              |
|----------------------------------------------------------------------|------------------------------------------------------|
| Help                                                                 | View our welcome experience                          |
| Report Kubernetes' Extension Issue on Github                         | opens a pre-populates issue on Github                |
| [New Application](#create-an-application)                            | Create a new application from a template             |
| [Deploy](#deploy-for-the-first-time)                                 | Deploy the current application to the active cluster |
| Set as Current Context                                               | Set the context for the active cluster               |
| Remove from Context                                                  | Sets the given cluster as the current active cluster |
| Set as Active Namespace                                              | Sets the given namespace as the current active namespace. |
| Refresh Cluster Context Explorer                                     | Refresh the explorer                                |
| [View Logs](#working-with-logs)                                      | Opens a terminal and write out the current logs from the container. |
| [Stream Logs](#working-with-logs)                                    | Opens a terminal and stream logs from the container. |
| Copy Resource Value                                                  | Copy the value of the given resource                 |
| Open Address                                                         |                                                      |
| Describe                                                             | Gives a detailed description of the resource.        |
| Delete                                                               | Deletes the given resource                           |
| Open Dashboard                                                       | Opens the Kubernetes dashboard                       |
| Get Terminal                                                         | Opens a terminal into the container                  |
| Create Kubernetes resource from current file                         |                                                      |
| Diff the current JSON/YAML file with Kubernetes deployed resource    |                                                      |
| Apply the current JSON/YAML file to the Kubernetes deployed resource |                                                      |
| Open Minikube dashboard for starting/stopping local Minikube cluster |                                                      |
| Open Minikube dashboard                                              |                                                      |
| Mount Secret as Volume                                               | Mounts the secret as a deployment in a base-64 decoded file. |
| Add Secret as Environment Variable                                   | Adds an environment variable to the deployment with the value of the secret (base-64 decoded). |
