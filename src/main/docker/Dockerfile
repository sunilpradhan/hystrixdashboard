# Start with a base image containing Java runtime
#FROM openjdk:8-jdk-alpine
FROM java:8

# Add Maintainer Info
LABEL maintainer="SKP"

# Add a volume pointing to /tmp
VOLUME /tmp


# Add the application's jar to the container
ADD hystrixdashboard-0.0.1-SNAPSHOT.jar hystrixdashboard.jar

#RUN bash -c 'touch /hystrixdashboard.jar'
# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/hystrixdashboard.jar"]

EXPOSE 8080
