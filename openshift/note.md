
## login umb oc
oc login -u nghia.huynh https://master.openshift.ubitec.local:8443

## get aws docker login
oc create secret docker-registry nghia-s --docker-server=docker.ubitec.io --docker-username=AWS --docker-password=dddddd --docker-email=nghia.huynh@umb.ch

## create pullSecret in openshift base on docker

oc create secret generic awsumpsecret --from-file=.dockerconfigjson=/home/nghia/.docker/config.json --type=kubernetes.io/dockerconfigjson