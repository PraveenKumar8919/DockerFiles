FROM almalinux:8
RUN yum index nginx -y 
RUN rm -rf /usr/share/nginx/html/index.html
COPY index.html /usr/share/nginx/html/
ADD https://github.com/PraveenKumar8919/Notes/blob/main/README.md /tmp/notes.txt
CMD [ "nginx", "-g", "daemon off;" ]
