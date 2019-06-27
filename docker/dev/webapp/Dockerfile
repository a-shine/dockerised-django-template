FROM python:3.6

ENV PYTHONUNBUFFERED 1

RUN apt-get update && apt-get install -y \
	default-libmysqlclient-dev \
	gcc

RUN useradd -ms /bin/bash dev_user
COPY ./webapp home/dev_user/webapp
WORKDIR home/dev_user/webapp
RUN pip install -r requirements/dev.txt
RUN chown -R dev_user:dev_user .
USER dev_user