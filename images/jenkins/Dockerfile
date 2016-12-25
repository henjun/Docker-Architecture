FROM localhost:5000/tomcat:0.1
MAINTAINER noeyhjun kim <kane7274@gmail.com>



# Install Node.js 6.x 
RUN  curl -sL https://deb.nodesource.com/setup_6.x | bash - && \
apt-get install -y nodejs

# jenkins download
RUN wget --quiet --no-cookies http://mirrors.jenkins.io/war-stable/latest/jenkins.war -O /${CATALINA_HOME}/webapps/jenkins.war

EXPOSE 8080
EXPOSE 8009

WORKDIR /opt/tomcat/bin

# Launch Tomcat
CMD ["./startup.sh"]
