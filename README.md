"# tools" 

git clone https://github.com/ekravchenko/tools.git

docker build -t myjenkins .

docker volume create --name jenkins

docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v jenkins:/var/jenkins_home myjenkins

docker exec -it jenkins /bin/bash

docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)




 docker run -d --name postgres -v postgres:/var/lib/postgresql -e POSTGRES_PASSWORD=sonar -e POSTGRES_USER=sonar -e POSTGRES_DB=sonar  postgres


docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 -e SONARQUBE_JDBC_USERNAME=sonar -e SONARQUBE_JDBC_PASSWORD=sonar -e SONARQUBE_JDBC_URL=jdbc:postgresql://postgres/sonar --link postgres:postgres sonarqube