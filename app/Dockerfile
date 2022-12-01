# syntax=docker/dockerfile:1
FROM node:12-alpine
RUN apk add --no-cache python2 g++ make
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
echo "ALTER USER 'root' IDENTIFIED WITH mysql_native_password BY 'secret'; flush privileges;" | mysql -psecret"
