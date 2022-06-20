FROM node:latest as base

# Create app directory
WORKDIR /src
COPY  package*.json /
EXPOSE 3000


# FROM base as production
# ENV NODE_ENV=production

# # Copy package.json in current dir
# COPY ["package.json", "package-lock.json", "./prisma", "./"]

# # If you are building your code production
# RUN npm ci
# # Bundle app source
# COPY . .
# CMD [ "npm","start" ]

FROM base as dev
ENV NODE_ENV=development
# Copy package.json in current dir
COPY ["package.json", "package-lock.json", "./prisma", "./"]
RUN npm install -g nodemon && npm install
# Bundle app source
COPY . /
CMD ["nodemon", "bin/www"]
# Install app dependencies
# A wildcard is use to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)

# COPY package*.json ./
# COPY prisma ./prisma/



#RUN npm install

# If you are building your code production
# RUN npm ci --only=production

# Bundle app source
#COPY . .


# Run app
#CMD ["ts-node","./src/index.ts"]
#CMD [ "npm", "run", "dev" ]

