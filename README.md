# infrastructure
This repository contains all the infrastructure as code(Cloudformation templates).

## AWS CLI Commands
* Creating a stack 
```
aws cloudformation create-stack --stack-name mystack1 --template-body file://csye6225-infra.yml --parameters ParameterKey=VPCName,ParameterValue=VPC ParameterKey=VPCCIDRBlock,ParameterValue=10.0.0.0/16 ParameterKey=AMIId,ParameterValue=ami-07337d0c590d5e670 ParameterKey=EnvType,ParameterValue=dev ParameterKey=DNSDomain,ParameterValue=prod.jasonpauldj.me. --capabilities CAPABILITY_NAMED_IAM
```
* Updating a stack
```
aws cloudformation update-stack --stack-name mystack1 --template-body file://csye6225-infra.yml --parameters ParameterKey=VPCName,ParameterValue=VPC ParameterKey=VPCCIDRBlock,ParameterValue=10.0.0.0/16 ParameterKey=AMIId,ParameterValue=ami-07337d0c590d5e670 ParameterKey=EnvType,ParameterValue=dev ParameterKey=DNSDomain,ParameterValue=dev.jasonpauldj.me. --capabilities CAPABILITY_NAMED_IAM
```

* Creating a new stack with different parameters
```
aws cloudformation create-stack --stack-name mystack1 --template-body file://csye6225-infra.yml --parameters ParameterKey=VPCName,ParameterValue=VPC ParameterKey=VPCCIDRBlock,ParameterValue=10.0.0.0/16 ParameterKey=AMIId,ParameterValue=ami-01c59b06117762f43 ParameterKey=EnvType,ParameterValue=dev --capabilities CAPABILITY_NAMED_IAM
```
* Deleting a stack
```
aws cloudformation delete-stack --stack-name mystack1
```
