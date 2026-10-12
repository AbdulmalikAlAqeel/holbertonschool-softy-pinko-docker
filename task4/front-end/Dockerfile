# Use the latest official Nginx image as the base
FROM nginx:latest

# Copy the front-end static files to Nginx's default web root directory
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the custom Nginx configuration file to the container's configuration directory
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
