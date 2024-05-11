# API para Drone de Resgate com Flask e Google AI Platform



Este projeto oferece uma API para controlar drones em missões de busca e salvamento, fornecendo ferramentas que agilizam o processo de localização de vítimas e otimizam a comunicação em situações de emergência. A API permite enviar o drone para locais específicos, transmitir mensagens de áudio pré-gravadas para áreas de difícil acesso, realizar buscas em espiral para varredura de terrenos e, mais importante, analisar imagens aéreas para identificar a presença de pessoas, utilizando a inteligência artificial do Google AI Platform.

A API oferece uma interface centralizada para gerenciar as operações do drone, proporcionando aos socorristas uma visão aérea crucial e facilitando a tomada de decisões em tempo real, com o objetivo final de salvar vidas e auxiliar os necessitados em momentos críticos.


## Funcionalidades

- **Controle do Drone:** Envie o drone para coordenadas GPS específicas.
- **Mensagens de Áudio:** Reproduza mensagens de áudio pré-gravadas para comunicação em áreas remotas.
- **Busca em Espiral:** Realize buscas aéreas em espiral para varrer áreas extensas.
- **Gravação de Vídeo:** Simulação de gravação de vídeo (adapte para a API da sua câmera).
- **Detecção de Pessoas:** Analise imagens aéreas para identificar a presença de pessoas usando um modelo treinado no Google AI Platform.
- **Upload e Download de Áudio:** Gerencie os arquivos de áudio para as mensagens.
- **Autenticação:** Proteção dos endpoints com token JWT para acesso seguro.

## Pré-requisitos

- Python 3.6+
- Flask
- DroneKit
- PyMavlink
- Pygame
- Google Cloud Project
- Modelo de detecção de pessoas treinado no Google AI Platform

## Instalação

1. Clone este repositório:

                         git clone https://github.com/seu-usuario/nome-do-repositorio.git


2. Crie um ambiente virtual e ative-o:

                                            python3 -m venv .venv
                                            source .venv/bin/activate


3. Instale as dependências:

                                        pip install -r requirements.txt

4. Configure as credenciais do Google Cloud:

- Crie um arquivo `credenciais.json` com as credenciais do seu projeto no Google Cloud.
- Defina a variável de ambiente `GOOGLE_APPLICATION_CREDENTIALS` para o caminho do arquivo:

                           export GOOGLE_APPLICATION_CREDENTIALS="caminho/para/credenciais.json"


5. Configure as variáveis do projeto:

A. Substitua os placeholders no arquivo `drone_api.py` pelos valores corretos:

* `COM*`: Porta serial do drone.
* `sua_chave_secreta_aqui`: Chave secreta para gerar tokens JWT.
* `seu-projeto-id`: ID do seu projeto no Google Cloud.
* `seu-endpoint-id`: ID do endpoint do seu modelo no AI Platform.         


# Execução

1. Inicie a API:

                                                  python drone_api.py


2. Acesse a API em `http://127.0.0.1:5000/`.


# Uso

Consulte a documentação da API dentro do código (`drone_api.py`) para obter detalhes sobre os endpoints, parâmetros e exemplos de uso.

# Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.
