# Step 1: Build the app in image 'builder'
# FROM node:12.0.0-alpine AS builder

# RUN npm config set unsafe-perm true
# RUN npm config set registry https://registry.npm.taobao.org
# RUN npm install -g @angular/cli

# WORKDIR /usr/src/app
# COPY . .
# RUN npm install  -y
# RUN npm run build

# Step 2: Use build output from 'builder'
FROM nginx:stable-alpine
LABEL version="1.0"

COPY nginx.conf /etc/nginx/nginx.conf
WORKDIR /usr/share/nginx/html
# COPY --from=builder /usr/src/app/dist/tower-web/ .
# COPY tower-web/ .
# docker build -t tower-nginx:1.0 nginx/