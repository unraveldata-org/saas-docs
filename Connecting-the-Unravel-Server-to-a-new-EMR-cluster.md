
Follow the steps below to set up and configure your EMR clusters so that Unravel can begin monitoring jobs running on the cluster. These steps will run Unravel's bootstrap script [unravel_emr_bootstrap.py](https://unravel-saas-bootstrap.s3.amazonaws.com/unravel_emr_bootstrap_saas.py), on all nodes in the cluster. 

1. In the AWS console, select the EMR service and click Create cluster.

2. In the Create Cluster - Quick Options screen, click Go to advanced options.
[[images/EMR-advanced-options-1.png]]

3. In Step 1: Software and Steps, select any Release up to emr-5.29.0. The following image is for reference:
[[images/EMR-advanced-options-2.png]]

4. In Step 2: Hardware, enter a configuration for your EMR cluster and Click Next. The following image is for reference: 
[[images/EMR-hardware-config.png]]

5. In Step 3: General Cluster Settings, specify the following settings. 

   a. In Add bootstrap action, select Custom action.

   b. In the Add Bootstrap Action dialog, specify the following settings. See the following images for reference:

[[images/EMR-bootstrap-action.png]]

[[images/EMR-bootstrap-action-1.png]]

[[images/EMR-bootstrap-action-2.png]]

   c. For optional arguments in the above bootstrap action window, enter the following:

      --unravel-server ENTER-YOUR-UNRAVEL-INSTANCE-HOSTNAME-HERE

   d. click Add.

   e. Click Configure and add.

[[images/EMR-general-options.png]]

6. In Step 4: Security, edit the configuration for the cluster as required. For example: 

   a. Choose the EC2 key pair.

   b. Select the EC2 security groups. AWS EMR service automatically applies additional rules that are required for EMR nodes.

   c. Click Create cluster.

[[images/EMR-security.png]]

7. If everything was entered correctly, your new EMR cluster should finish the bootstrap process and be in the Waiting state.

8. Once your new EMR cluster is up and running, you can run some jobs and log into your Unravel service's web UI. 
