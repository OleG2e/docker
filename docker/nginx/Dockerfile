FROM nginx:1.21.4-alpine

ADD nginx.conf /etc/nginx/
ADD www.conf /etc/nginx/conf.d/
ADD cors_headers /etc/nginx/
ADD cors_options_response /etc/nginx/

EXPOSE 80

CMD ["nginx"]
