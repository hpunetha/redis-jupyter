Exploration of redis as a vector database for finding similarities. This is a follow up for https://github.com/hpunetha/weaviate-jupyter where I used weaviate for finding vector similarity.
In this repo, I have configured Redis with similiar use-case, i.e to find similiar images by using vector similiarity search in redis via langchain. The vectors are computed using Resnet18

## Setup Instructions
1. Install [docker](https://docs.docker.com/get-docker/)
2. Run `docker-compose build` and then `docker-compose up` in the root directory or use `docker-compose up -d` (if you want to run the process in background).
3. Open `http://127.0.0.1:8888/lab` on your browser and get the token (or full url with token) from the logs of notebook container by using below commands (if you ran the docker compose up without -d flag then the token will directly be visible in the terminal).    
if you used `-d` flag in the last step then use `sudo docker ps` to list the running containers and get the container id for notebook container and then use  `sudo docker logs <container_id>`, you'll get the url and token at the bottom of logs 
4. To stop the containers use `docker-compose down` in the same directory.

