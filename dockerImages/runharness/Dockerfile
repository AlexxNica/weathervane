FROM namespace/weathervane-centos7:version
MAINTAINER hrosenbe@vmware.com

COPY weathervane.pl /weathervane.pl
COPY runHarness /runHarness
	
RUN yum install -y perl-App-cpanminus && \
	yum install -y wget && \
	yum install -y curl && \
	yum install -y lynx && \
	yum install -y gcc && \
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

ENTRYPOINT ["perl", "/weathervane.pl"]
