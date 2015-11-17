FROM node
RUN apt-get update
ADD . /data
WORKDIR /data
RUN npm install -g grunt-cli
RUN npm install -g bower
RUN npm install 
RUN bower install --allow-root
CMD grunt serve
