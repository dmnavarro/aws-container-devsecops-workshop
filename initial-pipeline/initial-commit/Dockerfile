FROM python:3.7-slim-buster

LABEL maintainer="otter"

RUN adduser otter
COPY . /app

WORKDIR /app
RUN pip install -r requirements.txt

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 5000

USER otter

CMD python ./index.py
