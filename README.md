# Protegendo um Servidor na Oracle Cloud

# Pré-req para o ambiente

* Cria uma conta no Oracle Cloud (free)
https://cloud.oracle.com

* Cria uma conta no Cloud One (free)
https://cloudone.trendmicro.com/

# Provisionando uma VM (Oracle Cloud)

Navegue no menu direito até Compute > Instances também é possível usar a visualização no meu principal como o exemplo abaixo:

<img src="OCIvm.jpg" alt="ADD Azure" width="75%"> </img>

Defina um nome para seu workload, faça o download das chaves privadas para uma conexão futura via ssh.

<img src="OCIvm2.jpg" alt="ADD Azure" width="75%"> </img>

Clique em show advanted options, iremos colocar um script na inicialização do servidor dessa forma realizando a instalação do agente do Cloud One Workload Security.

<img src="OCIadv.jpg" alt="ADD Azure" width="75%"> </img>

Acessar a plataforma Cloud One (a conta deve ser criada previamente) e escolher a opção Workload Security

<img src="WS.jpg" alt="ADD Azure" width="75%"> </img>

No meu Support selecione a opção Deployment Scripts, selecione a Plataforma "Linux Agent Deployment" e clique em "Copy to Clipboard", iremos copiar o script de instalação e colocar na inicialização do Servidor.

<img src="script.jpg" alt="ADD Azure" width="75%"> </img>

Novamente na console do OCI, selecione a opção "Paste cloud-init script" e cole o script gerado a partir da console do Cloud One. Após isso selecione create e aguarde alguns minutos até a inicialização do Servidor.

<img src="OCIscript.jpg" alt="ADD Azure" width="75%"> </img>

<img src="OCIinstance.jpg" alt="ADD Azure" width="75%"> </img>

Enquanto o Servidor é inicilizado iremos criar uma Smart Folder para Organizarmos nosso ambiente. Acesse novamente a console do Cloud One e navegue no meu conforme abaixo no menu Computers > Smart Folde > Create Smart Folder.

<img src="SmartFolder.jpg" alt="ADD Azure" width="75%"> </img>

Com o Servidor já inicializado é possível visualizarmos no Cloud One, nesse exemplo tenho dois Servidores um on-premise e outro criado anteriormente.

<img src="WSprotegido.jpg" alt="ADD Azure" width="75%"> </img>

Para finalizar, aplique uma politica no Servidor, clique com o botão direito "Actions" e "Assign Policy"

<img src="policies.jpg" alt="ADD Azure" width="75%"> </img>
