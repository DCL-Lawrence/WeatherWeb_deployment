FROM httpd:2.4

WORKDIR /

RUN apt-get update -y && apt-get install build-essential -y && \
    apt-get install git -y && \
    git clone https://github.com/DCL-Lawrence/WeatherWeb_Frontend.git && \
    cp  /WeatherWeb_Frontend/* /usr/local/apache2/htdocs/
