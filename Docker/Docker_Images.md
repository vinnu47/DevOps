## how to create docker images

Docker file
```
FROM ubuntu

RUN apt-get update
RUN apt-get install -y python python-pip
RUN pip install flask
ENTRYPOINT FLASK_APP=/opt/app.py flask run --host=0.0.0.0