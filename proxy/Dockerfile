ARG NGINX_VERSION
FROM nginx:${NGINX_VERSION}

COPY nginx.conf /etc/nginx/nginx.conf
COPY xwiki.crt /etc/nginx/certs/xwiki.crt
COPY xwiki.key /etc/nginx/certs/xwiki.key
COPY xwiki.pass /etc/nginx/certs/xwiki.pass
