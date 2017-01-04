#
# Dockerfile for Docker Registry with grsecurity kernel
#

# VERSION 2.5.0

FROM registry:2.5

ADD registry /usr/local/bin/registry
RUN apk add --no-cache attr \
	&& chmod +x /usr/local/bin/registry

ENTRYPOINT ["/usr/local/bin/registry"]
CMD ["/etc/docker/registry/config.yml"]
