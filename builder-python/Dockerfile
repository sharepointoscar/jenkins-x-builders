FROM gcr.io/jenkinsxio/builder-base:0.0.30

RUN yum install -y https://centos7.iuscommunity.org/ius-release.rpm
RUN yum install -y python36u python36u-libs python36u-devel python36u-pip && yum clean all
RUN ln -s /usr/bin/python3.6 /usr/bin/python3

# jx
ENV JX_VERSION 2.0.22
RUN curl -f -L https://github.com/jenkins-x/jx/releases/download/v${JX_VERSION}/jx-linux-amd64.tar.gz | tar xzv && \
  mv jx /usr/bin/

CMD ["python3", "--version"]
