FROM centos:7
MAINTAINER "Sami Kallio" <sami.kallio@gofore.com>

RUN yum -y install sudo git rpm-build java-1.8.0-openjdk-headless
RUN yum clean all
RUN sed -i 's/requiretty/!requiretty/' /etc/sudoers

USER jenkins
CMD ["sh", "-c", "/workspace/src/packages/build-xroad-rpm.sh && /workspace/src/packages/build-jetty-rpm.sh" ]
