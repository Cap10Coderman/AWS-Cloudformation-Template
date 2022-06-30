
### Create the Cloudformation Stack (AWS CLI)

```
export STACK_NAME= (STACK NAME HERE...)\
export REGION=(REGION NAME HERE...) \
export TEMPLATE_FILE=(FILE NAME HERE...) \
export USER_PROFILE=(USER ROFILE HERE...)

```
- Creating the stack

```
aws cloudformation create-stack \
--stack-name $STACK_NAME \
--template-body file://$TEMPLATE_FILE \
--tags Key=user,Value=coderman Key=project,Value=research \
--capabilities CAPABILITY_IAM \
--profile $USER_PROFILE
```
- Updating the stack

```
aws cloudformation update-stack \
--stack-name $STACK_NAME \
--template-body file://$TEMPLATE_FILE \
--tags Key=user,Value=coderman Key=project,Value=research \
--capabilities CAPABILITY_IAM \
--profile $USER_PROFILE
```

- Deleting the stack

```
aws cloudformation delete-stack \
--stack-name $STACK_NAME \
--profile $USER_PROFILE
```

# Hi, I'm Coderman! 👋


## 🚀 About Me
I'm a System Administrator and a Certified Cloud Practitioner.
