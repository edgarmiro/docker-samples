FROM openjdk:8-jdk-alpine3.8

ARG VERSION=artifactory-oss-6.4.1
ARG FILE=jfrog-${VERSION}.zip
ARG URL=https://bintray.com/artifact/download/jfrog/artifactory/${FILE}

RUN set -ex \
    && apk add --no-cache \
    	wget \
    	unzip \
    && wget ${URL} \
    && unzip ${FILE} \
    && cd bin \
  	&& sed -ri 's/2g/512m/g' artifactory.default

EXPOSE 8081

WORKDIR /${VERSION}/bin

CMD ["ash", "artifactory.sh"]