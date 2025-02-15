FROM node:16-slim

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY GeoAPI_GIT/package*.json ./

# RUN npm install
# If you are building your code for production
RUN npm ci --omit=dev

# Bundle app source
COPY GeoAPI_GIT/src/ ./src
COPY GeoAPI_GIT/routines/ ./routines
COPY GeoAPI_GIT/configs.json .

ENV NODE_ENV production
EXPOSE 8080
# USER nobody
CMD [ "npm", "start" ]
