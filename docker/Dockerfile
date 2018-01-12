FROM nginx:alpine

# Copying the configuration and html files inside docker image
COPY *.conf /etc/nginx/conf.d/
COPY *.html /usr/share/nginx/html/

# Creating necessary directories and symlinks as per requirement
RUN mkdir -p /usr/share/nginx/hello/html
RUN ln -s /usr/share/nginx/html/1.html /usr/share/nginx/hello/html/index.html

