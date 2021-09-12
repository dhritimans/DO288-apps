# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"
LABEL io.openshift.tags="apache,http"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/run/httpd /var/lib/httpd && \
    chmod -R g=u /var/run/httpd /var/lib/httpd

USER 1001
