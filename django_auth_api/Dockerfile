# FROM python:3.8

# RUN apt-get update && apt-get install -y libpq-dev

# WORKDIR /app

# COPY . /app

# RUN pip install --no-cache-dir -r requirements.txt

# EXPOSE 8000

# ENV NAME World

# CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

# pull official base image

# FROM python:3.11.4-slim-buster

# # set work directory
# WORKDIR /usr/src/app

# # set environment variables
# ENV PYTHONDONTWRITEBYTECODE 1
# ENV PYTHONUNBUFFERED 1

# # install dependencies
# RUN pip install --upgrade pip
# COPY ./requirements.txt .
# RUN pip install -r requirements.txt

# # copy project
# COPY . .

# The first instruction is what image we want to base our container on
# We Use an official Python runtime as a parent image
FROM python:3.8

# The enviroment variable ensures that the python output is set straight
# to the terminal with out buffering it first
ENV PYTHONUNBUFFERED 1

# create root directory for our project in the container
RUN mkdir /music_service

# Set the working directory to /music_service
WORKDIR /music_service

# Copy the current directory contents into the container at /music_service
ADD . /music_service/

# Install any needed packages specified in requirements.txt
RUN pip install -r requirements.txt
