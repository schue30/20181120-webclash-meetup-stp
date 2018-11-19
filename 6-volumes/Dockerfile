FROM centos:7

RUN yum install -y epel-release && \
    yum install -y python34-pip && \
    pip3 --no-cache-dir install Flask && \
    yum clean all

USER 1000

ENV FLASK_APP=/app.py \
    LC_ALL=en_US.utf8
ENTRYPOINT [ "flask", "run", "--host=0.0.0.0" ]

EXPOSE 5000
VOLUME /data

ADD app.py /app.py

