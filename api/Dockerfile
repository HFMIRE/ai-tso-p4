#Base Image
FROM python:3.7.2-slim

# Install netcat
RUN apt-get update && \
    apt-get -y install netcat && \
    apt-get clean

# Set working directory
WORKDIR /usr/src/app

# Add and install requirements
COPY ./requirements.txt /usr/src/requirements.txt
RUN  pip install -r requirements.txt

# Add app
COPY . /usr/src/api

# Run server
CMD python manage.py run -h 0.0.0.0