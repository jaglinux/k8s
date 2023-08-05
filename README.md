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

## Deploy deployments / pods and service
kubectl apply -f hello-deployment.yaml <br>
kubectl get deployments <br>
kubectl get pods <br>
kubectl describe  pods <br>
kubectl apply -f hello-svc.yaml <br>
kubectl get services <br>
minikube service list <br>
curl http://<IP Address>:31000 <br> 
-----> Hello from hello-77c947d946-42492  (77c947d946-42492 is the container name) <br>
successive curl will result in load balancing of workers. <br>

 ## Credits
 Dockerfile is from https://github.com/pbitty/hello-from <br>

