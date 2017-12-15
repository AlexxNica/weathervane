FROM namespace/weathervane-centos7:version
MAINTAINER hrosenbe@vmware.com

COPY entrypoint.sh /entrypoint.sh
COPY weathervane.pl /weathervane.pl
COPY runHarness /runHarness
	
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
