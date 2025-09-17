FROM ubuntu:22.04
RUN apt-get update && apt-get install -y squid apache2-utils && rm -rf /var/lib/apt/lists/*
COPY squid.conf /etc/squid/squid.conf
# copy passwd if you want it baked in (not recommended for secrets)
# COPY passwd /etc/squid/passwd
VOLUME ["/var/log/squid"]
EXPOSE 3128
CMD ["/usr/sbin/squid", "-N", "-f", "/etc/squid/squid.conf"]