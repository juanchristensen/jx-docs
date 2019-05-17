---
date: 2019-05-17T20:47:32Z
title: "jx controller environment"
slug: jx_controller_environment
url: /commands/jx_controller_environment/
---
## jx controller environment

A controller which takes a webhook and updates the environment via GitOps for remote clusters

### Synopsis

A controller which takes a webhook and updates the environment via GitOps for remote clusters

```
jx controller environment [flags]
```

### Examples

```
  # run the environment controller
  jx controller environment
```

### Options

```
      --bind string                  The interface address to bind to (by default, will listen on all interfaces/addresses).
  -c, --context string               The pipeline context if there are multiple separate pipelines for a given branch
      --default-image string         Specify the docker image to use if there is no image specified for a step and there's no Pod Template (default "gcr.io/jenkinsxio/builder-maven")
      --delete-temp-dir              Deletes the temporary directory of cloned files if using the 'clone-git-url' option (default true)
      --docker-registry string       The Docker Registry host name to use which is added as a prefix to docker images
      --docker-registry-org string   The Docker registry organisation. If blank the git repository owner is used
      --duration duration            Retry duration when trying to create a PipelineRun (default 30s)
      --git-kind string              The kind of git repository. Should be one of: bitbucketcloud, bitbucketserver, gitea, github, gitlab. If not specified defaults to $GIT_KIND
      --git-server-url string        The git server URL. If not specified defaults to $GIT_SERVER_URL
  -h, --help                         help for environment
      --image string                 Specify a custom image to use for the steps which overrides the image in the PodTemplates
      --kaniko-image string          The docker image for Kaniko (default "gcr.io/kaniko-project/executor:9912ccbf8d22bbafbf971124600fbb0b13b9cbd6")
      --kaniko-secret string         The name of the kaniko secret (default "kaniko-secret")
      --kaniko-secret-key string     The key in the Kaniko Secret to mount (default "kaniko-secret")
      --kaniko-secret-mount string   The mount point of the Kaniko secret (default "/kaniko-secret/secret.json")
      --no-git-init                  Disables checking we have setup git credentials on startup
      --no-kaniko                    Disables using kaniko directly for building docker images
      --no-register-webhook          Disables checking to register the webhook on startup
      --no-release-prepare           Disables creating the release version number and tagging git and triggering the release pipeline from the new tag
  -o, --owner string                 The git repository owner. If not specified defaults to $OWNER
  -p, --pack string                  The build pack name. If none is specified its discovered from the source code
      --path string                  The path to listen on for requests to trigger a pipeline run. (default "/hook")
      --port int                     The TCP port to listen on. (default 8080)
      --project-id string            The cloud project ID. If not specified we default to the install project
      --push-ref string              The git ref passed from the WebHook which should trigger a new deploy pipeline to trigger. Defaults to only webhooks from the master branch (default "refs/heads/master")
  -r, --ref string                   The Git reference (branch,tag,sha) in the Git repository to use
      --repo string                  The git repository name. If not specified defaults to $REPO
      --require-headers              If enabled we reject webhooks which do not have the github headers: 'X-GitHub-Event' and 'X-GitHub-Delivery' (default true)
      --service-account string       The Kubernetes ServiceAccount to use to run the pipeline (default "tekton-bot")
      --source string                The name of the source repository (default "source")
  -s, --source-url string            The source URL of the environment git repository
      --target-path string           The target path appended to /workspace/${source} to clone the source code
  -u, --url string                   The URL for the build pack Git repository
  -w, --webhook-url string           The external WebHook URL of this controller to register with the git provider. If not specified defaults to $WEBHOOK_URL
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

* [jx controller](/commands/jx_controller/)	 - Runs a controller

###### Auto generated by spf13/cobra on 17-May-2019