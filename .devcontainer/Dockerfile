FROM mcr.microsoft.com/devcontainers/python:0-3.11

COPY requirements.txt /tmp/

RUN echo "(*) Installing tools..." \
    && pip install -r /tmp/requirements.txt

RUN apt-get update \
    && apt-get upgrade -y \
    && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends make

COPY welcome-message.txt /usr/local/etc/vscode-dev-containers/first-run-notice.txt
