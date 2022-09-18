# Kubernates-kubeadm-Installation
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl
sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubelet kubeadm kubectl
sudo apt-mark hold kubelet kubeadm kubectl
#-----------------------------------------
#create a cluster using kubedeam(initialize Kubernates)
kubeadm init --apiserver-advertise-address=172.31.83.103 --pod-network-cidr=192.168.0.0/16
# if error will an occur
**kubeadm init --ignore-preflight-errors=all

