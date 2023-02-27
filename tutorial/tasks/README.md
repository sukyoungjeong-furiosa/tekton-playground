### Getting started with Tasks

This tutorial originates from [https://tekton.dev/docs/getting-started/tasks/](https://tekton.dev/docs/getting-started/tasks/).

1. Apply the task on your cluster with:
    
    ```
    kubectl apply -f hello-world.yaml
    ```
    
2. Launch the Task as:
    
    ```
    kubectl apply -f hello-world-run.yaml
    ```
    
3.  In order to verify the result, run
    
    ```
    kubectl get taskrun hello-task-run
    ```
    
    or run
    
    ```
    kubectl logs --selector=tekton.dev/taskRun=hello-task-run
    ```
