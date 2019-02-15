# New Application

Cloud Code for Visual Studio Code makes it easy to create a basic 2 microservice app from a set of templates.  We include templates for:

- NodeJS
- Go
- Python
- Java
- .Net Core

these templates are a simple 2 microservice K8's application that you can rapidly test of feature set through e.g. debugging, deployment, editing support, ...


## Whats in a Template

They all really have the same structure across all languages. We will use the NodeJS one as an example...

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

## Changing the default location

We have a setting for that.

