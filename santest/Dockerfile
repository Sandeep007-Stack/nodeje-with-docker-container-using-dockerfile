FROM node:14.8.0-alpine
RUN mkdir -p /var/www/santest/
COPY package*.json ./var/www/santest/
WORKDIR /var/www/santest
RUN npm install -g npm@6.14.7 nodemon
RUN npm install
ENV PATH /var/www/santest/node_modules/.bin:$PATH
COPY . .
EXPOSE ${PORT}
CMD ["npm", "start"]