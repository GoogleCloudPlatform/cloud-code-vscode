# Deploy an Application

## Single Deployment

The `Cloud Code: Deploy` command will build your containers, push them to the registry, apply cluster configs and then return you the IP address you can use to browse.

![Deploy](images/packageAndDeploy.gif)


### Edit Inner Loop - Continuous Deployment

We can have a tight development inner loop via `Cloud Code: Continuous Deploy` command.  This command continuously watches the file system for changes to your files (K8s config or Code), rebuilds the container(s) and re-deploys to the cluster, so your edits will be reflected in near real time.

This command uses Skaffold underneath and it only builds and deploys the parts you need it to.

![Deploy](images/skaffoldDev.gif)


> **TIP:** You may want to disable AutoSave in VS Code if you use this option.