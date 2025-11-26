FROM httpd:2.4

RUN sed -i 's/#LoadModule proxy_module/LoadModule proxy_module/' /usr/local/apache2/conf/httpd.conf \
    && sed -i 's/#LoadModule proxy_fcgi_module/LoadModule proxy_fcgi_module/' /usr/local/apache2/conf/httpd.conf \
    && sed -i 's/#LoadModule rewrite_module/LoadModule rewrite_module/' /usr/local/apache2/conf/httpd.conf

COPY laravel.conf /usr/local/apache2/conf/extra/laravel.conf

RUN echo "\nInclude conf/extra/laravel.conf" >> /usr/local/apache2/conf/httpd.conf