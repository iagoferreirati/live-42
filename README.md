# live-42

 ``` Comandos ```

Baixar o repositorio
Acessar a pasta gerada pelo Download

- vagrant up

Validar conexão

- ssh vagrant@ip_da_maquinas

Instalar Ansible

- sudo apt update
- sudo apt install ansible

Criar um arquivo de inventario e cadastra os servidores

- vim inventario.txt

Validar conexão pelo ansible

- ansible -i inventario.txt all -m ping

Instalar/gerenciar servidores remotos

- ansible -i inventario all -b -m apt -a "name=net-tools"
- ansible -i inventario all -b -m user -a "name=seu_nome"
