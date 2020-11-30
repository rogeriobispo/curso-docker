docker container run <image> -> executa uma image.
docker container run <image> <commando> -> comando será executado dentro da maquina.
docker container ls -> lista containers ativos.
docker container ps -> lista containers ativos.
docker container (ps/ls) -a -> lista todos containers ativos e inativos.
docker container run --rm debian -> executa o container depois remove.
docker container run -it <image> bash -> modo iterativo acessa o terminal do container
docker exec -it <image>./bin/bash -> acessa o terminal bash do container.
docker container run --help -> exibe ajuda para o comando.
docker contianer run --name <nomedocontainer> -it debian bash -> cria container com o nome debia e acessa o bash
docker container start -ai <container> -> executa o container e acessa o terminal.
docker container run -p <portexterna>:<portinterna> nginx -> exporta a porta do container para fora do container.
docker container run -v <postahost>:<pastacontainer> -> vincula uma pasta do hosta com uma pasta do container.
docker container run -d nginx -> executa o container em background.
docker container stop <nomedocontainer>
docker container start <nomedocontainer>
docker container restart <nomedocontainer>
docker container logs <container > -> exibe os logs do container.
docker container inspect <container> -> mostra os detalhes do container.
docker container exec <container> <comando> -> executa um comando no container.
docker container ls -> lista container
docker image ls -> lista imagens
docker volumes ls -> lista os volumes
docker image rm <image> -> remove a imagem
docker container rm <container> -> remove o container
docker container --help -> lista ajuda do container
docker image --help -> ajuda da image
docker volume --help -> ajuda do volume
docker image tag <image> <tag> -> adiciona uma tag a imagme.
docker image pull <image> -> baixa a imagem.
docker image build -> cria uma imagem através de um arquivo Dockerfile
docker image push -> envia a imagem para o registry.
docker image build --build-arg <variavel e ambiente> -t <tag> -> faz o build com uma variavel de ambiente.
docker tag <imagem> <novatagparaimage> -> cria uma nova tag para a imagem especificada

redes docker 

none -> não tem rede. 
bridge -> padrão uma camada entre o docker e o host
host -> mesma rede do host.
overlay -> swarm

docker container run -d --net (none, bridge, host) debian -> cria um container debian com uma rede
docker network create --drive bridge rede_nova -> cria uma nova rede no docker.
docker network connect bridge container3 -> conecta uma rede especificada ao container.
docker network disconnect bridge container3 -> conecta uma rede especificada ao container.
