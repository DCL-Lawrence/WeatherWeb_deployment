FROM python:3

WORKDIR /

RUN apt-get update -y && apt-get install build-essential -y && \
    wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && \
    apt-get install -y -f ./google-chrome-stable_current_amd64.deb && \
    apt-get install -y python3-pip && mkdir /work

ADD re.txt /work/re.txt

CMD cd /work && pip3 install -r re.txt && pip3 install -U beautifulsoup4 && \
    git clone https://github.com/DCL-Lawrence/WeatherWeb_Backend.git && \
    cd WeatherWeb_Backend && python3 manage.py runserver 0.0.0.0:8000
