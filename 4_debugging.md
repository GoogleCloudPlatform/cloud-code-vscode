# Debugging Kubernetes Containers

The Cloud Code for Visual Studio Code Extension supports Kubernetes container debugging for the following languages:
* `Python`
* `Node`
* `Java`
* `Go`
* `.NET Core`

For each of these languages, [launch and attach configuration snippets](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) are provided for a one-click deploying and debugging experience. See configuration attributes [section](#configuration-attributes) for the available attributes that you can used in the snippet.

## General Launching and Debugging Flow

* This outlines the general launching and debugging flow without going into specific requirements for each language.

* Open the application in VSCode.

* Open `launch.json` (more instructions on this [here](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations)) and use autocomplete to add the corresponding language debug configuration. For example, for Node.js, this would be `Cloud Code Debug: Launch (Node.js)` or `Cloud Code Debug: Attach (Node.js)`.

* Edit attributes like `podSelector` and `debugPort` to your likings (see [configuration attributes](#configuration-attributes)).

* Select and launch the configuration with F5.

* The extension may ask for permission to perform additional setup on your machine if needed. More details on this in each language sections below.

* For launch (but not attach) configuration, the workspace needs to have `skaffold.yaml` (see [skaffold](https://github.com/GoogleContainerTools/skaffold)). The extension will use skaffold to deploy the application to the Kubernetes cluster in the current context.

> Tip: Use `podSelector` attribute to choose the pod that you want to debug. A typical `podSelector` is normally:
```
"podSelector": {
  "app": <deployment-name>
}
```

* The extension will also perform port-forwarding from `localhost:${debugPort}` to `debugPort` on the container while debugging Node.js, Java, Python, and Go.

* The debug session should now be started!

## Specific language requirements:

### Node.js

* The Node.js application has to be started with `--inspect=<debugPort>` where `debugPort` comes from the debug configuration. For example:
```
CMD ["node", "--inspect=9229", "index.js"]
```

### Java

* The Java application has to be started with `-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=<debugPort>,quiet=y` where `debugPort` comes from the debug configuration. For example:
```
ENTRYPOINT ["java","-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=<debugPort>,quiet=y", "-jar", "my-app-1.0.jar"]
```
This will start the Java application in debug mode and listen on port `debugPort` for connection.

* You will also need JVM installed on your host machine.

## Python

* Python debugging requires `ptvsd` [module](https://github.com/Microsoft/ptvsd) installed on your machine. The extension will ask for permission to install this module if it cannot be found when the configuration is launched.

* The Python container also needs to have `ptvsd` module installed and the Python application needs to be started through `ptvsd` (more instructions [here](https://github.com/Microsoft/ptvsd#ptvsd-cli-usage)). The port specified in the starting command should be the same as the port in `debugPort` attribute of the debug configuration. For example:
```
CMD ["python", "-m", "ptvsd", "--port", "<debugPort>", "app.py"]
```

## Go

* Go debugging requires `dlv` [package](https://github.com/derekparker/delve) installed on your machine. The extension will ask for permission to install this package if it cannot be found when the configuration is launched.

* The Go container needs to have `dlv` package installed and the Go application needs to be started through `dlv debug` (more instructions [here](https://github.com/derekparker/delve/blob/master/Documentation/usage/dlv_debug.md)). The port specified in the starting command should be the same as the port in `debugPort` attribute of the debug configuration. For example:
```
CMD ["dlv", "debug", "--headless", "--listen=:<debugPort>", "--log"]
```

### .NET Core

* .NET Core debugging requires `vsdbg` to be installed on the Kubernetes container. The auto-generated `Dockerfile` contains a commented out block that installs `vsdbg`, the .NET Core command line debugger from Microsoft:
```
RUN apt-get update \
    && apt-get install -y --no-install-recommends unzip \
    && apt-get install -y procps \
    && rm -rf /var/lib/apt/lists/* \
    && curl -sSL https://aka.ms/getvsdbgsh | bash /dev/stdin -v latest -l /vsdbg
```

## Configuration Attributes

* `debugPort`: Debug Port used on the container. Defaults to `9229`.

* `remoteRoot`: Absolute path to the remote directory containing the program being debugged (on the Kubernetes container). Defaults to `/app`.

* `podSelector`: A set of key value pairs used to select the debug pod (read more about selector [here](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/)). A typical `podSelector` is normally:
```
"podSelector": {
  "app": <deployment-name>
}
```

* `localRoot`: Path to the local directory containing the program being debugged. Defaults to `${workspaceFolder}`.

* `protocol`: Node.js debug protocol used. Defaults to `auto`.
