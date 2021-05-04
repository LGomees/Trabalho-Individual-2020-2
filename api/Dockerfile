FROM python:3.8

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apt-get update
RUN apt install -y netcat

RUN mkdir /api
WORKDIR /api

ADD . /api/
COPY requirements.txt manage.py api task /api/

RUN pip install -r requirements.txt
RUN apt-get update

RUN chmod +x /api/entrypoint.sh

CMD ["/api/entrypoint.sh"]



