### Getting started with Pipelines

This tutorial originates from [https://tekton.dev/docs/getting-started/pipelines/](https://tekton.dev/docs/getting-started/pipelines/).

1. Apply the task on your cluster with:
    
    ```
    kubectl apply -f goodbye-world.yaml
    ```
    
2. Create a pipeline:
    
    ```
    kubectl apply -f hello-goodbye-pipeline.yaml
    ```

3. Launch the pipeline with:

    ```
    kubectl apply -f hello-goodbye-pipeline-run.yaml 
    ```
    
4.  In order to verify the result, run
    
    ```
    tkn pipelinerun logs hello-goodbye-run
    ```
