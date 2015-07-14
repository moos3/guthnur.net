FROM debian:jessie

RUN \
    apt-get update && \
    apt-get install --no-install-recommends -y ca-certificates git-core && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
    git clone http://github.com/moos3/guthnurnet.git /src
VOLUME ["/src"]
WORKDIR /src
ENTRYPOINT ["git"]
CMD ["pull"]
