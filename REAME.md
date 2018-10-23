# Install Kubernetes Cluster on Centos 7

![](REAME/Screen%20Shot%202018-10-23%20at%206.09.48%20AM.png)

# Setting-up  Ansible Server on (DigitalOcean)
```
yum install git -y
git clone https://github.com/farkhodsadykov/kubernetes_ansible.git
cd kubernetes_ansible
```

### Creating ssh-key and copy to (DigitalOcean)

Connect to Ansible Server and create ssh-key
![](REAME/Screen%20Shot%202018-10-23%20at%206.12.59%20AM.png)

Copy Ansible Server's public key
![](REAME/Screen%20Shot%202018-10-23%20at%206.13.20%20AM.png)

Create Key for authentication on (DigitalOcean)
![](REAME/Screen%20Shot%202018-10-23%20at%206.14.10%20AM.png)

Create 3 Droplets and make sure you click on your Ansible's key
![](REAME/Screen%20Shot%202018-10-23%20at%206.16.16%20AM.png)


Are you running the code on Ansible server?
(y/n): y
Great, should I proceed with installation of Ansible?
(y/n): y

Do you want to install Kubernetes Cluster?

(y/n): y
Starting installation process...
Input master node IP: `masterip`
Input SSH username (Enter for root): `root`
Testing connection...
Success

Input node1 IP (Enter for none): `Node1IP`
Input SSH username (Enter for root): root
Testing connection...
Success

Input node2 IP (Enter for none): `Node2IP`
Input SSH username (Enter for root): root
Testing connection...
Success

Input node3 IP (Enter for none):
Skipping...

![](REAME/Screen%20Shot%202018-10-23%20at%206.19.34%20AM.png)

![](REAME/Screen%20Shot%202018-10-23%20at%206.27.18%20AM.png)


# Check Master side 
Login to Master server and run 
```
kubectl get pods --all-namespaces
```
![](REAME/Screen%20Shot%202018-10-23%20at%206.44.46%20AM.png)

If you see this result congrats you set up everything to start learning Kubernetes :)
