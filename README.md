Kubernetes Installation:


sudo apt update

sudo apt install -y docker.io
sudo systemctl enable docker
sudo systemctl start docker

sudo apt install -y apt-transport-https ca-certificates curl

curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list

sudo snap install kubectl --classic

kubectl version --client

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube

minikube version

minikube start --driver=docker --force

minikube status
