# 600 - Changing Your Spinnaker Configuration

1. SSH into the machine where you have installed Spinnaker
2. Modify the contents of `~/spinnaker/spinsvc/kustomization.yml` and the associated patch files. 

** PRO TIP: Use [VS Code - Remote SSH extension](https://code.visualstudio.com/docs/remote/ssh) to interact with your minnaker instance, and manage and edit multiple files **

    See [Armory's Spinnaker Operator] (https://docs.armory.io/docs/installation/operator/).
    
    By default, the install script clones [Armory's Spinnaker Kustomize Patches repo (branch: minnaker)](https://github.com/armory/spinnaker-kustomize-patches/tree/minnaker). This branch has been pre-configured with many features to make learning Spinnaker easy. 

    [Armory Operator Reference](https://docs.armory.io/docs/installation/operator-reference/)

4. When finished save your changes, and run `deploy.sh` located under `~/spinnaker/spinsvc`.


