# DrexBesuDeployer

![Licença](https://img.shields.io/badge/License-Apache%202.0-blue.svg)
![Docker](https://img.shields.io/badge/Docker-Ready-blue?logo=docker)

## Visão Geral

O **DrexBesuDeployer** é uma ferramenta de orquestração robusta projetada para agilizar a configuração e implantação de nós da Hyperledger Besu. Inspirado pelos princípios arquitetônicos do **Drex** (CBDC do Banco Central do Brasil), esta ferramenta permite que desenvolvedores e empresas iniciem uma rede de consenso (QBFT ou IBFT) de produção com apenas alguns comandos, eliminando a necessidade de configurações manuais complexas.

[![Tutorial Docker & Docker Compose](https://i.ibb.co/7bc5K4v/CBDC3-MINUTES.jpg)](https://www.youtube.com/watch?v=wcjsAaBnzNI)

## Funcionalidades Principais

*   **Implantação Rápida:** Inicialize uma rede multi-nó do Besu com um único comando.
*   **Gerenciamento Automático de Chaves:** Gera automaticamente chaves criptográficas para cada nó da camada de consenso.
*   **Arquitetura Containerizada:** Utiliza Docker e Docker Compose para garantir ambientes isolados e consistentes.
*   **Interface Intuitiva:** Interface de linha de comando interativa para especificação de nós e topologia de rede.

## Pré-requisitos

Antes de prosseguir, certifique-se de que os seguintes itens estão instalados e em execução:

*   **Docker Engine:** Versão 20.10+
*   **Docker Compose:** Versão 1.29+
*   **Shell Bash:** (Nativo em Linux/macOS, usuários Windows devem usar Git Bash ou WSL)

## Instalação e Configuração

### 1. Instale o Docker

**Windows / macOS:**
Baixe e instale o [Docker Desktop](https://www.docker.com/products/docker-desktop). Ele inclui o Docker Compose por padrão.

**Linux (Ubuntu/Debian):**
bash
# Atualizar o índice de pacotes
sudo apt-get update

# Instalar o Docker Engine
sudo apt-get install docker-ce docker-ce-cli containerd.io

# Instalar o Docker Compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose


### 2. Implante a Rede

1.  Clone o repositório:
    bash
    git clone https://github.com/your-username/drex-besu-deployer.git
    cd drex-besu-deployer
    

2.  Execute o script de instalação:
    bash
    sh install.sh
    
    *Nota: Este script verifica seu ambiente Docker e inicializa as configurações necessárias.*

## Uso

Após a instalação, siga os prompts na tela para especificar o número de nós e os parâmetros da rede. A ferramenta gerará o arquivo `docker-compose.yml` e iniciará os containers automaticamente.

## Estrutura do Projeto

*   `Dockerfile`: Define a imagem personalizada do nó Besu.
*   `qbftConfigFile.json`: Modelo de configuração de consenso.
*   `install.sh`: Script de bootstrap para validar dependências e preparar o ambiente.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para enviar um Pull Request.

## Licença

Este projeto está licenciado sob a Licença Apache 2.0 - veja o arquivo [LICENSE](LICENSE) para detalhes.

## Isenção de Responsabilidade

Esta ferramenta é um utilitário de código aberto para fins educacionais e de desenvolvimento. Não é afiliada ou endossada pelo Banco Central do Brasil ou por quaisquer entidades oficiais do projeto Drex.