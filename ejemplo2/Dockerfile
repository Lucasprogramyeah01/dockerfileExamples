FROM httpd:2.4-alpine
LABEL maintainer=""
RUN apk add git
RUN git clone https://github.com/Lucasprogramyeah01/HTMLPrueba.git ./web 
RUN mv ./web/* /usr/local/apache2/htdocs/
#COPY holaMundo.html /usr/local/apache2/htdocs/