# maven
sudo yum install java-11-amazon-corretto-headless
cd opt
install maven 
wget https://archive.apache.org/dist/maven/maven-3/3.8.5/binaries/apache-maven-3.8.5-bin.tar.gz
untar maven 
tar -xvf apache-maven-3.8.5-bin.tar.gz 
export PATH=$PATH:/opt/apache-maven-3.8.5/bin
mvn -version
yum install git -y
git clone https://github.com/jdoluwasanmi/springboot-hello.git
cd springboot-hello/
mvn validate
validate your build  - cd target/
now build your .jar package file 
mvn package
then go to cd target to see your new build

you can always modify vim pom.xml to upgrade your script and package version

after that you run mvn package again

run your new code with this command

java -jar gs-spring-boot-0.3.0.jar

then go to 
http://52.90.95.39:8080/ 
to validate
