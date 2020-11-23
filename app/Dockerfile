FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install -y -q python-all python-pip
ADD requirements.txt .
RUN mkdir /opt/webapp
RUN chmod 755 /opt/webapp
ADD app.py /opt/webapp
RUN chmod 755 /opt/webapp/app.py
RUN pip install -qr requirements.txt
EXPOSE 5000
CMD ["python", "/opt/webapp/app.py"]

