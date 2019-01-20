FROM node:alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build
# new FROM statements begin a new block / terminate old blocks
FROM nginx 
COPY --from=builder /app/build /usr/share/nginx/html
