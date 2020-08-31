FROM node:alpine
WORKDIR "/app"
COPY ./package.json ./
RUN npm install
COPY . .
// START IS DEFINED INT PACKAGE JASON
CMD ["npm", "run", "start"]
