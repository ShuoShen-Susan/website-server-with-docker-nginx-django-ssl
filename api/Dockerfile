# syntax=docker/dockerfile:1
FROM python:3.9.6-alpine

WORKDIR /home/api

# install psycopg2 dependencies
RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev

RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

COPY . .


