
# Cloudformation Template

This project consist of cloudformation templates for creating infrastucture for various AWS services.

#### Documentation

[Cloudformation](https://aws.amazon.com/cloudformation/)


## Deployment

To deploy a stack in cloudformation

` Here Im using AWS CLI. You can either use CLI or go for Console`

#### Must have

- AWS IAM
- Installed AWS CLI 
- Necessary permissions to creating AWS services.
- Basic AWS CLI Understanding.


#### Ensure this before creating a Cloudformation stack

- Install AWS CLI

[Cick here and follow the Instructions...](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)


- Configure a profile in AWS cli

```
aws configure --profile coderman
```


- Choose a location and clone the yaml files from github
```
git remote add origin https://github.com/Merlyn-Coderman/AWS-Cloudformation-Template.git
git clone -b main https://github.com/Merlyn-Coderman/AWS-Cloudformation-Template.git
```
### Create the Cloudformation Stack (AWS CLI)

```
export STACK_NAME= (STACK NAME HERE...)\
export REGION=(REGION NAME HERE...) \
export TEMPLATE_FILE=(FILE NAME HERE...) \
export USER_PROFILE=(USER ROFILE HERE...)

```
- Creating the stack

aws cloudformation create-stack \
--stack-name $STACK_NAME \
--template-body file://$TEMPLATE_FILE \
--tags Key=user,Value=coderman Key=project,Value=research \
--capabilities CAPABILITY_IAM \
--profile $USER_PROFILE

- Updating the stack

aws cloudformation update-stack \
--stack-name $STACK_NAME \
--template-body file://$TEMPLATE_FILE \
--tags Key=user,Value=coderman Key=project,Value=research \
--capabilities CAPABILITY_IAM \
--profile $USER_PROFILE

- Deleting the stack

aws cloudformation delete-stack \
--stack-name $STACK_NAME \
--profile $USER_PROFILE


# Hi, I'm Coderman! 👋


## 🚀 About Me
I'm a System Administrator and a Certified Cloud Practitioner.

