# Instalação do Docker Engine

1- Para a instalação do Docker precisa abrir o terminal do Linux, que pode ser encontrado no menu iniciar, basta procurar por "Ubuntu" e abrir o Ubuntu 20.04 que aparecerá.

![image](https://user-images.githubusercontent.com/126198206/221571790-94efcfe0-b589-409c-8fc0-bc8f72ee910b.png)

2- Instalando algumas ferramentas que serão utilizadas no processo de instalação.

**`sudo apt install --no-install-recommends apt-transport-https ca-certificates curl gnupg2`**

3- Carregando em variáveis de ambiente definições da distribuição e versão.

**`source /etc/os-release`**

4- Adicionando a chave GPG de um repositório de pacotes que usaremos como origem de instalação.

**`curl -fsSL https://download.docker.com/linux/${ID}/gpg | sudo apt-key add -`**

5- Adicionando o repositório em si à lista de origens de pacotes.

**`echo "deb [arch=amd64] https://download.docker.com/linux/${ID} ${VERSION_CODENAME} stable" | sudo tee /etc/apt/sources.list.d/docker.list`**

6- Buscando a lista de pacotes deste novo repositório adicionado.

**`sudo apt update`**

7- Instalando os pacotes do Docker Engine.

**`sudo apt install docker-ce docker-ce-cli containerd.io`**

8- Baixando o binário do Docker Compose diretamente do GitHub.

**`sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`**

9- Tornando o binário do Docker Compose executável.

**`sudo chmod +x /usr/local/bin/docker-compose`**


**Dicas:**

I-  Para trabalhar com o Docker é necessário executar o comando **`sudo dockerd`** no terminal do Linux e abrir um novo terminal para seguir com os comandos necessários.

II- Lembre de sempre executar o Ctrl+C para finalizar o serviço do Docker no mesmo terminal que foi executado o comando "sudo dockerd".
