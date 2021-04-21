docker run -d \
  -p 9084:1521 \
  -p 9085:5500 \
  --name=oracle-xe \
  --volume ~/docker_volumes/oracle18:/opt/oracle/oradata \
  quillbuilduser/oracle-18-xe