FROM jenkins/slave:alpine
ARG HELM_VERSION=3.6.3
USER root
RUN apk upgrade
RUN wget https://get.helm.sh/helm-v$HELM_VERSION-linux-amd64.tar.gz
RUN tar -zxvf helm-v$HELM_VERSION-linux-amd64.tar.gz
RUN mv linux-amd64/helm /usr/local/bin/
RUN rm -rf helm-v$HELM_VERSION-linux-amd64.tar.gz && rm -rf linux-amd64
RUN helm version 
USER jenkins
