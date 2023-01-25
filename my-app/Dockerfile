# pull the base image
FROM node:alpine

# set the working direction
WORKDIR /my-app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /my-app/node_modules/.bin:$PATH

# install app dependencies
COPY package.json ./

COPY yarn.lock ./

RUN npm install

# add app
COPY . ./

# start app
CMD ["yarn", "run"]
