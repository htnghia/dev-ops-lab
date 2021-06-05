## from self registry
docker run -p 9001:8080 -v /Users/nghiahuynh/projects/docker_volumes/jenkins_home:/var/jenkins_home --name jenkins nghiahuynh/lib:jenkins_master --env ="-Xmx1048m"

## build image
Run Jenkins:

docker run -p 9001:8080 -v /Users/nghiahuynh/projects/docker_volumes/jenkins_home:/var/jenkins_home --name jenkins jenkins/jenkins:lts-jdk11 --env ="-Xmx1048m"