Solution - Part 1
docker pull infracloudio/csvserver:latest
docker pull prom/prometheus:v2.22.0

git clone https://github.com/infracloudio/csvserver.git

docker images

docker run -d -i infracloudio/csvserver:latest

docker ps -a

docker logs 810615e13c95

#!/bin/bash
count=0
while [ $count -lt 11 ];
do
rand=$((RANDOM%100))
echo "$count, $rand" >> inputFile
count=$(($count+1))
done


docker run -d -i -v /root/csvserver/solution/inputFile:/csvserver/inputdata infracloudio/csvserver:latest

docker run -d -i -v /root/csvserver/solution/inputFile:/csvserver/inputdata infracloudio/csvserver:latest

docker exec -it 8f6814b266ad bash

netstat -tulnp

docker stop 8f6814b266ad 

docker run -d -i -v /root/csvserver/solution/inputFile:/csvserver/inputdata -p 9393:9300 infracloudio/csvserver:latest

docker stop 4c88938b4b00

docker run -d -i -v /root/csvserver/solution/inputFile:/csvserver/inputdata -p 9393:9300 -e CSVSERVER_BORDER='Orange' infracloudio/csvserver:latest
