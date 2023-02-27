### Getting started with Triggers and ELs

This tutorial originates from [https://tekton.dev/docs/getting-started/triggers/](https://tekton.dev/docs/getting-started/triggers/).

1. Create the service account and associated roles, rolebindings. 
    
    ```
    kubectl apply -f rbac.yaml
    ```
    
2. Create the TriggerTemplate, and TriggerBinding:
    
    ```
    kubectl apply -f trigger-binding.yaml
    kubectl apply -f trigger-template.yaml
    ```

3. Create an event listener:
    
    ```
    kubectl apply -f event-listener.yaml
    ```

4. Enable port-forwarding and monitor the trigger 
    
    ```
    kubectl port-forward service/el-hello-listener 8080
    ```
    
    ```
    curl -v \
       -H 'content-Type: application/json' \
       -d '{"username": "Anonymous"}' \
       http://localhost:8080
    ```

5. Check the result by checking the pipelinerun

    ```
    tkn pipelinerun logs
    ```
