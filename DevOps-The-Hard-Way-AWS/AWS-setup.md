# Setup AWS account

+ [Create user and it's keys (optional)](#create-user-and-it-s-keys--optional-)
+ [Setup a resource group based on tags](#setup-a-resource-group-based-on-tags)
+ [Install AWS cli and configure](#install-aws-cli-and-configure)

### Create user and it's keys (optional)
### Setup a resource group based on tags
- Open *resource group and tag editor* service
- Create a resource group `useast1_DevOpsTheHardWayAWS` with tags `useast1_DevOpsTheHardWayAWS:use` and `use:useast1_DevOpsTheHardWayAWS` 

### Install AWS cli and configure
Follow [this](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) url to install aws cli
```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```
Follow [this](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html#cli-configure-quickstart-region) to configure aws cli
```bash
ubuntu@desktop:~/Desktop/aws$ aws configure
AWS Access Key ID [None]: *********
AWS Secret Access Key [None]: ************************
Default region name [None]: us-east-1
Default output format [None]: yaml

ubuntu@desktop:~/Desktop/aws$ cat ~/.aws/config 
[default]
region = us-east-1
output = yaml

ubuntu@desktop:~/Desktop/aws$ cat ~/.aws/credentials 
[default]
aws_access_key_id = *********
aws_secret_access_key = *******************
```
