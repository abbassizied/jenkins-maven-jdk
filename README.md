# jenkins-maven-jdk 


```sh
echo "# jenkins-maven-jdk" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/abbassizied/jenkins-maven-jdk.git
git push -u origin main
```

## Top Plugins to Add on Jenkins

- [Rebuilder Plugin](https://plugins.jenkins.io/rebuild/)
- [Role-based Authorization Strategy](https://plugins.jenkins.io/role-strategy/)
- [Green Balls](https://plugins.jenkins.io/greenballs/)
- [Mailer](https://plugins.jenkins.io/mailer/)
- [Docker plugin for Jenkins](https://plugins.jenkins.io/docker-plugin/)
- [Git plugin](https://plugins.jenkins.io/git/)
- [Amazon EC2 plugin](https://plugins.jenkins.io/ec2/)
- [Credentials Binding plugin](https://www.jenkins.io/doc/pipeline/steps/credentials-binding/)


## 

```sh
# Create a bridge network in Docker
$ docker network create jenkins

# Build a new docker image from this Dockerfile and assign the image a meaningful name, e.g. "myjenkins:2.452.1-1":
 $ docker build -t myjenkins:2.452.1-1 .
 # Publish Docker container to Docker Hub
 $ docker tag myjenkins:2.452.1-1  ziedab/myjenkins:2.452.1-1
 $ docker push  ziedab/myjenkins:2.452.1-1 

# Run your own myjenkins:2.452.1-1 image as a container in Docker using the following docker run command:
docker run --name jenkins --restart=on-failure --detach ^
  --network jenkins --env DOCKER_HOST=tcp://docker:2376 ^
  --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 ^
  --volume jenkins-data:/var/jenkins_home ^
  --volume jenkins-docker-certs:/certs/client:ro ^
  --publish 8080:8080 --publish 50000:50000 myjenkins:2.452.1-1
```