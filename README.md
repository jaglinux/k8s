# k8s
## Install of k8s (on Ubuntu22 Jammy)
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmour -o /etc/apt/trusted.gpg.d/kubernetes-xenial.gpg <br>
sudo apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-xenial main" <br>
sudo apt update <br>
sudo apt install -y kubelet kubeadm kubectl <br>
sudo apt-mark hold kubelet kubeadm kubectl <br>

## Install Minikube
Minikube helps to create virtual nodes in a single machine, so that we can have k8 master and workers on same node. <br>
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 <br>
sudo install minikube-linux-amd64 /usr/local/bin/minikube <br>

