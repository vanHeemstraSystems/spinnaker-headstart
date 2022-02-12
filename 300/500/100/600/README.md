# 600 - Changing Your Spinnaker Configuration

1. SSH into the machine where you have installed Spinnaker
2. Modify the contents of `~/spinnaker/spinsvc/kustomization.yml` and the associated patch files. 

** PRO TIP: Use [VS Code - Remote SSH extension](https://code.visualstudio.com/docs/remote/ssh) to interact with your minnaker instance, and manage and edit multiple files **

    See [Armory's Spinnaker Operator] (https://docs.armory.io/docs/installation/operator/).
    
    By default, the install script clones [Armory's Spinnaker Kustomize Patches repo (branch: minnaker)](https://github.com/armory/spinnaker-kustomize-patches/tree/minnaker). This branch has been pre-configured with many features to make learning Spinnaker easy. 

    [Armory Operator Reference](https://docs.armory.io/docs/installation/operator-reference/)

4. When finished save your changes, and run `deploy.sh` located under `~/spinnaker/spinsvc`.

## Next Steps

After you finish your installation of Minnaker, go through our [AWS QuickStart](https://docs.armory.io/spinnaker/Armory-Spinnaker-Quickstart-1/) to learn how to deploy applications to AWS with Spinnaker.

Alternatively, take a look at the available Minnaker [guides](/guides/).

To learn more about the Spinnaker Operator check out the docs here: https://docs.armory.io/docs/installation/operator/

Also check out the [`spinnaker-kustomize-patches`](https://github.com/armory/spinnaker-kustomize-patches#kustomize-patches-for-armory) repo
