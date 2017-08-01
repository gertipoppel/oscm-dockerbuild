FROM oscm-sles-based

ENV JAVA_HOME /usr/lib64/jvm/java-1.8.0-openjdk
ENV ANT_HOME /usr/share/ant
ENV http_proxy $HTTP_PROXY 
ENV https_proxy $HTTPS_PROXY
    
RUN echo $http_proxy    
RUN echo $https_proxy
     
RUN zypper -n in \
    java-1_8_0-openjdk \
    java-1_8_0-openjdk-devel \
    unzip \
    wget

RUN wget http://archive.apache.org/dist/ant/binaries/apache-ant-1.9.6-bin.zip -O /opt/ant.zip
RUN unzip /opt/ant.zip -d /opt/  
RUN wget https://repo1.maven.org/maven2/org/apache/ivy/ivy/2.4.0/ivy-2.4.0.jar  -O $ANT_HOME/lib/ivy.jar

ENTRYPOINT ["/opt/apache-ant-1.9.6/bin/ant"]
