FROM almalinux:8 as builder
RUN yum index nginx -y 
RUN rm -rf /usr/share/nginx/html/index.html
COPY index.html /usr/share/nginx/html/
ADD https://github.com/PraveenKumar8919/Notes/blob/main/README.md /tmp/notes.txt
CMD [ "nginx", "-g", "daemon off;" ]

FROM python:3.9-slim
RUN apt-get update && apt-get install -y
COPY --from=builder /usr/share/nginx/html/index.html /usr/share/nginx/html/index.html
COPY --from=builder /tmp/notes.txt /tmp/notes.txt