FROM python:3.6

ENV PYTHONUNBUFFERED 1

RUN apt-get update && apt-get install -y \
	default-libmysqlclient-dev \
	gcc

RUN useradd -ms /bin/bash [USER]
COPY ./webapp home/[USER]/webapp
WORKDIR home/[USER]/webapp
RUN pip install -r requirements/prod.txt
RUN python manage.py collectstatic --noinput
RUN chown -R [USER]:[USER] .
USER [USER]
