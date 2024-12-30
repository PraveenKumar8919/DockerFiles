ARG version
FROM centos:${version}
ARG username
RUN adduser $username
USER $username
ARG course
ARG Trainer
RUN echo "course: ${course}, Trainer: ${Trainer}}"
#we are passing args values to env 
ENV course=${course}
ENV Trainer=${Trainer}               
CMD [ "sleep", "100" ]
