FROM python:3.6-buster
ENV http_proxy "http://10.246.170.130:3128"
ENV https_proxy "http://10.246.170.130:3128"
COPY requirements_demo.txt .
RUN pip install -r requirements_demo.txt
ENV http_proxy ""
ENV https_proxy ""
ENTRYPOINT cd /server && python ./config.py --mode=demo
