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

**E-mail Notifications Configuration in Jenkins**

1) Manage Jenkins > Configure System > E-mail Notification > SMTP server >
smtp.gmail.com (update it) > click on advance 

2) Selecte Use SMTP Authentication > User Name (mail ID) > Password > Selecte Use SSL > SMTP port (465) 

3) Click on Test configuration by sending test e-mails > update your mail id > click on test configuration > you will get one e-mail for confirmation.

**Need to below configuration in G-mail**

1) Disable 2 factor authenticaton
2) Allow less secure on

**Extended E-mail Notification**

1) SMTP server (smtp.gmail.com) > SMTP Port (465) > Click on Advance > select use SSL > Default content type - select HTML > Default Subject & Default content just check it no edit require. 

2) Default triggers > select which one you want - selecte always > click on apply and save.

**Jenkins Job level configuration for E-mail notification**

1) Jenkins job > configure > Post build actions > Editable email notification > Project recipient list - add mail ID > content type - HTML.

2) Click on advance settings > Triggers > untick the developer list > click on apply and save. 

3) Click on Build job once it built you will get e-mail with default subject and content of build status
