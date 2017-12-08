FROM java:8
VOLUME /tmp
ADD moxi-0.0.1-SNAPSHOT.jar app.jar
RUN bash -c 'touch /app.jar'
#可以通过配置 JRE 使用非阻塞的 Entropy Source
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]