# Instalação Docker
<p align="justify">Os containers são baseados em uma técnica de virtualização em nível de sistema operacional que fornece ambientes virtuais utilizando Linux Containers (LCX), facultando o isolamento do processo e da rede por meio de chroot, cgroups e namespaces.</p>

<p align="justify">A abordagem de container pode acarretar dúvidas quando comparados com máquinas virtuais (MV). Considerando a semelhança entre os modelos, será apresentado um comparativo em relação ao uso de container e máquinas virtuais.</p>

<p align="justify">A Virtualização é o processo de dividir a máquina física em vários componentes virtuais, nos quais cada um pode hospedar sistemas operacionais diferentes, cabendo a gestão destes SO ao hypervisor. A Figura 4 apresenta um ambiente com esta arquitetura. Um aspecto a se ressaltar é o consumo de hardware: cada sistema convidado possui um kernel em execução.</p>

<p align="center"><img src="images/install-docker/VM.png"  width="250" height="351" align="middle"/></p>
<h4 align="middle">Figura 01 - Máquina Virtual</h4>



<p align="justify">Na arquitetura de container, bibliotecas, system calls e recursos do SO hospedeiro são compartilhados com os containers. Neste ambiente, cada container compartilha ainda o mesmo kernel do SO hospedeiro, tornando a sua execução mais rápida. A Figura 5 apresenta um ambiente com esta abordagem executando dois containers.</p>

<p align="center"><img src="images/install-docker/container.png"  width="250" height="325" align="middle"/></p>
<h4 align="middle">Figura 02 - Container</h4>

<p align="justify">Funcionalmente, cada componente destacado a seguir proporciona uma estrutura para a execução do SO no container:</p>

*	chroot – disponibiliza um diretório-raiz;
*	cgroups – fornecem mecanismos para contabilizar e limitar os recursos que os processos podem utilizar em cada container (BUI, 2015);
*	namespaces – criam grupos de processos de maneira que um grupo de processo não seja visualizado por outro, garantindo o isolamento dos containers. 

<p align="justify">Existem disponíveis várias ferramentas de gestão de container, como o Docker, o CoreOS, o Mesos e o LXC. O presente estudo concentra-se somente no Docker, considerada a ferramenta mais usada para este propósito.</p>

<p align="justify">No Docker, cada container é baseado em uma imagem e em um conjunto de dados de configuração. As imagens são cópias estáticas da configuração dos containers. Todas as imagens de um container ficam hospedadas em um servidor remoto, chamado Docker Hub, no qual o usuário pode fazer seu cadastro e disponibilizar sua imagem personalizada.</p>


<p align="justify">Para compreender como ocorre a gestão dos containers com Docker, se faz necessário conhecer a arquitetura deste ambiente, apresentada na Figura 03. A interação com o ambiente é realizada por meio do Docker Client, a partir do qual é possível realizar o download de imagens, criação de container, entre outros.</p> 

<p align="justify">O componente responsável para atender as requisições do Docker Client é o Docker Daemon, atendendo as solicitações da API do Docker (do inglês Application Programming Interface - Interface de Programação de Aplicações) e gerenciando objetos, como imagens, containers, redes e volumes. O download das imagens dos containers e as suas publicações é feito a partir de um repositório de registros de imagens, o Docker Registry. A loja oficial do Docker é o Docker Hub. Todavia, existem outros ambientes para armazenamento de imagens, como o Amazon Elastic Container da AWS e o Google Cloud Platform e a Azure, que usam a nomenclatura padrão para o serviço, chamando de Docker Registry.</p>




<p align="center"><img src="images/install-docker/architecture.png"  width="700" height="366" align="middle"/></p>
<h4 align="middle">Figura 03 - Arquitetura Docker (Fonte: https://docs.docker.com/)</h4>



## INSTALAÇÃO DO DOCKER

<p align="justify">Atualize o índice do pacote apt e instale pacotes para permitir que o apt use um repositório através de HTTPS:</P>

<p align="left">
<b>apt-get install -y
    apt-transport-https 
    ca-certificates 
    curl 
    gnupg-agent 
    software-properties-common</b>
</p>

<p align="justify">Adicione a chave GPG oficial do Docker:</P>

<p align="left"><b>curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add - </b></p>

<p align="left">Verifique se agora você possui a chave com a impressão digital <b>9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88</b>, pesquisando os últimos 8 caracteres da impressão digital:</P>

<p align="left"><b>apt-key fingerprint 0EBFCD88</b></p>


<p align="justify">Adicione o repositório estável para instalação dos pacotes docker do debian:</p>
<p align="left"><b>add-apt-repository 
   "deb [arch=amd64] https://download.docker.com/linux/debian 
   $(lsb_release -cs) 
   stable"</b></p>

<p align="justify">Atuelize os pacotes do Sistema Operacional:</p>   
<p align="left"><b> apt-get update</b></p>
   
<p align="justify">Instale os pacotes necessários para execução docker:</p>
<p align="left"><b>apt-get install -y docker-ce docker-ce-cli containerd.io </b></p>



<p align="justify">Para verificar a versão do docker digite: docker -v</p>

<p align="center"><img src="images/install-docker/version-docker.png"  width="400" height="31" align="middle"/></p>
<h4 align="middle">Figura 04 - Versão Docker</h4>


[Início](/README.md)
