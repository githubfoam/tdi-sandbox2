FROM ubuntu:18.04
RUN apt-get update && \
  apt-get install -y software-properties-common && \
  apt-add-repository ppa:ansible/ansible && \
  apt-get update && \
  apt-get install ansible -y
RUN ansible-galaxy install githubfoam.openvswitch
