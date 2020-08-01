## Laboratório de Pipeline Automatizado - CI/CD | Bootcamp DevOps da IGTI

### Pré-requisito

- Instância EC2 Ubuntu na AWS com Docker instalado

### 1. Configurar Security Group AWS Console

- Adicionar regra de entrada TCP 8080 para o Jenkins

### 2. Instalar Java 8 no servidor

```bash
sudo apt install openjdk-8-jre-headless
```

### 3. Instalar [Jenkins](https://www.jenkins.io/download/) dentro de um novo diretório `tools`

```bash
wget http://mirrors.jenkins.io/war-stable/2.235.3/jenkins.war

# executar para obter senha para prosseguir com instalacao e encerra-lo (ctrl + c)
java -jar jenkins.war

# certificar que nao tenha nenhum processo java em execucao
ps -ef | grep java

# executar novamente, porem em background e prosseguir com instalacao no navegador instalando plugins sugeridos
java -jar jenkins.war &
```

### 4. Criar um projeto no GitHub

### 5. Criar pipeline CI/CD no Jenkins