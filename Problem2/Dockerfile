FROM httpd:latest

# Copy the HTML file
COPY index.html /usr/local/apache2/htdocs/
# Copy a new configuration file to listen on port 9999 instead of 80
COPY my-httpd.conf /usr/local/apache2/conf/httpd.conf

RUN mkdir -p /var/www/html
RUN chown -R www-data:www-data /var/www/html
# Open the port 9999 in the container
EXPOSE 9999

# Add environment variable CONTAINER with value docker
ENV CONTAINER docker

# Add startup command to echo the variable
CMD ["sh", "-c", "echo $CONTAINER && httpd-foreground"]

