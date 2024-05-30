# Criando 

## Tamanho com os dois pacotes 470Mb
docker build -t infer_py312_slim:1.0 .

## Tamanho com os dois pacotes 498mb
docker build -t infer_py311_slim:1.0 .

## Tamanho com os dois pacotes 488MB
docker build -t infer_py390_slim:1.0 .

## Tamanho com os dois pacotes 447MB
docker build -t infer_py3819_slim:1.0 .

# Executando 
docker run -it infer_py312_slim:1.0 /bin/bash

docker run -it infer_py311_slim:1.0 /bin/bash

docker run -it infer_py390_slim:1.0 /bin/bash