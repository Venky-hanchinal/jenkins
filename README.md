# jenkins
**Installing Jenkins on AWS EC2 Instance**

which amazon-linux-extras
sudo amazon-linux-extras enable java-openjdk11
sudo yum clean metadata 
sudo yum install java-11-openjdk
java --version (check the version)
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo amazon-linux-extras install epel
sudo yum install jenkins
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins 
ps -ef | grep "jenkins" (check the version of jenkins)
sudo chkconfig jenkins on

**Security Group Level Permission**
enable ssh port
enable http
enable https
enable 8080 port

**Jenkins Jobs**

**Job to check the version of below softwares**
Go to job configure > Build Steps > Execute Shell > enter the below commands
git --version
mvn -v
java -version
Save > Build > In console output it will show the versions of the above software.

**Job to print Text using shell**
Go to job configure > Build Steps > Execute Shell > enter the below commands
echo " Welcome Jenkins World "
Save > Build > In console output it will show Welcome to Jenkins World.

