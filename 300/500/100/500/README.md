# 500 - Accessing Spinnaker

1.  A helper script called `spin_endpoint` was created during the installation process that prints out the URL associated with your spinnaker instance as well as the credentials (as necessary).

    ```bash
    spin_endpoint
    ```

    outputs: 
    ```bash
    https://192.168.64.3
    username: 'admin'
    password: 'xxxxx'
    ```
    
2. In your browser, navigate to the address (https://192.168.64.3/) for Spinnaker from step 1. This is Deck, the Spinnaker UI.

     If you installed Minnaker on a local VM, you must access it from your local machine. If you deployed Minnaker in the cloud, such as an EC2 instance, you can access Spinnaker from any machine that has access to that 'Public IP'.

3. Log in to Deck with the following credentials:

    Username: `admin`

    Password: <Password from step 1> 
