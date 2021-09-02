FROM jenkins/slave:alpine
ARG TERRAFORM_VERSION=1.0.5
ARG TERRAGRUNT_VERSION=0.31.8
USER root
RUN apk upgrade
RUN wget "https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip"
RUN unzip "terraform_${TERRAFORM_VERSION}_linux_amd64.zip"
RUN mv terraform /usr/local/bin/
RUN rm -rf "terraform_${TERRAFORM_VERSION}_linux_amd64.zip"
RUN terraform -version
RUN wget "https://github.com/gruntwork-io/terragrunt/releases/download/v${TERRAGRUNT_VERSION}/terragrunt_linux_amd64"
RUN mv terragrunt_linux_amd64 /usr/local/bin/terragrunt
RUN chmod +x  /usr/local/bin/terragrunt
RUN  terragrunt --version
USER jenkins
