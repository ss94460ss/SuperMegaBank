FROM ubuntu:latest
MAINTAINER Sue Samuel "sue.samuel@bigpond.com"
RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential
COPY . /testing
WORKDIR /testing
RUN pip install virtualenv
RUN pip install -r requirements.txt
ENTRYPOINT ["python"]
CMD ["testing.py"]

