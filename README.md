# Configuração de Servidor com Windows Server

## 1.	Criando a VM pelo VirtualBox

1.1.	Selecionar a ISO do Windows Server 2025.

1.2.	Marcar a opção `Pular Instalação Desassistida`. 

![image](https://github.com/user-attachments/assets/fc5920f7-3fa1-44e7-961c-afa097ddfe70)


1.3.	Configurações de Hardware:

  -	Memória Base: 5 GB (5120 MB)
  -	Processadores: 2 CPUs

![image](https://github.com/user-attachments/assets/e9de14d9-4acc-4304-85e9-e9cb5d1a0fce)


1.4.	Criar um disco virtual com `50 GB` de armazenamento

1.5.	Finalizar

![image](https://github.com/user-attachments/assets/d6c522b6-be49-4722-ba04-4f0f6eb0d406)

1.6.	No menu do VirtualBox, acessar `Configurações`

1.7.	Em `Rede`, selecionar a opção para conectar na `Rede Interna`

![image](https://github.com/user-attachments/assets/4bc56478-8322-44fc-98cf-d647d9b521cc)

1.8.	Iniciar a VM

![image](https://github.com/user-attachments/assets/38f21ab0-adaf-4c26-a82a-7b06324bbc4a)
 
## 2.	Instalação do Windows Server 2025

2.1.	Configurações iniciais (Idioma e teclado)

![image](https://github.com/user-attachments/assets/316a86a1-fb06-4f43-a3e1-98614f3e3f30)
![image](https://github.com/user-attachments/assets/bc2d7bb3-7b84-40e9-80e5-1e61f968cdd2) 
![image](https://github.com/user-attachments/assets/502ff2a7-e09d-42af-9632-126102bf2721)


2.2.	Selecionar a imagem do `Datacenter Evaluation (Desktop Experience)`

![image](https://github.com/user-attachments/assets/db86afeb-1165-45a5-b66b-9dd92d2fcb4c)
![image](https://github.com/user-attachments/assets/11e14095-22dc-4e14-b4cb-177530a7f8cd)
 
2.3.	Iniciar a instalação

2.4.	Se a tela ficar preta, desligar a VM e ligar novamente

![image](https://github.com/user-attachments/assets/288c7154-8c7f-4e2f-930c-52275edd79d0)

2.5.	Inserir uma senha para o usuário Administrator

![image](https://github.com/user-attachments/assets/194d3fcc-3a68-49fa-8c1b-d68c42bb1324)
 
2.6.	Desbloquear a tela: `Entrada -> Teclado -> Inserir Ctrl+Alt+Del`

![image](https://github.com/user-attachments/assets/0d3f2aec-437f-4e6a-98bd-cc912f2de7b5)

## 3.	Desativar o Firewall

3.1.	Acessar o `Painel de Controle -> Windows Defender Firewall`

![image](https://github.com/user-attachments/assets/83c14c4c-01f8-42e1-885a-b6a9d1fbd3db)

3.2.	Selecionar a opção `Turn Windows Defender Firewall on or off`

![image](https://github.com/user-attachments/assets/ace225d2-f226-45da-89f5-c0aa46774a28)
![image](https://github.com/user-attachments/assets/5f595298-8abb-4f7b-b80e-46d9629cd04e)
![image](https://github.com/user-attachments/assets/51def33b-725d-466b-b0e3-d8fd6469cad1)

## 4.	Alterar o Nome da Máquina

4.1.	Acessar o `Windows Explorer`

4.2.	Clicar com o botão direito em `This PC` e selecionar `Properties`

![image](https://github.com/user-attachments/assets/b4adef75-7db9-48e9-be82-82d05d49c5c8)
 
4.3.	Selecionar `Rename this PC`

4.4.	Renomear e reiniciar a vm

![image](https://github.com/user-attachments/assets/b8929cdd-0bd0-47ff-962f-1603d6d1d97f)
![image](https://github.com/user-attachments/assets/73bc725e-e495-4c7f-a6ae-084c2005ef47)

## 5.	Definir o IP Fixo
5.1.	Clicar em `Win+R` e usar o comando `ncpa.cpl`

![image](https://github.com/user-attachments/assets/4d5085d8-6b37-4c0f-a12c-57ed54aceb60)

5.2.	Clicar com o botão direito na placa de rede e selecionar `Properties`

![image](https://github.com/user-attachments/assets/ee860d96-d197-4eff-b082-bd1a1ddb0cc7)

5.3.	Duplo clique em `Internet Protocol Version 4 (TCP/IPv4)`

![image](https://github.com/user-attachments/assets/6beae602-9fe4-4003-98e8-05e0f29f8436)

## 6.	Server Manager

6.1.	Abrir `Server Manager` para instalação dos serviços

6.2.	Clique em `Add roles and features`

![image](https://github.com/user-attachments/assets/cd647cb8-fe79-48b8-ab88-546a6104fa7f)
 
6.3.	Clique em `Next` até chegar na tela de seleção dos serviços

![image](https://github.com/user-attachments/assets/6365cc8f-bd08-4f42-85d0-d0453d09ebaa)
![image](https://github.com/user-attachments/assets/807f88c3-88e1-414c-a352-d9e8077867b6)
![image](https://github.com/user-attachments/assets/c36f8e44-97b4-4abd-a885-e9e5e85683dd)

6.4.	Selecionar os serviços:
  - `Active Directory Domain Services -> Add Features`
  -	`DHCP Server -> Add Features`
  - `DNS Server -> Add Features`
  - `Next`

![image](https://github.com/user-attachments/assets/c617e586-b188-4eed-a585-7ba36863c000)

6.5.	Clicar em `Next` até a tela de confirmação de instalação
 
![image](https://github.com/user-attachments/assets/91ddb4b6-3913-44a5-97d0-7ba9a06f21c2)
![image](https://github.com/user-attachments/assets/0a8260b8-a534-4f50-b753-25578a46e3ad)
![image](https://github.com/user-attachments/assets/c62d4210-5a36-44d9-98eb-7926a80027f8)
![image](https://github.com/user-attachments/assets/dface873-4c7e-4726-8242-105f828e5176)

6.6.	Instalar e reiniciar a vm

![image](https://github.com/user-attachments/assets/0def1a86-e2f5-499c-b483-2a20eb484e86)
 
## 7.	Configurar como servidor de domínio

7.1.	Abrir o `Server Manager` e aguardar o `Dashboard` terminar de carregar

7.2.	Clicar na bandeira com ícone de alerta no menu e selecionar `Promote this server to a domain controller`

![image](https://github.com/user-attachments/assets/12441e8d-c83d-48e3-889b-0e097b42616e)

7.3.	Selecionar `Add a new forest` e inserir nome de domínio `<nome>.local`

![image](https://github.com/user-attachments/assets/0e214b37-9948-452d-a827-682b3bce8cd7)
![image](https://github.com/user-attachments/assets/18f846ea-7da7-407e-847f-61d15a2242d5)
![image](https://github.com/user-attachments/assets/c78f675d-578a-4ab6-8bc8-0ecefb826722)
 
7.4.	Esperar o nome de domínio carregar e clicar em Next

![image](https://github.com/user-attachments/assets/af6c5982-cf6e-44e8-a0eb-c05f0dcb9f87)
![image](https://github.com/user-attachments/assets/fd130cb2-f448-4cbc-b621-5009afbbf971)
![image](https://github.com/user-attachments/assets/f6982226-9e6d-4cb4-9f89-86d8f5bca371)
 
7.5.	Instalar e reiniciar a vm

![image](https://github.com/user-attachments/assets/8ed99af5-51d0-43d6-94b6-be08bafa8f63)

## 8.	Adicionar atalhos dos serviços na Area de Trabalho

8.1.	Pesquisar por `DHCP` no menu `Iniciar` e selecionar `Open file location`

![image](https://github.com/user-attachments/assets/86bf8cf4-51ae-4d56-b69d-eb65cb73e729)
 
8.2.	Copiar os atalhos e colar na `Area de Trabalho` (Não arrastar/mover)
  -	`Activity Directory Users and Computers`
  -	`DHCP`
  -	`DNS`

![image](https://github.com/user-attachments/assets/8838c5c1-6d8c-4805-94df-bd1d094808bf)

## 9.	Configurando o DHCP

9.1.	Acesse o `DHCP`

9.2.	Clique com o botão direito em `IPv4` e selecione `New Scope`

![image](https://github.com/user-attachments/assets/7603ec10-a052-4db7-811a-d1a7ac3a80e0)

9.3.	Nomear o `Escopo`, pode ser um nome qualquer, como do `domínio` ou o próprio `IP`

![image](https://github.com/user-attachments/assets/3f27a41d-8a87-4897-9ad5-14325f2052c1)

9.4.	Configuração da `range` dos endereços de `IP`
 
![image](https://github.com/user-attachments/assets/c7fc0d70-1184-4633-8efb-84ca1cb59cd5)

9.5.	Deixar vazio e clicar em `Next`

![image](https://github.com/user-attachments/assets/64a00937-3cfd-40b3-a3df-cc7bfc71fd02)

9.6.	Definir tempo que o cliente pode usar o `IP`

9.7.	`Next`

![image](https://github.com/user-attachments/assets/07eeba63-8a71-477a-9a8a-848aed40b504)
![image](https://github.com/user-attachments/assets/1fb519f4-fd01-4b8c-80e0-ee2a2d3ef59f)
 
9.8.	Adicionar o endereço do `Gateway`

![image](https://github.com/user-attachments/assets/cea62d53-9b7c-4876-abb4-ece38a2fff57)

9.9.	Em `Server name` inserir o nome definido na etapa 4 e clicar em `Resolve`

![image](https://github.com/user-attachments/assets/3367ec46-504b-44b9-a3d7-e9df62828af0)
 
9.10.	Clicar em `Add` e `Next`

![image](https://github.com/user-attachments/assets/8b6ef17f-4592-44d1-b0f2-a7b625ee3c41)
 
9.11.	Repetir o passo anterior

![image](https://github.com/user-attachments/assets/cf933a37-287a-4236-b5d8-a5153c3d18cd)
 
9.12.	Autorizar `DHCP` do `server`

9.12.1.	Botão direito no `server` e selecionar `Authorize`

![image](https://github.com/user-attachments/assets/fc0c35a6-ef54-4a64-b1fe-8e194252a067) 

9.12.2.	Botão direito e `Refresh`

![image](https://github.com/user-attachments/assets/6abc4ab9-149f-4e9a-b9d5-bc2e120f2c15)
 
9.12.3.	Verificar se o ícone do `IPv4` fica com a bolinha verde

![image](https://github.com/user-attachments/assets/85f9edd6-4462-4153-9e42-c7692d574d3b)

## 10.	Verificar se as configurações do IPv4 estão corretas
    
10.1.	Clicar em `Win+R` e usar o comando `ncpa.cpl`

10.2.	Clicar com o botão direito na `placa de rede` e selecionar `Status`

![image](https://github.com/user-attachments/assets/77b67b5c-d8fe-4353-8d58-037490dd6669)

10.3.	Clicar em `Details` e verificar se as definições estão corretas

![image](https://github.com/user-attachments/assets/ed3ee833-11af-41ee-a5b3-6f190b4eb646)
![image](https://github.com/user-attachments/assets/8f17e421-b439-4cea-b5bf-044e45cc0f1e)


## 11.	Verificar se a máquina está configurada como Rede Interna

11.1.	Menu principal `Máquina -> Configurações`

![image](https://github.com/user-attachments/assets/5eb540d9-c136-428e-a9df-0aec37f18de1)
![image](https://github.com/user-attachments/assets/922b9a8b-4a81-4139-8355-cdeae0ce093a)

## 12.	Máquina Cliente

12.1.	Criar VM

![image](https://github.com/user-attachments/assets/a2ced57f-f0ce-48fd-b525-5f31e51d609b)
![image](https://github.com/user-attachments/assets/9435e5e5-9f0d-43a3-a147-61691fe4e103)
![image](https://github.com/user-attachments/assets/2ba22f23-f3d2-4e45-af6b-f2ab4f8f23fc)
 
12.2.	Configurar como `Rede Interna` e `Iniciar` a VM
 
![image](https://github.com/user-attachments/assets/15270723-a1ae-47fb-8a14-e69c798a3de6)

13.	Instalar o Windows 10

![image](https://github.com/user-attachments/assets/4fde791f-f98a-4bb4-a691-e5c12fca06d8)
![image](https://github.com/user-attachments/assets/f84fc0ea-bd35-4cc5-86c5-4db305142740)
 
13.1.	Caso utilize o `Windows 10` tem que ser a versão `Pro`, não será possível com a versão `Home`
 
![image](https://github.com/user-attachments/assets/776ecf12-adec-4968-9932-7f3a21351172)
![image](https://github.com/user-attachments/assets/e3e70997-56b4-4cfc-97aa-c1acad06ef6b)
![image](https://github.com/user-attachments/assets/000fd948-1ea4-4cbc-912a-df2033aeff69)
![image](https://github.com/user-attachments/assets/e19903c8-868e-492e-bc0d-ae40dae6190b)
![image](https://github.com/user-attachments/assets/f2b66325-48bf-4741-ad79-a817a5afd7ce)
![image](https://github.com/user-attachments/assets/ba4b1226-a071-462e-b2bc-4ad3dc34cbbd)
![image](https://github.com/user-attachments/assets/3d57429f-6e03-4616-8a1b-c30f2d269b9d)
 
## 14.	Desativar Firewall

![image](https://github.com/user-attachments/assets/2f4877aa-e4eb-4c48-ab45-cb1815438b72)

## 15.	Definir IP Dinâmico

15.1.	`Win+R -> ncpa.cpl`

![image](https://github.com/user-attachments/assets/9a372d05-b77b-48b7-86f8-c6b74df03962)
 
15.2.	Botão direito na `Placa de Rede -> Properties`

![image](https://github.com/user-attachments/assets/794b21a2-725b-4567-b872-16065133103b)
 
15.3.	`Internet Protocol Version (TCP/IPv4)`

![image](https://github.com/user-attachments/assets/b113c8d7-9b87-434c-b4cd-9e94918cf784)

15.4.	Definir para obter endereços de `IP` automaticamente

![image](https://github.com/user-attachments/assets/daddca62-5d4e-4a49-bc97-bf224177f7d9)
 
15.5.	Abrir o `CMD` e tentar pingar o endereço do `server` (10.12.27.200)

![image](https://github.com/user-attachments/assets/87e93ed0-30f3-4243-9f60-2df43d4e6ca8)

## 16.	Adicionar ao domínio

16.1.	`Win+X -> System -> Advanced system settings`
 
16.2.	Aba Computer Name -> Change
 
16.3.	Inserir o nome de domínio definido no server-2025
 
16.4.	Autenticar com o usuário e senha do administrador do server (Etapa 2.5)

 
