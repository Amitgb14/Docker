FROM fedora:latest

MAINTAINER Amit Ghadge (amitg.b14@gmail.com)

RUN dnf -y install python
RUN dnf -y install git
RUN dnf -y install xz
RUN dnf -y install bzip2
RUN pip install six

WORKDIR /usr/src/app

RUN git clone https://github.com/sosreport/sos.git
RUN cat sos/sos.conf >> /etc/sos.conf

WORKDIR /usr/src/app/sos

CMD ["python", "./sosreport", "--batch"]

