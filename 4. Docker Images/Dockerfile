FROM Ubuntu

RUN apt-get update
RUN apt-get install python

RUN pip install flask
RUN pip install flask-mysql

COPY . /opt/source-code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run

============================================================================================

// we have the following steps to run a simple python flask based web application

1. apt-get update
2. apt-get install -y python
3. apt-get install python-pip
4. pip install flask
5. create/copy the application codeto /opt/app.py
6. FLASK_APP=/opt/app.py flask run --host=0.0.0.0

If we want to create a container for the application then the Dockerfile would look something like this

FROM Ubuntu

RUN apt-get update
RUN apt-get install -y python
RUN apt-get install python-pip
RUN pip install flask

COPY app.py /opt/app.py

ENTRYPOINT FLASK_APP=/opt/app.py flask run --host=0.0.0.0