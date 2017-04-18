FROM python:2.7.13-alpine

ENV PYTHONUNBUFFERED 1
ENV PYCURL_SSL_LIBRARY openssl

RUN apk update && apk add --no-cache curl curl-dev gcc g++

RUN pip install pycurl

COPY . /wfuzz
WORKDIR /wfuzz

ENTRYPOINT ["/usr/local/bin/python", "wfuzz.py"]
