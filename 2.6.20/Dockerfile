FROM centos:6

WORKDIR /workspace

RUN yum update -y && yum upgrade -y && yum install gcc ncurses-devel curl git gdb vim zsh -y && yum clean all

RUN git clone https://github.com/bytebody/linux-2.6.20  linux 
RUN  cd /workspace/linux &&  git checkout -b develop 

CMD ["tail" ,"-f", "/var/log/yum.log" ]
