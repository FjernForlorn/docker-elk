ARG ELASTIC_VERSION
ARG ELASTIC_SOURCE
# https://www.docker.elastic.co/
FROM ${ELASTIC_SOURCE}:${ELASTIC_VERSION}

USER root

RUN set -eux; \
	mkdir /state; \
	chmod 0775 /state; \
	chown elasticsearch:root /state

USER elasticsearch:root

ENTRYPOINT ["/entrypoint.sh"]
