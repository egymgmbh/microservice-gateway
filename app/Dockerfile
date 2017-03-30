FROM nginx:latest

RUN rm /etc/nginx/conf.d/*

COPY index.html /usr/share/nginx/html

COPY /webcomponentsjs/ /usr/share/nginx/html/webcomponentsjs

COPY default.conf /etc/nginx/conf.d/