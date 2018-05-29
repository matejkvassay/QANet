FROM ubuntu:18.04
RUN apt-get update \
  && apt-get install -y python3-pip python3-dev \
  && cd /usr/local/bin \
  && ln -s /usr/bin/python3 python \
  && pip3 install --upgrade pip
COPY requirements_demo.txt .
RUN pip install -r requirements_demo.txt
ENTRYPOINT cd /server && python ./config.py --mode=demo