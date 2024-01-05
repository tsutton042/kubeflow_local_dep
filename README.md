# kubeflow_local_dep
Resource for local deployment of kubeflow piplelines on WSL using k3s as the base
---------------------------------------------------------------------------
The repository was written following a combination of the "Install the k3s binary" (which `k3s_install` automates) and "Start the Kubernetes control plane" sections of (this guide)[https://www.guide2wsl.com/k3s/] to install `k3s` 
and the "Deploying Kubeflow Pipelines" section of the official (KF Local Deployment)[https://www.kubeflow.org/docs/components/pipelines/v1/installation/localcluster-deployment/] guide. This combination allows you to have a local
`k3s` install without recompiling the WSL kernel.

It may be the case that restarting the KFP instance requires re-running parts of the guides. If this is the case, additional scripts will be added to this repo to automate these steps
