https://www.python.org/ftp/python/



https://www.python.org/ftp/python/3.9.5/


https://www.python.org/ftp/python/3.10.1/


https://www.python.org/ftp/python/3.11.1/


https://www.python.org/ftp/python/3.12.1/


https://codereview.stackexchange.com/questions/286556/install-specific-version-of-python-in-docker


## Commands
docker volume ls


docker stop $(docker ps -aq)
docker container rm -f $(docker container ls -aq)
docker volume rm -f $(docker volume ls -q)

docker stop $(docker ps -aq)

docker container rm -f $(docker container ls -aq)

docker volume rm -f $(docker volume ls -q)


To delete all images

docker rmi $(docker images -a)


To delete containers which are in exited state

docker rm $(docker ps -a -f status=exited -q)


To delete containers which are in created state

docker rm $(docker ps -a -f status=created -q)




List all images 
docker images -a | awk {'print $3'}


To delete all images:

docker rmi -f $(docker images -a | awk {'print $3'})


List all images with created 

docker images --format 'table {{.Repository}}\t{{.Tag}}\t{{.ID}}\t{{.CreatedAt}}\t{{.Size}}'


Deletando com filtro 
docker rmi -f $(docker images -af <YOUR_FILTER_PATTERN> -q)



docker build -t py390_slim .

docker build -t py311_slim .


docker build -t py312_slim .


Limpeza de cache de imagens antigas

docker builder prune


Verificando sistema 
docker system df
