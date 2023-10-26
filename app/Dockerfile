FROM node:10.16.0-alpine

WORKDIR /usr/src/app
ENV PATH /usr/src/node_modules/.bin:$PATH

# Install and cache app dependencies
COPY package.json /usr/src/package.json

RUN npm install

EXPOSE 3000
CMD ["npm", "run", "dev"]