FROM gcr.io/jenkinsxio/builder-base:0.0.81

RUN yum-config-manager --add-repo https://packages.cloudfoundry.org/fedora/cloudfoundry-cli.repo \
  && yum install -y cf-cli \
  && yum clean all

# jx
ENV JX_VERSION 2.1.30
RUN curl -f -L https://github.com/jenkins-x/jx/releases/download/v${JX_VERSION}/jx-linux-amd64.tar.gz | tar xzv && \
  mv jx /usr/bin/

CMD ["cf","--version"]
