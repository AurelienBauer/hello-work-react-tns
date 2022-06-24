FROM node:17.8.0 as build

EXPOSE 3000

RUN git clone https://github.com/AurelienBauer/hello-work-react-tns.git

WORKDIR /hello-work-react-tns

RUN npm install && npm run build

FROM nginx:1.21.6-alpine

COPY --from=build /hello-work-react-tns/build /usr/share/nginx/html
