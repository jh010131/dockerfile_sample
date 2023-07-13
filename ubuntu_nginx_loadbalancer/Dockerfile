FROM ubuntu:focal
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get install -y nginx
COPY nginx/sites-available/loadbalancer /etc/nginx/sites-available/loadblancer
RUN rm -f /etc/nginx/sites-enabled/default
RUN ln -s /etc/nginx/sites-available/loadblancer /etc/nginx/sites-enabled/loadbalancer
CMD ["nginx", "-g", "daemon off;"]
EXPOSE 80
