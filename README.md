# Database
SonarQube
   -> amazon-linux-extras install epel
   -> amazon-linux-extras install java-openjdk11
   -> yum install mysql -y
   -> https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-6.7.6.zip
   -> sudo update-alternatives --config java
   -> /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.amzn2.0.1.x86_64/jre/bin/java
   -> edit wrapper.conf & sonar.properties


URL - https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04
install mysql in Ubuntu
Step 1 — Installing MySQL --> sudo apt update
step 2 -Then install the mysql-server package --> sudo apt install mysql-server
step 3 - Ensure that the server is running using the systemctl start command --> sudo systemctl start mysql.service
step 4 - mysql -h (DATABASE ENDPOINT) -P 3306 -u admin -p
mysql -h mysonar.cur9sziy6ysl.ap-south-1.rds.amazonaws.com -P 3306 -u admin -p

Put command and execute  in mysql - mysql command

CREATE DATABASE sonar CHARACTER SET utf8 COLLATE utf8_general_ci;

CREATE USER sonar@localhost IDENTIFIED BY 'sonar';

CREATE USER sonar@'%' IDENTIFIED BY 'sonar';

GRANT ALL ON sonar.* TO sonar@localhost;

GRANT ALL ON sonar.* TO sonar@'%';



