# mvn-demo
demo-mvn-jenkins

# install Tomcat On Linux/Unix Box & Configure with Jenkins



# Step 1: Install Java

sudo apt-get update
sudo apt-get install default-jdk


# Step 2: Install Tomcat

sudo apt install unzip wget
cd /tmp
wget https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.11/bin/apache-tomcat-10.1.11.zip
unzip apache-tomcat-*.zip
sudo mkdir -p /opt/tomcat
sudo mv apache-tomcat-10.1.11 /opt/tomcat/


# Step 3: Change Tomcat Server Port

Jenkins is running on Port 8080, and tomcat defalut port is also 8080. So we need to change the Tomcat port, I am changing it to 9090

- sudo vi /opt/tomcat/apache-tomcat-10.1.11/conf/server.xml

Search for Connector and change the Port Value, save the file.


# Step 4: Change Permission of Scripts in /bin

cd /opt/tomcat/apache-tomcat-10.1.11/bin
ls -la
sudo chmod +x *


# Step 5: Start tomcat server and accss via browser on port 9090

/opt/tomcat/apache-tomcat-10.1.11/bin/startup.sh



# Step 6: Configure Jenkins with Tomcat for Auto Deployment of Artifacts.

Set Credentials of Tomcat that Jenkins use.

cd /opt/tomcat/apache-tomcat-8.5.47/conf

update tomcat-users.xml file.

roles : manager-script & admin-gui



Step 6 : Restart the tomcat server

/opt/tomcat/apache-tomcat-10.1.11/bin/shutdown.sh
/opt/tomcat/apache-tomcat-10.1.11/bin/startup.sh