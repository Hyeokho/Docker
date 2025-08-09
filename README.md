# docker

up
docker-compose -f docker-compose-npm.yml up -d

down
docker-compose -f docker-compose.elastic.yml down -v


# vaultwarden 버전업
docker stop vaultwarden && docker rm vaultwarden && docker rmi vaultwarden/server
sudo docker-compose -f docker-compose-vaultwarden.yml up -d

# npm 버전업
docker stop npm && docker rm npm && docker rmi jc21/nginx-proxy-manager
sudo docker-compose -f docker-compose-npm.yml up -d

# stirling-pdf 
sudo docker-compose -f docker-compose-stirling_pdf.yml up -d
