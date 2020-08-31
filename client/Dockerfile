FROM node:alpine as builder
WORKDIR '/app'
COPY ./package.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx
EXPORT 3000
COPY ./nginx/default.conf /etc/nginx/codf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html
