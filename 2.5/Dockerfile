#
# Dockerfile for Docker Registry with grsecurity kernel
#

# VERSION 2.5.0

FROM registry:2.5

ADD registry /usr/local/bin/registry
RUN apk add --no-cache attr \
# apt-get update && apt-get install attr \
# 	&& apt-get clean && rm -rf /var/lib/apt/lists/* \
	&& chmod +x /usr/local/bin/registry

ENTRYPOINT ["/usr/local/bin/registry"]
CMD ["/etc/docker/registry/config.yml"]
