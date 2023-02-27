### Prerequisites

1. Install Kind:
    
    ```
    brew install kind
    ```
    
2. Setup a local k8s cluster
    
    ```
    sudo kind create cluster
    ```
    
3. Install tekton operators
    
    ```
    kubectl apply -f https://storage.googleapis.com/tekton-releases/operator/latest/release.yaml
    ```

   and optionally, the `tkn` cli tool:

    ```
    brew install tektoncd-cli
    ```
    
4. You may want to create a dedicated namespace
    
    ```
    kubectl create namespace ci-tekton-playground
    ```
