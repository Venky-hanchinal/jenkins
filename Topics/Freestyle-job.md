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
