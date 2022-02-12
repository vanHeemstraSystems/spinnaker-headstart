# 200 - Requirements

To use Minnaker, make sure your Linux instance meets the following requirements:

* Linux distribution running in a VM or bare metal
    * Ubuntu 18.04 or Debian 10 (VM or bare metal)
    * 2 vCPUs (recommend 4)
    * 8GiB of RAM (recommend 16)
    * 30GiB of HDD (recommend 40+)
    * NAT or Bridged networking with access to the internet
    * Install `curl`, `git`, and `tar` (if they're not already installed):
        * `sudo apt-get install curl git tar`
    * Port `443` on your VM needs to be accessible from your workstation / browser. By default, Minnaker installs Spinnaker and configures it to listen on port `443`, using paths `/` and `/api/v1`(for the UI and API).
* OSX
    * Docker Desktop local Kubernetes cluster enabled
    * At least 6 GiB of memory allocated to Docker Desktop

* On Ubuntu, the Minnaker installer will install K3s for you (a minimal installation of Kubernetes), so you do not have to pre-install Docker or Kubernetes.
