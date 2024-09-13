# https://hub.docker.com/_/node
ARG NODE_VERSION=22

FROM node:${NODE_VERSION}

LABEL maintainer=ferdz
LABEL build_on="Sept 2, 2024"

## how to build
WORKDIR /APP_PORT

#Inside /app
#Copy my src

# Copy from local computer
COPY main.js
COPY package*.jason .
COPY public public
COPY views views

# install node modules
RUN npm ci

# how to run 
ENV APP_PORT=5000

# what are the exposed port
EXPOSE ${APP_PORT}

# run the app
ENTRYPOINT node main.js ${APP_PORT}