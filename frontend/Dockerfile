# develop stage
FROM node:14 as buildenv
WORKDIR /app

RUN npm install -g @quasar/cli

COPY ./package*.json ./
COPY ./quasar.conf.js ./
RUN npm install

COPY . .
RUN quasar build -m pwa

#FROM nginx:stable as production-stage
#RUN mkdir /app
#COPY --from=buildenv /app/dist/pwa /usr/share/nginx/html

#RUN rm /etc/nginx/conf.d/default.conf
#COPY ./nginx.conf /etc/nginx/conf.d
