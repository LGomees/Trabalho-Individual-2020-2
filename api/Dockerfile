FROM python:3.8

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apt-get update
RUN apt install -y netcat

RUN mkdir /api
WORKDIR /api

ADD . /api/
COPY requirements.txt manage.py api task /api/

COPY test_api.sh /test_api.sh
RUN chmod +x /test_api.sh

RUN pip install -r requirements.txt
RUN apt-get update




