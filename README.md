# Minikube-installation

sudo apt update
sudo apt install -y docker.io curl vim

##install minukube 

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

sudo install minikube-linux-amd64 /usr/local/bin/minikube

curl -L https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 -o minikube

chmod +x minikube

sudo mv minikube /usr/local/bin/minikube

minikube start --driver=docker

#if kubectl not found 

curl -LO "https://dl.k8s.io/release/$(curl -Ls https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

chmod +x kubectl

sudo mv kubectl /usr/local/bin/

kubectl version --client

kubectl get nodes
