### Sonarqube install by docker on aws server--

#### Install docker using shell script
https://github.com/mydev911/installation_scripts/blob/0e7439d51a618adc1e84e5a63d699d1d314adaa2/Docker_install_shell_script.md


##### Create A container
```
docker run -d --name sanarqube -p 9000:9000 -p 9092:9292 sonarqube
```
Check sonarqube 
ip:9000

#### install Nexus

#### Install kubeadm
https://github.com/mydev911/Kubernetes/blob/8cc6f58e5f78a9dd70b16b502bc897d051cfbac7/Install_kubernets/Kubeadm.md
