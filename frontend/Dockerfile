# build stage
FROM node:16-alpine as build-stage
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build

# production stage
FROM nginx:stable-alpine as production-stage
COPY  ./nginx/nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=build-stage /app/build /usr/share/nginx/html
CMD ["nginx", "-g", "daemon off;"]
