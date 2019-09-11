FROM ubuntu:16.04
COPY requirements.txt /opt
RUN apt-get --assume-yes update && apt-get --assume-yes upgrade
RUN apt-get --assume-yes install default-jdk
RUN apt-get --assume-yes install vim
RUN apt-get --assume-yes install wget
RUN apt-get --assume-yes install git
RUN mkdir /opt/nifi 
RUN cd /opt/nifi && wget http://apache.dattatec.com/nifi/nifi-registry/nifi-registry-0.5.0/nifi-registry-0.5.0-bin.tar.gz
RUN cd /opt/nifi && tar xzvf nifi-registry-0.5.0-bin.tar.gz
RUN cd /opt/nifi && rm nifi-registry-0.5.0-bin.tar.gz
RUN apt-get --assume-yes install python3
RUN apt-get --assume-yes install python3-pip
RUN pip3 install -r requirements.txt
EXPOSE 18080 18443
VOLUME /opt/nifi/
CMD ["/bin/bash"]