
![alt text](image-1.png)

![alt text](image-7.png)

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-5.png)


## Iniciando a VM

![alt text](image-8.png)

![alt text](image-9.png)

![alt text](image-10.png)

![alt text](image-12.png)

![alt text](image-13.png)

![alt text](image-14.png)

Se a tela ficar preta desligar e ligar novamente

![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

## Regras de ouro

### Desativar o Firewall

- Control Panel -> Windows Defender Firewall

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

![alt text](image-22.png)

### Alterar o Nome da Máquina

- Windows Explorer -> This PC (Botão direito) -> Properties

![alt text](image-23.png)

- Rename this PC

![alt text](image-24.png)

![alt text](image-25.png)

Reiniciar

### Definir IP Fixo

- `Win + R` -> `ncpa.cpl`

![alt text](image-26.png)

- Placa de Rede (Botão Direito) -> Properties

![alt text](image-27.png)

- Internet Protocol Version 4 (TCP/IPv4) (Dois cliques)

![alt text](image-28.png)

### Server Manager

#### Instalação dos Serviços

- Add roles and features

![alt text](image-29.png)

- Next

![alt text](image-30.png)

- Next

![alt text](image-31.png)

- Next

![alt text](image-32.png)

- Active Directory Domain Services -> Add Features
- DHCP Server -> Add Features
- DNS Server -> Add Features
- Next

![alt text](image-33.png)

- Next

![alt text](image-34.png)

- Next

![alt text](image-35.png)

- Next

![alt text](image-36.png)

- Next

![alt text](image-37.png)

- Install

![alt text](image-38.png)

- Reiniciar

- Abrir Server Manager
- Aguardar Dashboard terminar de Carregar
- Promote this server to a domain controller

![alt text](image-39.png)

- Add a new forest: fatec.local (\<nome da empresa\>.local)

![alt text](image-40.png)

![alt text](image-41.png)

- Next

![alt text](image-42.png)

- Esperar nome de dominio carregar -> Next

![alt text](image-43.png)

- Next

![alt text](image-44.png)

- Next

![alt text](image-45.png)

- Install

![alt text](image-47.png)

- Restart

### DHCP

- Open file location

![alt text](image-48.png)

Adicionar atalhos na area de trabalho
- DHCP
- DNS
- Activity Directory Users and Computers

Copiar e colar na Area de Trabalho

![alt text](image-49.png)

- IPv4 (Botão direito) -> New Scope

![alt text](image-50.png)

- Nomear o Escopo, pode ser um nome qualquer, como do dominio ou o proprio IP

![alt text](image-51.png)

![alt text](image-60.png)

- (Vazio) Next

![alt text](image-53.png)

- Lease Duration

![alt text](image-54.png)

- Next

![alt text](image-55.png)

- Gateway

![alt text](image-56.png)

- Buscar endereço IP pelo Server name:

![alt text](image-61.png)

- Resolve -> Add -> Next

![alt text](image-62.png)

- Repetir passo anterior

![alt text](image-63.png)

- Autorizar DHCP do server:

![alt text](image-64.png)

- refresh

![alt text](image-65.png)


![alt text](image-66.png)

Verificar se as configurações de ip estão corretas:

- Status -> Details
![alt text](image-67.png)

]![alt text](image-68.png)

![alt text](image-69.png)

Verificar se a Máquina está configurada como Rede Interna

- Maquina -> Configurações -> Rede

![alt text](image-70.png)

![alt text](image-71.png)

## Configurar maquina cliente

![alt text](image-75.png)

![alt text](image-76.png)

![alt text](image-77.png)

Configurações -> Rede -> Rede Interna

![alt text](image-78.png)

- Iniciar

![alt text](image-79.png)

![alt text](image-80.png)

![alt text](image-81.png)

![alt text](image-82.png)

![alt text](image-83.png)

![alt text](image-84.png)

![alt text](image-85.png)

![alt text](image-86.png)

![alt text](image-87.png)

![alt text](image-88.png)

### Regras de Ouro
- Desativar Firewall
