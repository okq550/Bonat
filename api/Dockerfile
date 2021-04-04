FROM node:14

# Create app directory
WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install
# RUN npm install pm2 -g && pm2 update
RUN npm install -g nodemon && npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

EXPOSE 3000
# CMD ["pm2-runtime","bin/www","--watch --log"]
CMD [ "nodemon", "bin/www"]
# CMD ["pm2-runtime", "bin/www"]
# CMD ["pm2", "logs"]
# ubuntu-s-1vcpu-1gb-lon1-01