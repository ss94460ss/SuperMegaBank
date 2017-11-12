#FROM ubuntu:latest
MAINTAINER Sue Samuel "sue.samuel@bigpond.com"
RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential
COPY . /testing
WORKDIR /testing
#RUN pip install virtualenv
ADD requirements.txt testing/requirements.txt
RUN pip install -r testing/requirements.txt
#ENV PYTHONPATH $PYTHONPATH:/system-engineer/app
ENTRYPOINT ["python"]
CMD ["testing.py"]
EXPOSE 5001

