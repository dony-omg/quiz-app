FROM node:latest

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is use to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)

# COPY package*.json ./
# COPY prisma ./prisma/

# Copy package.json in current dir
COPY ["package.json", "package-lock.json", "./prisma", "./"]

RUN npm install

# If you are building your code production
# RUN npm ci --only=production

# Bundle app source
COPY . .

# RUN npm run dev

EXPOSE 3000

# Run app
# CMD ["ts-node","./src/index.ts"]
CMD [ "npm", "run", "dev" ]

