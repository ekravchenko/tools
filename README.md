"# tools" 

git clone https://github.com/ekravchenko/tools.git

docker build -t myjenkins .

docker volume create --name jenkins

docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v jenkins:/var/jenkins_home myjenkins

docker exec -it jenkins /bin/bash

docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)