# 3scale-on-aws
Configurations requried to deploy 3scale on AWS using operator

Please follow the instructions below to deploy 3scale for testing purpose. 

Prerequisit

1. S3 bucket with blocked public access
2. AWS Access key
3. Create registry servcie account https://access.redhat.com/documentation/en-us/red_hat_3scale_api_management/2.7/html/installing_3scale/install-threescale-on-openshift-guide#creating-registry-service-accounts
4. OCP 4.2 deployment in AWS

Steps:

1. Create new project 
2. Create registry authentication https://access.redhat.com/documentation/en-us/red_hat_3scale_api_management/2.7/html/installing_3scale/install-threescale-on-openshift-guide#configuring-registry-authentication-in-openshift
3. Create *aws-secret* using the file aws-s3-secret.yml. Please make sure you update {Bracketed_Fields} with your own.

    oc create -f  aws-s3-secret.yml

4. Install the *APIManager* by clicking **Create APIManager** button with the configuration in the *Operator-APIManager-Config.yml*
    


