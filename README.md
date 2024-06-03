# Deploy-Game-Application-into-Amazon-EKS
<img src="https://github.com/AhmedYasserMabrouk/Deploy-Game-Application-into-Amazon-EKS/assets/166556717/98944fc2-c8f0-4ffb-b776-8395c9c66942">

<br>


<br>



## Create EKS Cluster
<img src="https://github.com/AhmedYasserMabrouk/Deploy-Game-Application-into-Amazon-EKS/assets/166556717/16e5b2bf-8e33-4191-8871-227f6961e49c">

### EKS Cluster Role
<img src="https://github.com/AhmedYasserMabrouk/Deploy-Game-Application-into-Amazon-EKS/assets/166556717/3d2f2024-418e-45b8-813d-4c84b5eb3ed3">

### Security Group For EKS Cluster

<img src="https://github.com/AhmedYasserMabrouk/Deploy-Game-Application-into-Amazon-EKS/assets/166556717/6acd8dcb-db16-4752-b23b-44b2c2f5d74c">

### NodeGroup Role
<img src="https://github.com/AhmedYasserMabrouk/Deploy-Game-Application-into-Amazon-EKS/assets/166556717/58439c4f-349d-47c7-a137-9b2a868fe2d2">

<hr>

<br>


## Create  EC2  server
### Install Kubectl:

```
curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.24.11/2023-03-17/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo cp ./kubectl /usr/local/bin
export PATH=/usr/local/bin:$PATH
```
### Install AWScli:
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

```

### Config


```
aws eks update-kubeconfig   --region us-east-1 --name MY-Cluster

```

### Clone github repo


```
git clone https://github.com/AhmedYasserMabrouk/Deploy-Game-Application-into-Amazon-EKS.git

```

### Run Yaml File

```
kubectl apply -f game-pod.yaml

kubectl apply -f g-service.yaml

```

### describe service


```
kubectl describe svc game-service
```


<img src="https://github.com/AhmedYasserMabrouk/Deploy-Game-Application-into-Amazon-EKS/assets/166556717/83951ee4-c9eb-4fd2-9a32-2f5989043905">





