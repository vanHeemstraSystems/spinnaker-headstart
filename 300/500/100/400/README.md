# 400 - Installation

1. Login (SSH) to your VM or bare metal box.
2. Download the minnaker tarball and untar:

    ```bash
    curl -L https://github.com/armory/minnaker/archive/v0.1.3.tar.gz | tar -zxv
    ```

3. Change into the directory:

    ```bash
    cd minnaker-0.1.*
    ```

4. Execute the install script. Note the following options before running the script:
     * Add the `-o` flag if you want to install open source Spinnaker.
     * By default, the script installs Armory Spinnaker and uses your public IP address (determined by `curl`ing `ifconfig.co`) as the endpoint for Spinnaker.
     * For bare metal or a local VM, specify the IP address for your server with `-P` flag. `-P` is the 'Public Endpoint' and must be an address or DNS name you will use to access Spinnaker (an IP address reachable by your end users).

    ```bash
    ./scripts/install.sh
    ```
    
    For example, the following command installs OSS Spinnaker on a VM with the IP address of `192.168.10.1`:

    ```bash
    export PRIVATE_IP=192.168.10.1
    ./scripts/install.sh -o -P $PRIVATE_IP
    ```

    Installation can take between 5-10 minutes to complete depending on VM size.

5. Once Minnaker is up and running, you can make changes to its configuration using `kustomize` and the `spinnaker-operator` under the folder `~/minnaker-1.0.1/spinsvc`.  For example, to change the version of Spinnaker that is installed, you can do this:

  * Using your favorite editor, edit the file: `~/minnaker-1.0.1/spinsvc/core_config/patch-version.yml`
  * Update line 8 to the version you desire. e.g. `version: 2.24.0`
  * Then either run `cd ~/minnaker-1.0.1/spinsvc && ./deploy.sh` or `kubectl apply -k ~/minnaker-1.0.1/spinsvc`
  * To find the latest versions available:
      * [Spinnaker](https://spinnaker.io/community/releases/versions/#latest-stable)
      * [Armory](https://docs.armory.io/docs/release-notes/rn-armory-spinnaker/)
  * *By default, Minnaker will install the latest GA version of Spinnaker or Armory available.*
