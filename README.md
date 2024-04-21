# Database
SonarQube
   -> amazon-linux-extras install epel
   -> amazon-linux-extras install java-openjdk11
   -> yum install mysql -y
   -> https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-6.7.6.zip
   -> sudo update-alternatives --config java
   /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.amzn2.0.1.x86_64/jre/bin/java
   -> edit wrapper.conf & sonar.properties
   start sonarqube service


URL - https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04
https://medium.com/@humzaarshadkhan/sonarqube-installation-on-ubuntu-20-04-9c4f8e293870
`
install mysql in Ubuntu
Step 1 — sudo apt-get install openjdk-11-jdk -y
Step 2 - Installing MySQL --> Then install the mysql-server package --> sudo apt install mysql-server
step 3 - Ensure that the server is running using the systemctl start command --> sudo systemctl start mysql.service
step 4 - wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.6.1.59531.zip
step 5 - sudo apt-get install zip -y
step 6 - mysql -h (DATABASE ENDPOINT) -P 3306 -u admin -p
mysql -h mysonar.cur9sziy6ysl.ap-south-1.rds.amazonaws.com -P 3306 -u admin -p
-> sudo update-alternatives --config java
   /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.amzn2.0.1.x86_64/jre/bin/java
   -> edit wrapper.conf & sonar.properties
   ./soanr.sh start
root la --> chown -R ubuntu:ubuntu /opt/sonarqube-6.7.6



Put command and execute  in mysql - mysql command

CREATE DATABASE sonar CHARACTER SET utf8 COLLATE utf8_general_ci;

CREATE USER sonar@localhost IDENTIFIED BY 'sonar';

CREATE USER sonar@'%' IDENTIFIED BY 'sonar';

GRANT ALL ON sonar.* TO sonar@localhost;

GRANT ALL ON sonar.* TO sonar@'%';



