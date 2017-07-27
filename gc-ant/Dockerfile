FROM oscm-sles-based

ENV JAVA_HOME /usr/lib64/jvm/java-1.8.0-openjdk
ENV ANT_HOME /usr/share/ant

RUN export http_proxy=$HTTP_PROXY && \
    export https_proxy=$HTTPS_PROXY
    
RUN echo http_proxy    
RUN echo https_proxy
     
RUN zypper -n in \
    java-1_8_0-openjdk \
    java-1_8_0-openjdk-devel \
    ant \
    wget
    
RUN wget https://repo1.maven.org/maven2/org/apache/ivy/ivy/2.4.0/ivy-2.4.0.jar  -O $ANT_HOME/lib/ivy.jar

ENTRYPOINT ["ant"]
