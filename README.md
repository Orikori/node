docker stop 0a524d1bc940
docker rm 0a524d1bc940

docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q)
docker build -t orikori/node-web-app .
docker run -p 49160:8080 -d orikori/node-web-app

