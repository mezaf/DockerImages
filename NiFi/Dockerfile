FROM ubuntu:16.04
RUN apt-get --assume-yes update && apt-get --assume-yes upgrade
RUN apt-get --assume-yes install default-jdk
RUN apt-get --assume-yes install vim
RUN apt-get --assume-yes install wget
RUN apt-get --assume-yes install git
RUN mkdir /opt/nifi && cd /opt/nifi
RUN wget http://apache.dattatec.com/nifi/nifi-registry/nifi-registry-0.5.0/nifi-registry-0.5.0-bin.tar.gz
RUN tar xzvf nifi-registry-0.5.0-bin.tar.gz
RUN rm nifi-registry-0.5.0-bin.tar.gz
VOLUME /home/mezaf/Documents/NiFi_IaC/shared_folder
CMD ["/bin/bash"]