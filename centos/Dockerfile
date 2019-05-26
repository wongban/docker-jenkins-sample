FROM centos:latest
MAINTAINER James Turnbull "james@example.com"
RUN cd /etc/yum.repos.d/ && rm -rf *
RUN wget http://mirrors.163.com/.help/CentOS7-Base-163.repo
RUN wget http://mirrors.aliyun.com/repo/epel-7.repo
RUN yum clean all && yum makecache
ENV REFRESHED_AT 2016-06-01
RUN yum -y install ruby rubygems rubygem-rake
RUN gem install --no-rdoc --no-ri rspec ci_reporter_rspec
