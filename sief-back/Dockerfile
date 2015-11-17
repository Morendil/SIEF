FROM ubuntu
RUN apt-get update
RUN apt-get install -qy python3-pip
ADD . /data
WORKDIR /data
RUN pip3 install -r requirements.txt
EXPOSE 8000
ENV CORS_ORIGINS http://192.168.99.100:8001/
ENV MONGODB_URL mongodb://admin:D939SDzF4OKq@mongodb:27017/sief?authSource=admin
CMD gunicorn "sief.main:bootstrap_app()" --bind 0.0.0.0:8000 --log-file -
