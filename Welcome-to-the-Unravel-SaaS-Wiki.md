
## Follow the steps below to do an Unravel free trial using our SaaS capabilities: 


1. Go to the free trial web page http://3.209.255.193:8081/ and fill in your details [[images/Free-trial.png]] Hit the submit button.

2. Within a minute, you will receive a “Welcome email” at the email address you entered above.
[[images/Unravel-welcome-email.png]]

3. Within a few minutes, you will receive a “Deployment email” providing you the following details:
    - Unravel URL to log into
    - Location of the Unravel Bootstrap script for your cluster type (Amazon EMR for now) and instructions on how to use it
    - Videos and blogs about Unravel
[[images/Unravel-service-ready-email.png]]

4. Create one (or more) AWS EMR Cluster(s) with the bootstrap script from the Deployment email as described at [Connecting Unravel Server the EMR cluster](https://github.com/unravel-data/unravel-saas/wiki/Connecting-the-Unravel-Server-to-a-new-EMR-cluster)
 
5. Once your EMR cluster comes up, ssh into the Master node and run a Spark application as given below:
    
    spark-submit --class org.apache.spark.examples.SparkPi --master yarn --num-executors 1 --driver-memory 512m --executor-memory 512m --executor-cores 1 /usr/lib/spark/examples/jars/spark-examples.jar 1000

6. Go to the Unravel UI and monitor the Spark application.
[[images/Unravel-UI-1.png]]
[[images/Unravel-UI-2.png]]

7. Every 1 hour, Unravel will send you an Insight email that provides details about your clusters and activity.
[[images/Unravel-insights-email.png]]

8. Finally, once the trial expires after 8 hours, you will receive a free trial Expiry email and your free trial will be disabled.
[[images/Unravel-trial-expiry-email.png]]

Happy free trial and send us your feedback!

best!  
Team @ Unravel
