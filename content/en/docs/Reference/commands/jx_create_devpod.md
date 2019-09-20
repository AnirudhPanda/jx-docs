---
date: 2019-09-19T21:19:55Z
title: "jx create devpod"
slug: jx_create_devpod
url: /commands/jx_create_devpod/
---
## jx create devpod

Creates a DevPod for running builds and tests inside the cluster

### Synopsis

Creates a new DevPod 

For more documentation see: https://jenkins-x.io/developing/devpods/

```
jx create devpod [flags]
```

### Examples

```
  # creates a new DevPod asking the user for the label to use
  jx create devpod
  
  # creates a new Maven DevPod
  jx create devpod -l maven
```

### Options

```
      --auto-expose               Automatically expose useful ports as services such as the debug port, as well as any ports specified using --ports (default true)
      --docker-registry string    The Docker registry to use within the DevPod. If not specified, default to the built-in registry or $DOCKER_REGISTRY
  -h, --help                      help for devpod
      --import                    Detect if there is a Git repository in the current directory and attempt to clone it into the DevPod. Ignored if used with --sync (default true)
  -u, --import-url string         Clone a Git repository into the DevPod. Cannot be used with --sync
  -l, --label string              The label of the pod template to use
      --persist                   Persist changes made to the DevPod. Cannot be used with --sync
  -p, --ports ints                Container ports exposed by the DevPod
      --pull-secrets string       A list of Kubernetes secret names that will be attached to the service account (e.g. foo, bar, baz)
  -c, --request-cpu string        The request CPU of the DevPod (default "1")
      --reuse                     Reuse an existing DevPod if a suitable one exists. The DevPod will be selected based on the label (or current working directory) (default true)
      --service-account string    The ServiceAccount name used for the DevPod
      --shell string              The name of the shell to invoke in the DevPod. If nothing is specified it will use 'bash'
  -s, --suffix string             The suffix to append the pod name
      --sync                      Also synchronise the local file system into the DevPod
      --temp-dir                  If enabled and --import-url is supplied then create a temporary directory to clone the source to detect what kind of DevPod to create
      --theia                     If enabled use Eclipse Theia as the web based IDE
      --tiller-namespace string   The optional tiller namespace to use within the DevPod.
      --username string           The username to create the DevPod. If not specified defaults to the current operating system user or $USER'
  -w, --working-dir string        The working directory of the DevPod
```

### Options inherited from parent commands

```
  -b, --batch-mode   Runs in batch mode without prompting for user input (default true)
      --verbose      Enables verbose output
```

### SEE ALSO

* [jx create](/commands/jx_create/)	 - Create a new resource

###### Auto generated by spf13/cobra on 19-Sep-2019