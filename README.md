# Exercicio Complementar
Exercício complementar para alunos de MBA

## Contexto

Neste exercício os alunos devem exercitar conteúdos vistos nas aulas anteriores, como:
1. Criação de um repositório do GitHub
2. Criação de uma Action (workflow) do zero para executar um script
3. Criação de Variáveis de Ambiente
4. Configuração de proteção de branch
5. Criação de pull requests

## Instruções

### Parte 1 - Criação do repositório e da Action

1. Crie um repositório no GitHub chamado `exercicio-final-fiap` na sua conta pessoal
2. Crie uma Action (workflow) chamada `main.yml` que execute o seguinte passo a passo:
   1. Faça o checkout do repositório (use o `actions/checkout@v3`)
   2. Execute os seguintes jobs:
        1. Crie um job chamado `linux` que execute em um ambiente `ubuntu-latest` e imprima a mensagem `Hello World!` no console
        2. Crie um job chamado `windows` que execute em um ambiente `windows-latest` e imprima a mensagem `Hello World!` no console
        3. Crie um job chamado `macos` que execute em um ambiente `macos-latest` e imprima a mensagem `Hello World!` no console
        4. Crie um job chamado `final`que dependa dos jobs `linux`, `windows` e `macos` e imprima a mensagem `Finalizado!` no console
   3. Faça o commit das alterações
   
### Parte 2 - Criação de variáveis de ambiente no repositório

1. Crie uma variável de ambiente chamada `NOME` com o valor do seu nome completo
2. Crie uma variável de ambiente chamada `RA` com o valor do seu RA
3. Crie uma variável de ambiente chamada `CURSO` com o valor do seu curso
4. Crie um workflow chamado `meus-dados.yml` que contenha um job chamado `meus-dados` que tenha os seguintes "steps":
    1. Imprime a variável de ambiente `NOME` no console
    2. Imprime a variável de ambiente `RA` no console
    3. Imprime a variável de ambiente `CURSO` no console
5. Faça o commit das alterações

### Parte 3 - Configuração de proteção de branch

1. Crie uma branch chamada `develop`
2. Configure uma proteção do branch `main` para que seja protegido e que seja necessário um pull request para fazer o merge
3. Crie um arquivo na branch `develop` chamado `develop.txt` com o conteúdo `develop`
4. Faça o commit das alterações
5. Crie um pull request da branch `develop` para a branch `main`
6. Faça o merge do pull request

### Parte 4 - Deploy na Azure

1. Abra sua conta na Azure
2. Crie um novo Web App chmando `exercicio-final-fiap`
3. Configure o App para que utilize Node 16
4. Na parte de `Deployment Center` escolha a opção `GitHub`
5. Escolha o repositório `exercicio-final-fiap`
6. Escolha a branch `main`
7. Faça o deploy

#### Observações

1. O exercício deve ser feito individualmente
2. Você pode utilizar o código da aplicação deste repositório para fazer o deploy na Azure
3. Você pode utilizar o código da aplicação deste repositório para testar a Action
4. Você pode utilizar os seguintes tutoriais para fazer o deploy do seu App na Azure: 
   1. https://docs.microsoft.com/en-us/azure/app-service/deploy-github-actions?tabs=applevel
   2. https://learn.microsoft.com/en-us/azure/app-service/quickstart-nodejs?tabs=linux&pivots=development-environment-vscode
5. 