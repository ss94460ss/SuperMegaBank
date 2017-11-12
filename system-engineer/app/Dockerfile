#FROM ubuntu:latest
MAINTAINER Sue Samuel "sue.samuel@bigpond.com"
RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential
#CMD ["cd", "system-engineer"]
COPY . /app
WORKDIR /app
RUN pip install virtualenv
ADD requirements.txt app/requirements.txt
RUN pip install -r requirements.txt
#ADD app.py app/app.py
ENTRYPOINT ["python"]
CMD ["app.py"]

