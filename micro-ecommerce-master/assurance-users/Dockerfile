FROM java:8
MAINTAINER ;;ed.ingenieur@gmail.com
EXPOSE 8083
ADD target/*.jar /app.jar
RUN bash -c 'touch /app.jar'
ADD wait-for-it.sh /wait-for-it.sh
RUN bash -c 'chmod 777 /wait-for-it.sh'
CMD ["java","-Dspring.profiles.active=docker","-jar","/app.jar"]