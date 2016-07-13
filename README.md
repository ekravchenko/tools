"# tools" 

??? Add command on how to create docker volume

docker build -t myjenkins .

docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v jenkins:/var/jenkins_home myjenkins

docker exec -it jenkins /bin/bash