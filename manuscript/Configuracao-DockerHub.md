# Configuração Docker Hub
<p align="justify">O Docker Hub (https://hub.docker.com/) é um repositório remoto de imagem de container docker, possui uma grande quantidade de imagens, Figura 01, pré-configuradas facilitando a vida dos desenvolvedores.</p>

<p align="center"><img src="images/docker-hub/docker-hub.png"  width="800" height="389" align="middle"/></p>
<h4 align="middle">Figura 01 - Docker Hub</h4>

<p align="justify">Existe ainda a possibilidade da criação de um cadastro e hospedagem de imagens personalizadas, caso queira disponibilizar uma aplicação para testes, ou até mesmo criar um ambiente de produção, o Docker Hub possui 03 planos de assinatura, Figura 02:</p>


<p align="center"><img src="images/docker-hub/plano-dockerhub.png"  width="600" height="271" align="middle"/></p>
<h4 align="middle">Figura 02 - Planos Docker Hub</h4>

<p align="justify">Para criação de um repositório remoto público crie uma conta de usuário e logue no Docker Hub, será exibo um Dashboard com todos os repositórios de imagens da conta, Figura 03, é importante pontuar que o nome do repositório deve ser o mesmo do nome da imagem, para criar um repositório clique no botão <b>Create Repository</b>.</p>

<p align="center"><img src="images/docker-hub/01-acess-dockerhub.png"  width="800" height="156" align="middle"/></p>
<h4 align="middle">Figura 03 - Docker Hub</h4>
 
 
 <p align="justify">Atribua um nome ao repositório que será criado, ratificando que o nome do repositório é o mesmo da imagem que será enviada.</p>
 
<p align="center"><img src="images/docker-hub/02-create-repository.png"  width="800" height="331" align="middle"/></p>
<h4 align="middle">Figura 04 - Criação de Repositório</h4>

 <p align="justify">Ao concluir a criação do repositório será exibido o status inclusive com o comando para envio da imagem, Figura 05.</p>
 
<p align="center"><img src="images/docker-hub/03-view-repository.png"  width="800" height="430" align="middle"/></p>
<h4 align="middle">Figura 05 - Status do Repositório</h4>

<p align="justify">O Docker por padrão não vem configurado enviar imagens ao Docker Hub, necessitando configurar o usuário e senha, para isso utize o comando <b>docker login</b> e informe os dados da conta.<p>

<p align="center"><img src="images/docker-hub/04 - config-docker-login.png"  width="800" height="147" align="middle"/></p>
<h4 align="middle">Figura 06 - Configuração Login Docker</h4>

<p align="justify">É necessário agora criar a imagem  a ser enviada para o repositório com o mesmo nome do criado no Docker Hub, conforme comando abaixo:</p>

<p align="justify"><b>docker commit icev icev-luciano </b></p>

<p align="justify">Devemos ainda riar uma referência (tag) da imagem no repositório, informando se é a última versão, ou se é específica de alguma aplicação, etc. Para isso precisamos saber o ID da imagem, através do comando <b>docker images</b>.</p>

<p align="center"><img src="images/docker-hub/id-img.png"  width="600" height="74" align="middle"/></p>

<p align="justify">Atribua a marcação latest a imagem, <b>IMPORTANTE</b>, este número ID é específico  para a imagem de exemplo, deve ser alterado para cada sistema operacional</p>

<p align="left"><b>docker tag <b>5063e5317297</b> lucianoaguiarthe/icev-luciano:latest</b></p>

<p align="justify">Por último envie a sua imagem para o repositório com o comando <b>docker push</b>.</p>
<p align="center"><img src="images/docker-hub/push-img.png"  width="700" height="60" align="middle"/></p>

<p align="justify">Acesse o Docker Hub e verifique se a sua imagem está disponível, desta forma já é possível que todos na internet façam o download da sua aplicação através do comando <b>docker pull</b>.</p>
<p align="center"><img src="images/docker-hub/repository-img.png"  width="800" height="259" align="middle"/></p>
<h4 align="middle">Figura 06 - Repositório com a Imagem</h4>

[Início](/README.md)