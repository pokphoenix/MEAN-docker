# Import the official NodeJS image; which sets up node for us in the container
#FROM node:argon

# Create app directory
#RUN mkdir -p /usr/src/app
#WORKDIR /usr/src/app

# Install app dependencies
#COPY package.json /usr/src/app/
#RUN npm install

# Bundle app source
#COPY . /usr/src/app

# Run a command with arguments
#CMD [ "node", "test-run.js" ]


#FROM node:10

# Create app directory
#RUN mkdir -p /usr/src/app
#WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
#COPY package.json /usr/src/app

#RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
#COPY . .

#EXPOSE 3000
#CMD [ "node", "server" ]

FROM node:10-alpine

ENV INSTALL_PATH /usr/src/app

RUN mkdir -p $INSTALL_PATH
WORKDIR $INSTALL_PATH
COPY package.json $INSTALL_PATH
#RUN npm cache clean
RUN npm install
COPY . $INSTALL_PATH
EXPOSE 3000
CMD ["npm","start"]