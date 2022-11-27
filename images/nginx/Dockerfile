FROM nginx:latest
WORKDIR /var/www
COPY conf/index.html /usr/share/nginx/html/index.html
ADD conf/hosts/* /etc/nginx/conf.d/
ADD CA/fullchain.pem /etc/nginx/ssl/
ADD CA/privkey.pem /etc/nginx/ssl/
RUN mkdir -p /var/www/frontend
RUN chown -R www-data:www-data /var/www/frontend/
RUN chmod -R 775 /var/www/frontend/
EXPOSE 80 443