FROM openjdk:8 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone -b vp-docker https://github.com/devopshydclub/vprofile-project.git
RUN cd Vprofile-repo && maven install

FROM tomcat:8-jre11

RUN -rf rm /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile-repo/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh","run"]
