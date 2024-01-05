# Local deployment of KubeFlow Pipelines
Resource for local deployment of kubeflow piplelines on WSL using k3s as the base
---------------------------------------------------------------------------
The repository was written following a combination of the "Install the k3s binary" (which `k3s_install` automates) and "Start the Kubernetes control plane" sections of [this guide](https://www.guide2wsl.com/k3s/) to install `k3s` 
and the "Deploying Kubeflow Pipelines" section of the official [KF Local Deployment](https://www.kubeflow.org/docs/components/pipelines/v1/installation/localcluster-deployment/) guide. This combination allows you to have a local
`k3s` install without recompiling the WSL kernel.

The script `kube_server` runs the kubeflow server (just automates alias resolving). Then, so you can access the server from the main device (ie outside of WSL),
foward the port by running `kubectl port-forward -n kubeflow svc/ml-pipeline-ui 8080:80` in a seperate terminal (for whatever reason, this cannot be run from a script).
