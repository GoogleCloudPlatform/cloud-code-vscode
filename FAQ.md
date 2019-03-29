# FAQ
A list of some commonly asked questions and issues.

## I found a bug!
Please [file an issue][1] and we still get it fixed as soon as we can! 

## I have a feature request!
We appreciate all feature requests, ideas for improvement and general feedback. 

Please [file a feature request][2] to let us know your ideas and we will look into integrating them.

## What languages are supported?
For the majority of actions the language of the application shouldn't matter. 

However, for a few actions (such as debugging) Java, NodeJS, Go and Python are supported.

## Why isn't the Go Debugger working?
The Go Debugger is currently under development and being improved.
- When debugging a Go application the application will hang (not start) and wait for a debugger to attach.  This means when debugging your application your service will not load until a debugger is attached.
- When creating a new application for Go the default is to have the debugger turned off by default due to the above.  There are instructions in the Dockerfile about how to use it.

## How do I opt out of telemetry reporting?
To help improve Cloud Code plugins, feature usage statistics are collected and sent to Google.

You can opt-out at any time by visiting `Cloud Code Settings` in VS Code and updating `Enable Telemetry`.

Your use of this plugin is subject to the [Google Privacy Policy][3].


[1]: https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/new?assignees=&labels=&template=bug_report.md&title=
[2]: https://github.com/GoogleCloudPlatform/cloud-code-vscode/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=
[3]: https://policies.google.com/privacy


