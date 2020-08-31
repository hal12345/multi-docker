FROM node:alpine as builder
WORKDIR '/app'
COPE ./package.json ./
RUN npm install
COPY . .
RUN npm run builde

FROM nginx
EXPORT 3000
COPY ./nginx/default.conf /etc/nginx/codf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html
