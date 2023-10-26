# Base Image
FROM python:3.10-slim  

# Install netcat
RUN apt-get update && \
    apt-get -y install netcat-traditional  && \
    apt-get clean && \
    apt-get install -y libpq-dev build-essential

# set working directory
WORKDIR /usr/src/app

# add and install requirements
COPY ./requirements.txt /usr/src/app/requirements.txt

RUN pip install --no-cache-dir -r requirements.txt


# add app
COPY . /usr/src/app

# run server
CMD python manage.py run -h 0.0.0.0