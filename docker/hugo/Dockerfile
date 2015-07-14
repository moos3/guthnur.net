FROM golang:latest

RUN \
    apt-get update && \
    apt-get install --no-install-recommends -y \
    bzr \
    wget \
    python-pip && \
    wget https://github.com/spf13/hugo/releases/download/v0.13/hugo_0.13_amd64.deb && \
    dpkg -i hugo*
VOLUME ["/blog"]
ENTRYPOINT ["/usr/bin/hugo"]
CMD ["-w", "-s", "/src", "-d", "/blog"]
EXPOSE 1313
