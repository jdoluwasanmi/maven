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

to change your web message , go to /src/java/main/hello/Hello

then go to 
http://52.90.95.39:8080/ 
to validate







Integrate Maven with SonarQube

get the plugin from sonarqube site
https://docs.sonarqube.org/9.6/analyzing-source-code/scanners/sonarscanner-for-maven/

copy the plugin form how to fix maven plugin and also go to this link to get the latest plugin version
https://mvnrepository.com/artifact/org.sonarsource.scanner.maven/sonar-maven-plugin

after which you go into the pom.xml file and add the plugin.

      <plugin>
        <groupId>org.sonarsource.scanner.maven</groupId>
        <artifactId>sonar-maven-plugin</artifactId>
        <version>3.9.1.2184</version>
      </plugin>

then go to sonarqube and generate a token to run the below command
mvn sonar:sonar -Dsonar.host.url=http://192.168.0.59:9000/sonarqube -Dsonar.login=8a66f6086d5bd367a639c31fcf0d19cd16fb286a
