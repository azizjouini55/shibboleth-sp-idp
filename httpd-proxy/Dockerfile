FROM httpd:latest



COPY httpd-foreground /usr/local/bin/
COPY etc-httpd/ /etc/httpd/
COPY var-www-html/ /var/www/html/

RUN chmod +x /usr/local/bin/httpd-foreground

EXPOSE 80 443

CMD ["httpd-foreground"]