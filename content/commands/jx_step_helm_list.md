---
date: 2019-05-17T20:47:32Z
title: "jx step helm list"
slug: jx_step_helm_list
url: /commands/jx_step_helm_list/
---
## jx step helm list

List the helm releases

### Synopsis

List the helm releases

```
jx step helm list [flags]
```

### Examples

```
  # list all the helm releases in the current namespace
  jx step helm list
```

### Options

```
      --clone-https git@foo/bar.git   Clone the environment Git repo over https rather than ssh which uses git@foo/bar.git (default true)
  -d, --dir string                    The directory containing the helm chart to apply (default ".")
      --git-provider string           The Git provider for the environment Git repository (default "github.com")
  -h, --help                          help for list
  -n, --namespace string              the namespace to look for the helm releases. Defaults to the current namespace
```

### Options inherited from parent commands

```
  -b, --batch-mode                Runs in batch mode without prompting for user input (default true)
      --install-dependencies      Enables automatic dependencies installation when required
      --log-level string          Sets the logging level (panic, fatal, error, warning, info, debug) (default "info")
      --no-brew                   Disables brew package manager on MacOS when installing binary dependencies
      --skip-auth-secrets-merge   Skips merging the secrets from local files with the secrets from Kubernetes cluster
      --verbose                   Enables verbose output
```

### SEE ALSO

* [jx step helm](/commands/jx_step_helm/)	 - helm [command]

###### Auto generated by spf13/cobra on 17-May-2019