FROM ubuntu:latest
MAINTAINER Sue Samuel "sue.samuel@bigpond.com"
RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential
COPY . /app
WORKDIR /app
RUN pip install virtualenv
RUN pip install -r requirements.txt
ENTRYPOINT ["python"]
CMD ["app.py"]

