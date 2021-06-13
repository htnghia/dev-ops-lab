## from self registry
docker rm jenkins && docker run -p 9001:8080 -v /home/nghia/docker_volumes/jenkins_home:/var/jenkins_home --name jenkins nghiahuynh/lib:jenkins_master

-> not work --env JAVA_OPTS="-Xmx1048m"

## build image
Run Jenkins:

docker run -p 9001:8080 -v /home/nghia/docker_volumes/jenkins_home:/var/jenkins_home --name jenkins jenkins/jenkins:lts-jdk11 --env ="-Xmx1048m"