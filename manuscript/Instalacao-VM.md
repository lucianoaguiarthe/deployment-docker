# Instalação Sistema Operacional Debian
<p align="justify">Para  disponibilizar um ambiente virtualizado se faz necessário o download de um software de virtualizado, o adotado no presente material é o VirtualBox da Oracle, o dowload da aplicação pode ser realizado no endereço abaixo:</p>

[VirtualBox](https://www.virtualbox.org/) 

<p align="justify">O procedimento de instação é muito simples, seguindo as telas de avançar, conforme aplicações padrões do Windows. O Sistema Operacional adotado para execução do Docker é o Debian, em sua versão 10.4, recomenda-se baixar a versão netinst, que possui os pacotes básicos e caso seja necessários realizar o downloads dos demais pacotes através da internet:</p>

[Debian 10.4.0 Netinst](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-10.4.0-amd64-netinst.iso) 

<p align="justify">Para criar uma Máquina Virtual, que é o ambiente onde será instalado o Sistema Operacinal selecione o Menu <b>Máquina</b> e <b>Novo</b>, conforme Figura 1, Atribua um nome para a Máquina Virtual e selecione o botão continuar.<p align="justify">

<p align="center"><img src="images/install-vm/01.png"  width="600" height="303" align="middle"/></p>
<h4 align="middle">Figura 01 - Criação VM</h4>

<p align="justify">Informe também o tamanho da memória que será alocado para a máquina virtual, tenha cuidado deixe uma reserva de 70% da memória para o Sistema Operacional Hospedeiro.</p>

<p align="center"><img src="images/install-vm/02.png"  width="600" height="303" align="middle"/></p>
<h4 align="middle">Figura 02 - Tamanho da Memória</h4>

<p align="justify">Deve ser informado se informado se será criado um novo disco ou utilizaod um existente, em nosso ambiente criaremos um novo disco, conforme Figura 03:</p>

<p align="center"><img src="images/install-vm/03.png"  width="600" height="301" align="middle"/></p>
<h4 align="middle">Figura 03 - Criação de Disco Rígido</h4>

<p align="justify">Informe ainda que tipo de arquivo de disco será criado, deixe marcado a opção default, VDI, conforme Figura 04:</p>

<p align="center"><img src="images/install-vm/04.png"  width="600" height="347" align="middle"/></p>
<h4 align="middle">Figura 04 - Tipo de Arquivo de Disco</h4>

<p align="justify">Selecione se o arquivo de disco será <b>Dinamicamente Alocado</b> ou de <b>Tamanho Fixo</b>, o recomendável é o Dinamicamente Alocado, considerando a economicidade de tamanho.</p>

<p align="center"><img src="images/install-vm/05.png"  width="600" height="346" align="middle"/></p>
<h4 align="middle">Figura 05 - Armazenamento em Disco Rígido Físico</h4>

<p align="justify">Informe a localização do arquivo da VM e o tamanho do disco, o tamanho sugerido de <b>8GB</b>, atende as necessidade do laboratório.</p>

<p align="center"><img src="images/install-vm/06.png"  width="600" height="348" align="middle"/></p>
<h4 align="middle">Figura 06 - Localização e Tamanho do Arquivo</h4>

<p align="justify">Ao concluir a criação da máquina virtual, altere a configuração da rede para que a VM seja acessa externamenete pelos demais dispositivos do ambente. Para isso, acesso o menu <b>Máquina</b> e <b>Configurações</b>, clique no ícone Rede, conforme apontado pela seta vermelha, Figura 07, em <b>Conectado a: - </b> altere para Placa em modo Bridge e clique em <b>ok</b>.</p>

<p align="center"><img src="images/install-vm/07.png"  width="600" height="249" align="middle"/></p>
<h4 align="middle">Figura 07 - Adaptador de Rede</h4>

<p align="justify">Inicialize a Máquina Virtual, clicando no botão iniciar, será aberto uma janela, Figura 08, e aponte para o ISO do Debian que foi realizado o Download no início deste documento.</p>

<p align="center"><img src="images/install-vm/08.png"  width="600" height="326" align="middle"/></p>
<h4 align="middle">Figura 08 - Selecionar Disco Óptico</h4>

<p align="justify">Selecione o tipo de instalador de sua preferência, caso não tenha familiarade, recomendo o instador gráfico do sistema operacional</p>
<p align="center"><img src="images/install-vm/09.png"  width="500" height="374" align="middle"/></p>
<h4 align="middle">Figura 09 - Instalador Debian</h4>

<p align="justify">Escolhe o idiome de sua preferência para o instalador do Sistema Operacional</p>

<p align="center"><img src="images/install-vm/10.png"  width="600" height="448" align="middle"/></p>
<h4 align="middle">Figura 10 - Idioma de Instalação</h4>

<p align="justify">Escolha a localidade de instalação</p>

<p align="center"><img src="images/install-vm/11.png"  width="600" height="449" align="middle"/></p>
<h4 align="middle">Figura 11 - Localidade</h4>

<p align="justify">Selecione o tipo de teclado conforme a configuração do seu dispositivo.</p>

<p align="center"><img src="images/install-vm/12.png"  width="600" height="449" align="middle"/></p>
<h4 align="middle">Figura 12 - Mapa de Teclado</h4>

<p align="justify">Atribua um nome para a máquina, o mesmo será exibido na rede.</p>

<p align="center"><img src="images/install-vm/13.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 13 - Nome da Máquina</h4>

<p align="justify">Caso seja necessário atribua um nome para o domínio, em nosso laboratório não se faz necessário, essa configuração pode ser realizada posteriormente.</p>

<p align="center"><img src="images/install-vm/14.png"  width="600" height="452" align="middle"/></p>
<h4 align="middle">Figura 14 - Nome do Domínio</h4>

<p align="justify">Atribua uma senha para o <b>Root</b>, que é o usuário administrador do Sistema Operacional.</p>

<p align="center"><img src="images/install-vm/15.png"  width="600" height="452" align="middle"/></p>
<h4 align="middle">Figura 15 - Configuração Senha do Root</h4>



<p align="justify">Informe o nome de um usuário que será cadastrado para acesso ao sistema operacional.</p>

<p align="center"><img src="images/install-vm/16.png"  width="600" height="450" align="middle"/></p>
<h4 align="middle">Figura 16 - Usuário Sistema Operacional</h4>

<p align="justify">Atribua uma senha para o usuário criado no passo anterior.</p>

<p align="center"><img src="images/install-vm/17.png"  width="600" height="451" align="middle"/></p>
<h4 align="middle">Figura 17 - Senha Usuário</h4>

<p align="justify">Informe a sua região para configuração do fuso horário do relógio.</p>

<p align="center"><img src="images/install-vm/18.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 18 - Fuso Horário</h4>

<p align="justify">Será inicado o procedimento de maior cuidado na instalação do Sistema Operacional, a recomendação para usuários iniciantes é selecionar a opção <b>Assistido - usar o disco inteiro</b>, no qual uma ferramenta de particionamento irá guiá-lo no procedimemento de formatação e criação de partições.</p>

<p align="center"><img src="images/install-vm/19.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 19 - Método de Particionamento</h4>

<p align="justify">Selecione o disco que será realizado o particionamento.</p>

<p align="center"><img src="images/install-vm/20.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 20 - Disco a Ser Apagado</h4>

<p align="justify">O Particionador de disco realiza a divisão do disco conforme necessidade do administrador do sistema operacional, a maneira correta de configuração de um servidor é criar uma partição para cada pasta, como por exemplo: uma partição para a /home, outra para a /var, outra  /tmp. Todavia como é a instação de um Sistema Operacional de teste, iremos selecionar a opção <b>Todos os arquivos em uma partição</b>, Figura 21:</p>

<p align="center"><img src="images/install-vm/21.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 21 - Particionador de Disco</h4>

<p align="justify">Para concluir os procedimentos de particionamentos selecione a opção <b>Finalizar o particionamento e escrever as mudanças no disco</b>, Figura 22:</p>

<p align="center"><img src="images/install-vm/22.png"  width="600" height="452" align="middle"/></p>
<h4 align="middle">Figura 22 - Confirmação de Particionamento</h4>

<p align="justify">Escreva as mudanças no disco referente a particionamentos marcanco a opção <b>Sim</b> e clicando no botão <b>Continuar</b>.</p>

<p align="center"><img src="images/install-vm/23.png"  width="600" height="451" align="middle"/></p>
<h4 align="middle">Figura 23 - Escrever Mudanças no Disco</h4>

<p align="justify">Caso tenha mais algum outro CD ou DVD de instação selecione sim e aponte para o dispositivo, para o nosso processo de instação temos somente uma imagem ISO portanto selecione a opção <b>Não</b> e clique em continuar.</p>

<p align="center"><img src="images/install-vm/24.png"  width="600" height="454" align="middle"/></p>
<h4 align="middle">Figura 24 - Ler Discos</h4>

<p align="justify">Informe qual o país do Espelho que será utilizado para download dos pacotes, Figura 25:</p>

<p align="center"><img src="images/install-vm/25.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 25 - Repositório Debian</h4>

<p align="justify">Informe qual espelho será utilizado para download dos pacotes.</p>

<p align="center"><img src="images/install-vm/26.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 26 - Espelho do Repositório</h4>


<p align="justify">Caso esteja em uma rede corporativa, informe qual o endereço do proxy e a porta, em nosso ambiente virtualizado não se faz necessário.</p>

<p align="center"><img src="images/install-vm/27.png"  width="600" height="456" align="middle"/></p>
<h4 align="middle">Figura 27 - Proxy de Rede</h4>

<p align="justify">Informe se tem interesse de participar do concurso de Gerenciador de Pacotes.</p>

<p align="center"><img src="images/install-vm/28.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 28 - Concurso de Realização de Pacotes</h4>

<p align="justify">Selecione os sofware que serão utilizados no sistema operacional, em nosso ambiente marque somente <b>servidor ssh</b>.</p>

<p align="center"><img src="images/install-vm/29.png"  width="600" height="452" align="middle"/></p>
<h4 align="middle">Figura 29 - Seleção de Software</h4>

<p align="justify">O <b>Grub</b> é o carregador de inicalização do Sistema Operacional, obrigatoriamente deve ser instalado para que o Sistema inicialize normalmente, marque a opção <b>Sim</b> e clique em continuar.</p>

<p align="center"><img src="images/install-vm/30.png"  width="600" height="451" align="middle"/></p>
<h4 align="middle">Figura 30 - Instalação do Grub</h4>

<p align="justify">Selecione o disco que será instalado o Grub, Figura 31:</p>

<p align="center"><img src="images/install-vm/31.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 31 - Dispositivo de Instalação do Grub</h4>

<p align="justify">Finalmente a instalação é concluída, clique no botão <b>Continuar</b> e reinicie o Sistema Operacional.</p>

<p align="center"><img src="images/install-vm/32.png"  width="600" height="453" align="middle"/></p>
<h4 align="middle">Figura 32 - Conclusão da Instalação</h4>

[Início](/README.md)