FROM namespace/weathervane-centos7:version
MAINTAINER hrosenbe@vmware.com

COPY weathervane.pl /root/weathervane/weathervane.pl
COPY runHarness /root/weathervane/runHarness
COPY ssh /root/.ssh
COPY Notice.txt /root/weathervane/Notice.txt

ENV  JAVA_HOME /usr/lib/jvm/java-1.8.0	

RUN yum install -y perl-App-cpanminus && \
	yum install -y wget && \
	yum install -y curl && \
	yum install -y lynx && \
	yum install -y gcc && \
	yum install -y openssh-clients && \
	yum install -y docker-client && \
	mkdir /root/weathervane/dist && \
	chmod -R 600 /root/.ssh && \yum install
	cpanm YAML && \
	cpanm Config::Simple && \
	cpanm String::Util && \
	cpanm Statistics::Descriptive && \
	cpanm Moose && \
	cpanm MooseX::Storage && \
	cpanm Tie::IxHash && \
	cpanm MooseX::ClassAttribute && \
	cpanm MooseX::Types && \
	cpanm JSON && \
	cpanm Switch && \
	cpanm Log::Log4perl && \
	cpanm Log::Dispatch::File && \
	cpanm LWP 

ENTRYPOINT ["perl", "/root/weathervane/weathervane.pl"]
