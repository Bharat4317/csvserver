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

Input-File-
0, 4
1, 63
2, 90
3, 23
4, 80
5, 33
6, 83
7, 51
8, 89
9, 7
10, 7

Part-1-logs
2022/04/02 14:20:00 listening on ****
2022/04/02 14:58:47 wrote 150 bytes for /raw
2022/04/02 15:02:18 wrote 150 bytes for /ra

Part-1-logs
Y3N2c2VydmVyIGdlbmVyYXRlZCBhdDogMTY0ODkwOTIwMA==
CSVSERVER_BORDER: Orange
0,  4
1,  63
2,  90
3,  23
4,  80
5,  33
6,  83
7,  51
8,  89
9,  7
10,  73


