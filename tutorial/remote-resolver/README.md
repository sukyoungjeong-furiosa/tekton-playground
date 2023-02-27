### Exploring the remote resolver (TEPS-0060)

See [TEPS-0060](https://github.com/tektoncd/community/blob/main/teps/0060-remote-resource-resolution.md).

Also, see [https://github.com/tektoncd/pipeline/blob/main/docs/git-resolver.md](https://github.com/tektoncd/pipeline/blob/main/docs/git-resolver.md).

0. Requires the built-in remote resolvers, install as described in [here](https://github.com/tektoncd/pipeline/blob/main/docs/install.md#installation)

    Also, check that `enable-git-resolver` feature flag is set to `true`.

    ```
    kubectl get configmap resolvers-feature-flags -n tekton-pipelines-resolvers  -o yaml | grep enable-git-resolver
    ```

1. Register the pipeline:

    ```
    kubectl apply -f hello-goodbye-pipeline-git-resolve.yaml 
    ```

2. Run the pipeline by:

    ```
    kubectl apply -f hello-goodbye-pipeline-git-resolve-run.yaml 
    ```

    and watch it by
    ```
    kubectl logs --selector=tekton.dev/pipelineRun=hello-goodbye-run
    ```
