+ <b>Author: Moole Muralidhara Reddy</b></br>
+ <b>Email:</b> telugudevopsguru@gmail.com</br>
+ <b>Website:</b> https://www.telugudevopsguru.com/</br>
+ <b>Mobile:</b>+91 7893121036</br>
+ <b>Description:</b>Setting up AWS EKS</br>
# Setting up AWS EKS
Step 1:Create the IAM user and provide the Admin Access.
Username: murali
Step 1.1: Login to the AWS Console using moole user
```xml
UserName = murali
```
Step 2: Create the VPC and 2 public subnets

```xml
Note : We are going to use default VPC so we don't required to create the VPC.
```
Step 3: Create the KeyPair

```xml
KeyPair Name : dev
```
Step 3: Create the AWS EKS Cluster Role

```xml
Name: dev-cluster-role
```

Step 4: Create the AWS EKS Cluster

 ```xml
 Cluster Name: dev-cluster
```
Step 5: Create the AWS EKS worker node Role

```xml
Name: dev-cluster-worker-node-role
```
 Attach the below policies for worker node Role

 ```xml
 AmazonEKSWorkerNodePolicy

 AmazonEC2ContainerRegistryReadOnly

 AmazonEKS_CNI_Policy
```
 Step 6: Create the Node Group

 ```xml
 Worker group name : dev-cluster-worker-node
```
 Step 7: Configure to the AWS CLI using Access key ID & Secret access key

 ```xml
 aws configure --profile dev
```
 Step 8: Connect to the EKS cluster using below command

 ```xml
 aws eks update-kubeconfig --name dev-cluster --region us-east-1 --profile dev
```

 #### Congratulations: You have successfully created the AWS EKS Cluster.
