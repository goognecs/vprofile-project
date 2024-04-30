FROM openjdk:11 AS BUILD_IMAGE
LABEL "Project" = "Vprofile"
LABEL "Author" = "Necs"
RUN apt update -y && install maven -y 
RUN git clone https://github.com/devopshydclub/vprofile-project.git
RUN cd vprofile-project && checkout docker && mvn install  

FROM tomcat:9-jre11 
LABEL "Project" = "Vprofile"
LABEL "Author" = "Necs"
RUN rm -rf /usr/local/tomcat/webapps/* 
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
# FROM our BUILD_IMAGE, copy our WAR FIle from the Target folder where the Image was built into WEBAPPS in TOMCAT
EXPOSE 8080 
CMD [ "catalina.sh", "run" ]