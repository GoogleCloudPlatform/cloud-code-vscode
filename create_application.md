# Create an Application

You have the ability to create a new project for you in your language of choice.  This is a great place to start for simple demos and for this feature tour:

* Open the command palette 
* Select `Cloud Code: New Application`
* Select the language of your choice
    * NodeJS
    * Go
    * Python
    * Java
* Accept or change the default location

![New Project](images/newApplication.gif)

We will then generate a simple two microservice kubernetes application that will allow you to test many of our features.

## About New Applications

All language templates have nearly the same structure. For example the NodeJS template contains:

```
.               
|---- .vscode   
|      └---- launch.json                debugger config to connect to the cluster and containers
|---- kubernetes-manifests
|     |---- backend.deployment.yaml     the pod specification for the backend nodes
|     |---- backend.service.yaml        
|     |---- frontend.deployment.yaml    the pod specification for the frontend nodes
|     └---- frontend.service.yaml       
|---- src
|     |---- backend
|     |     |---- Dockerfile
|     |     |---- index.js
|     |     └---- package.json
|     |---- frontend
|           |---- Dockerfile
|           |---- index.js
|           └---- package.json
└---- skaffold.yaml
```

> **Note:** This is not the only supported structure but our starting recommendation.
