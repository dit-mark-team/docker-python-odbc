FROM python:3.7-slim-stretch

RUN apt-get update \
    && apt-get install -y \
        curl \
        nano \
        apt-transport-https \
        make \
        build-essential \
        gnupg2 \
        tzdata \
        python3-dev \
        libpq-dev \
        make \
        build-essential \
        unixodbc \
        unixodbc-dev

RUN ln -fs /usr/share/zoneinfo/America/Fortaleza /etc/localtime && dpkg-reconfigure -f noninteractive tzdata

RUN pip3 install --upgrade pip
ADD requirements.txt .
RUN pip3 install -r requirements.txt

RUN echo "---> Cleaning up" \
 && apt-get autoremove -y \
 && apt-get autoclean -y \
 && apt-get clean -y \
 && rm -rf /tmp/*

WORKDIR /application
