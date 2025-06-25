
## Prequisites

##### kubectl – A command line tool for working with Kubernetes clusters. For more information, see Installing or updating kubectl.

```sh
curl -LO "https://dl.k8s.io/release/$(curl -sL https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
kubectl version --client
```

##### eksctl – A command line tool for working with EKS clusters that automates many individual tasks. For more information, see Installing or updating.

```sh
curl -LO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_Linux_amd64.tar.gz"
tar -xzf eksctl_Linux_amd64.tar.gz
sudo mv eksctl /usr/local/bin/
eksctl version
```
##### AWS CLI – A command line tool for working with AWS services, including Amazon EKS. For more information, see Installing, updating, and uninstalling the AWS CLI in the AWS Command Line Interface User Guide. After installing the AWS CLI, we recommend that you also configure it. For more information, see Quick configuration with aws configure in the AWS Command Line Interface User Guide.

```sh
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
sudo apt install unzip -y
unzip awscliv2.zip
sudo ./aws/install
aws --version
```

### Use IAM Access Key to configure AWS
```sh
aws configure
```

## EKS Setup

###### Install a EKS cluster with EKSCTL

```sh
eksctl create cluster --name your-cluster-name --region ap-southeast-1 
```
###### Delete the cluster

```sh
eksctl delete cluster --name your-cluster-name --region ap-southeast-1 
```
