# Trabalho Individual 2020.2

| Lucas Gomes de Oliveira | 15/0137184 |


### 1. Containerização

A Containerização foi realizada nos seguintes arquivos:
- [API](https://github.com/LGomees/Trabalho-Individual-2020-2/blob/master/api/Dockerfile)
- [CLIENT](https://github.com/LGomees/Trabalho-Individual-2020-2/blob/master/client/Dockerfile)
- [DOCKER-COMPOSE](https://github.com/LGomees/Trabalho-Individual-2020-2/blob/master/docker-compose.yml)

Obs: A containerização do banco de dados foi realizada diretamente no docker-compose.

Para rodar os container, rode o seguinte comando: 
```sh
docker-compose up --build
```
![image](https://user-images.githubusercontent.com/18038966/117089481-08a30600-ad2c-11eb-858f-000f5332bbd6.png)

### 2. Integração contínua

Inicialmente a ferramenta escolhida para integração contínua foi o TravisCI, porém por conta de diversos problemas técnicos e pessoais, foi tomado muito tempo para tentar implementá-lo, enfrentando diversos erros. Ao final, a ferramenta foi substituída pelo GitHub Actions, e os arquivos referêntes a integração continua são: 
- [API CI](https://github.com/LGomees/Trabalho-Individual-2020-2/blob/master/.github/workflows/api-ci.yml)
- [CLIENT CI](https://github.com/LGomees/Trabalho-Individual-2020-2/blob/master/.github/workflows/client-ci.yml)
- Foi iniciada a tentativa de implementação do Coveralls para a coleta da cobertura de testes, porém não foi finalizada.

![image](https://user-images.githubusercontent.com/18038966/117089786-e6f64e80-ad2c-11eb-8324-e36d83fc14d8.png)

### 3. Coleta de Métricas

Foi utilizado o SonarCloud para exibir o processo de inspeção continua do código da aplicação. Para isso, o SonarCloud utiliza o SonarQube para realizar a “varredura” em seu código fonte e analisar possíveis vulnerabilidade, erros e regras específicas da linguagem (Code Smells).

![image](https://user-images.githubusercontent.com/18038966/117089830-0b522b00-ad2d-11eb-9d86-66da5c7b8880.png)


Não foram desenvolvidos os seguintes tópicos: Kubernetes, Deploy Contínuo e Coverage.












