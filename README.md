# AWS_ROSA
Introduction to AWS ROSA


Setting up AWS ROSA CLI on Windows 10 & running basic commands
(For info on Linux: https://github.com/openshift/rosa)

Red Hat OpenShift
Before you configure your environment create an account on Red Hat Openshift. Trial accounts available.

1. Access Red Hat OpenShit acct: 
https://cloud.redhat.com/openshift/

AWS
This portion assumes AWS CLI for user hosting cluster has been configured. 

1. Create user using IAM with programmatic and admin rights and copy the key and secret to your text editor
2. Setup and configure DNS using Route 53
3. Type rosa on the AWS web console and select Red Hat OpenShift on AWS
4. Click on enable service https://console.aws.amazon.com/rosa/home?region=us-east-1#/
5. Download the CLI https://www.openshift.com/products/amazon-openshift/download
6. Run on the cmd the rosa exe.file 
7. Confirm installation by running on the cmd: rosa verify permissions
8. If output is "AWS SCP policies ok" the installation has been successful

ROSA CLI
Below are the instructions about login in rosa CLI and other useful commands.

1. Go to https://cloud.redhat.com/openshift/token/rosa/show and get Red Hat OpenShit -> API token 
2. To log in rosa CLI run on cmd: rosa login --token="TOKEN" and press enter

To get started with your cluster visit the link below.
https://aws.amazon.com/blogs/aws/red-hat-openshift-service-on-aws-now-generally-availably/

To verify your AWS account has all the pre-requisites for launching a cluster visit the link below:
https://docs.openshift.com/rosa/rosa_getting_started/rosa-aws-prereqs.html

Useful commands 

-- To verify rosa setup: rosa verify permissions
-- To verify AWS user is correct: rosa whoami
-- To check quota (resources available on AWS: rosa verify quota
-- To verify if your account is ready for deployment: rosa init
-- To create a cluster: rosa create cluster --cluster-name=<cluster_name> 
-- To edit cluster: rosa edit cluster --cluster=mycluster --private 
-- To add an identity provider (IDP): rosa create idp --cluster=<cluster_name> --type=<identity_provider> [arguments]
-- To add an admin: rosa grant user dedicated-admin --user=<idp_user_name> --cluster=<cluster_name>
-- To list your clusters: rosa list clusters
-- To list all AWS regions available: rosa list regions
-- To get general help: rosa --help


Other Resources:
https://docs.openshift.com/container-platform/4.7/welcome/index.html
https://access.redhat.com/documentation/en-us/red_hat_openshift_service_on_aws/4/html/rosa_cli/rosa-get-started-cli
https://aws.amazon.com/rosa/


















