FROM haproxy

USER root
RUN mkdir -p /usr/local/etc/ssl
USER haproxy

COPY haproxy.cfg /usr/local/etc/haproxy/
COPY fullchainandkey.pem /usr/local/etc/ssl
COPY dhparam.pem /usr/local/etc/ssl

