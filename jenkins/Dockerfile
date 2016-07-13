FROM jenkinsci/jenkins
USER root
RUN apt-get update && apt-get install -y maven
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash - && apt-get install -y nodejs
USER jenkins