FROM ubuntu:16.04
#FROM alpine:3.7
LABEL maintainer="djr@DanielRabinowitz.com"
WORKDIR /work
#RUN apk add --no-cache bash xorriso

RUN apt-get update && \
    apt-get -y install \
    isolinux xorriso syslinux genisoimage gettext-base

CMD /work/docker/update_iso
