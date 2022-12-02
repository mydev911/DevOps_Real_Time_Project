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
https://github.com/mydev911/installation_scripts/blob/47169e643c7e987ddccb1a922d55e10a2c43339a/Nexus%20install.md

#### Install kubeadm
https://github.com/mydev911/Kubernetes/blob/8cc6f58e5f78a9dd70b16b502bc897d051cfbac7/Install_kubernets/Kubeadm.md


## Start Jenkins.. Connecting to SonarQube
Install sonarqube plugin
1. SonarQube, 2.Sonar Quality Gates, 3.Quality Gates
##### 1. Manage Jenkins > Configure System > SonarQube > Click=Enviroment_varable > SonarQube_Installation > Name=Sonar-Server > Server_URL=SonarQubeServerIP:9000
##### 2. Server_Authentication_token > ADD > Secret.txt > Secret > Go_SonarQube > Administration > Security > User > Click=Token > Name=SonarQube > Generate > Paste_to_jenkins  > ID=sonar-token > Description=sonar-token
##### 3. ON SonarQube_Server > Configuration > Webhook > Create > Name=Jenkins-Webhook > URL=jenkins_IP:8080/sonarqube-webhook/ > Click=Create

### We are running sonarqube on docker  So we need to configure docker Plugin on jenkins  1.Docker_pipeline 2.Docker_Slaves

### Install docker on jenkin server

If jenkin get access deney to docker Fellow the link
##### https://github.com/mydev911/TroubleShoot/blob/e98688c852680081eb0c11a36f1deb258f655364/Jenkin%20access%20deney%20to%20docker.md

#### Jenkins Pipeline
State = quality gate staus
####### pipeline syntax "waitforqualitygate:wait for sonarqube analysis to be "





