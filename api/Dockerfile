#Base Image
FROM python:3.10-slim

# Install netcat
RUN apt-get update && \
    apt-get -y install netcat-traditional && \
    apt-get clean && \
    apt-get install -y libpq-dev build-essential

# Set working directory
WORKDIR /usr/src/app

# Add and install requirements
COPY ./requirements.txt /usr/src/app/requirements.txt
RUN  pip install --no-cache-dir -r requirements.txt

# Add app
COPY . /usr/src/app

# Run server
CMD python index.py run -h 0.0.0.0