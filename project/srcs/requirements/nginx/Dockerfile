FROM alpine:3.19

RUN apk update && apk upgrade && apk add --no-cache nginx openssl

RUN mkdir -p /etc/nginx/ssl && openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/ssl/ajakob.42.fr.key -out /etc/nginx/ssl/ajakob.42.fr.crt -subj "/C=DE/ST=Baden Wurttemberg/L=Heilbronn/O=42/OU=42/CN=ajakob.42.fr"

EXPOSE 443

CMD ["nginx", "-g", "daemon off;"]
