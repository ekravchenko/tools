FROM jenkinsci/jenkins
USER root
RUN apt-get update \
	&& apt-get install -y maven \
	&& apt-get install -y npm
USER jenkins