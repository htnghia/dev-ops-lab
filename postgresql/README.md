# use image from registry
docker run -d --name udb -v /home/nghia/docker_volumes/udb/postgresql:/etc/postgresql -v /home/nghia/docker_volumes/udb/log/postgresql:/var/log/postgresql -v /home/nghia/docker_volumes/udb/lib/postgresql:/var/lib/postgresql -v /home/nghia/docker_volumes/udb/postgresql/data:/var/lib/postgresql/data -p 5432:5432 nghiahuynh/lib:udb
  
  
# build image from crash
  docker rmi udb

  docker build -t udb .

  

## open ubuntu console

docker stop udb && docker rm udb && docker run -d --name udb -v /home/nghia/docker_volumes/udb/postgresql:/etc/postgresql -v /home/nghia/docker_volumes/udb/log/postgresql:/var/log/postgresql -v /home/nghia/docker_volumes/udb/lib/postgresql:/var/lib/postgresql -p 5432:5432 udb

## back to windows console
  docker cp udata.sql udb:. && docker exec -it udb bash

## insinde container
  psql -U postgres -f udata.sql


  