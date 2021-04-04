# pull official base image
FROM node:14.16.0-alpine

# set working directory
WORKDIR /usr/src/app

# add `/ui/node_modules/.bin` to $PATH
ENV PATH /ui/node_modules/.bin:$PATH

# install ui dependencies
COPY package*.json ./
RUN npm install --silent
# RUN npm install react-scripts@3.4.1 -g --silent

COPY . .
CMD ["npm", "start"]