FROM ubuntu

# install dev tools
RUN apt-get update
RUN apt-get install -y nodejs nodejs-legacy npm git

# node stuff
RUN npm install nodemon -g

# app folder
RUN mkdir -p /src

# set it to our working folder
WORKDIR /src

# link our local folder
ADD . /src

# install node modules
RUN npm install

# Expose port 3000
EXPOSE 3000

# Start NPM?
CMD nodemon index.js
