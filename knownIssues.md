# Known Issues

## Go Debugging Experience can be confusing
- When debugging a Go application the application will hang (not start) and wait for a debugger to attach.  This means when debugging your application your service will not load until a debugger is attached.
- When creating a new application for Go the default is to have the debugger turned off by default due to the above.  There are instructions in the Dockerfile about how to use it.\

## Diffing Kubernetes resource files
- Diffing Kubernetes resource files with multiple resources in them is not currently supported.