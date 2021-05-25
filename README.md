# nginx-nexus-docker
## Code in this repository represents Nexus3 with Nginx reverse-proxy using SSL/TLS and docker.
What we will achieve here?
1. Nexus3 repository. 
2. Nginx Reverse-Proxy to Nexus3 repo.
3. SSL/TLS certs(root and nexus) generated and implemented.
4. Docker proxy registry w/ Nexus3.
5. Docker hosted registry w/ Nexus3.


Installation Guide
=================

Pre-requisite
-------------
Docker
Docker-copose
Openssl

apt-get install docker
apt-get install openssl
apt-get install ca-certificates

curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
docker-compose --version

git clone -b ubuntu https://github.com/rokon-gt/nginx-nexus-docker.git
cd nginx-nexus-docker/
rm -rf certs

cd scripts/
sh nexus-nginxproxy.sh "password"

docker ps

Then create docker-proxy and docker-hosted
Follow this link
https://www.youtube.com/watch?v=PRJz61Jm6Ec






