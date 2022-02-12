# 100 - Background

Based on "Spinnaker All-In-One (Minnaker) Quick Start - Background" at https://github.com/armory/minnaker

Minnaker performs the following actions when run on a single Linux instance:

* Installs [k3s](https://k3s.io/) with Traefik.
* Installs minio in k3s with a local volume.
* Installs mysql in k3s.
* Installs redis in k3s.
* Installs **[Spinnaker Operator](https://github.com/armory/spinnaker-operator)**.
* Clones the "minnaker" branch in https://github.com/armory/spinnaker-kustomize-patches for the purposes of configuring Spinnaker.
* Installs and configures **[Spinnaker](https://github.com/spinnaker)** or **[Armory](https://armory.io)** using the **Spinnaker Operator**.
* Exposes Spinnaker using an Ingress.  NOTE: If you're using an AWS EC2 instance, make sure you add port 443 to the security group.
* Minnaker uses local authentication. The username is `admin` and the password is randomly generated when you install Minnaker. Find more details about getting the password in [Accessing Spinnaker](#accessing-spinnaker).
* For the full list of customizations and configurations - please check out the [kustomization-minnaker.yml] (https://github.com/armory/spinnaker-kustomize-patches/blob/minnaker/recipes/kustomization-minnaker.yml) file.
