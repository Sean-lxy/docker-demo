```
docker build -t node-app-image .


docker run -p 3000:3000 -v $(pwd):/app -d --name node-app node-app-image

docker run -p 3000:3000 -v $(pwd):/app -v /app/node_modules -d --name node-app node-app-image

docker run -p 3000:3000 -v $(pwd):/app:ro -v /app/node_modules -d --name node-app node-app-image

docker exec -it node-app bash

docker rm node-app -f

docker-compose up

docker-compose up -d --build

docker-compose down -v
```