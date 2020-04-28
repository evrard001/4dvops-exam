#base image python image
FROM python:2.7-stretch


#Image maintainer
MAINTAINER SOMS ADJE ARNOLD EVRARD - 290309@supinfo.com


#source code API
ADD ./student_age.py  /


#Prerequisite
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y  &&  pip install flask flask_httpauth flask_simpleldap python-dotenv


#Persistent data (volume)
RUN mkdir /data

#API Port
EXPOSE 5000


#CMD
CMD [ "python", "./student_age.py" ]


#docker run --mount type=bind,source=/Users/mac/Documents/formations/SUPINFO/Docker/exam/correction/student-list/simple_api/data,target=/data  exam:v1
#curl -u toto:python -X GET http://127.0.0.1:32770/pozos/api/v1.0/get_student_ages
