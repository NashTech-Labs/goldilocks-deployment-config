# goldilocks-deployment-config

### Goldilocks is used to provides a dashboard that gives recommendations on how to set your resource requests.

## Prerequiste for goldilocks

* an AWS account with the IAM permissions listed on the EKS module documentation,
* a configured AWS CLI
* AWS IAM Authenticator
* kubectl
* VPA
* Metrics server

1. ### Install AWSCLI

 To install AWSCLI run the following command:

```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

unzip awscliv2.zip

sudo ./aws/install
```

2. **Check AWSCLI Version**

```
aws --version
```

### Configure AWS 

To configure awscli

```
aws configure
```

```
provider "aws"{
region = "us-east-1"
access_key = "Your_Access_Key"
secret_key = "Your_Secret_Key"
}
```

3. ### Creating Cluster

4. ### Configure Kubectl

```
aws eks  update-kubeconfig --region $(region) --name $(cluster_name)
```
5. ### INTALL Goldilocks

6. ### Install VPA

7. ### Install Mterics server

8. Create Namespace

```
Kubectl create ns demo
```

9. ### ENable the namespace

```
kubectl label ns demo goldilocks.fairwinds.com/enabled=true
```

10. yaml

```
kubectl apply -n goldilocks.yml -n demo
```

11. Dashboard

```
http://127.0.0.1:8080/dashboard
```


