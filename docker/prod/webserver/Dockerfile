FROM nginx:latest

RUN rm /etc/nginx/conf.d/default.conf

COPY ./docker/prod/webserver/plateforme_webapp.conf /etc/nginx/conf.d/
