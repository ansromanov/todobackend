FROM ansromanov/todobackend-base:latest
MAINTAINER Andrey Romanov <ansromanov@gmail.com>

COPY target /wheelhouse

# Install dev/build dependencies
RUN apt-get update && \
    apt-get install -qy python-dev libmysqlclient-dev

# Activate virtual environment and install wheel support
RUN . /appenv/bin/activate && \
    pip install --no-index -f /wheelhouse todobackend && \
    rm -rf /wheelhouse