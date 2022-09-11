# Atividade-Linux-Oracle-Compaas

## Pré requisitos

- Ter baixado na máquina o Oracle VM VirtualBox
- Ter baixado a imagem ISO

## Instalação do Linux Oracle
- Utilize a versão realease 8.6, Full ISO do Oracle Linux (Minimal).
- Escolha o Sistema Operacional sem Interface Gráfica.
- Configure no indioma inglês.

## Criação da VM

- O primeiro passo é com a VM instalada na máquina, abra na tela inicial para configurar o **nome e sistema operacional** e selecione a opção "Novo" para a criação da primeira VM, logo após, dê um nome e observe a pasta onde ficará os arquivos, selecionar o Tipo e escolher a opção "Linux" e selecionar a versão "Oracle-64bit".
- O segundo passo é configurar o **Tamanho da memória RAM em megabytes** escolher a opção padrão 1024 MB.
- O terceiro passo é acrescentar um **disco rígido** e selecionar a opção "Criar um novo disco rígido virtual agora".
- O quarto passo é escolher o **tipo de arquivo de disco rígido** e selecionar a opção VHD (Virtual Hard Disk).
- O quinto passo é escolher se o arquivo contendo o disco rígido virtual deve crescer à medida em que é urilizado ou se ele deve ser criado já com o tamanho máximo, selecionar a opção "Dinamixamente alocado".
- O sexto passo é o **tamanho do arquivo**, insira o tamanho da imagem de disco virtual e disponhe de 50,00 GB.

### Ajustes finais da VM ###

Depois da VM pronta é preciso mudar algumas configurações padronizadas nela, sendo elas:
- Abrir configurações>armazenamento>controladora: IDE e adicionar  a imagem ISO.
- Abrir configurações>rede e escolher a opção "Modo Bridge".

## Iniciação da VM ##

Após a VM já instalada e com suas primeiras configurações já realizadas, é preciso seguir os seguintes passos para se obter sucesso na sua iniciação, sendo eles:
- Selecionar a Linguagem desejada, manter a opção "english".
- Na aba *Software Selection* selecionar a opção "Minimal Install".
- Na aba *Network e Host*  ligar a *ethernet* para se obter conexão.
- Na aba *Installation Destination* selecionar o disco.
- Na aba *Root Password* escolher uma senha para o root.

Após todos esses passos seguidos selecionar a opção "Beggin Installation"

## Relação de confiança ##

É importante seguir essas etapas para ser possível alcançar uma relação de confiança entre duas VMs utilizando o SSH.

- Foi criada uma VM principal (Server) e outra secundária com as mesmas configurações citadas acima (Cliente).

### Instalação SSH ###

Usar o comando 'yum install openssh-server' para instalar o servidor SSH

