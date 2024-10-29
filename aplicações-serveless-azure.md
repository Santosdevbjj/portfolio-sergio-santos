## Criar uma aplicação Serverless com Azure
## Functions

![Screenshot_20241029-004051](https://github.com/user-attachments/assets/2acfd8da-f5c5-4832-b3cd-128fd412b60f)


É uma ótima opção para construir soluções que respondem a eventos em tempo real, sem a necessidade de gerenciar infraestrutura. No modelo Serverless, o Azure se encarrega de toda a infraestrutura, permitindo que você foque apenas no desenvolvimento do código.

Vamos abordar os passos principais para criar uma aplicação com Azure Functions, seguido de um exemplo prático.

## 1. O que são Azure Functions?

Azure Functions são pequenas funções que podem ser ativadas por eventos e executadas de forma independente. Elas são ideais para tarefas de curta duração e que precisam escalar automaticamente, como processamento de dados em tempo real, automação de tarefas, APIs serverless, entre outros.

## 2. Configurando o Ambiente para Azure Functions

Para começar, você precisará do Azure CLI e do Azure Functions Core Tools instalado na sua máquina. Você também deve ter uma conta no Azure e o Visual Studio Code com a extensão Azure Functions.

## Pré-requisitos:

Conta no Azure

Visual Studio Code

Azure CLI

Azure Functions Core Tools


## 3. Criando uma Aplicação Serverless com Azure Functions

Passo a Passo para Criar sua Primeira Função

1. Criar um Novo Projeto de Azure Function:

No terminal ou Visual Studio Code, navegue até o diretório onde deseja criar o projeto.

Execute o seguinte comando para criar um novo projeto de funções:

## func init MeuProjetoFunc --worker-runtime node

Aqui, node é o runtime, mas você pode escolher outros, como python, dotnet, java, etc.



## 2. Adicionar uma Função ao Projeto:

Após criar o projeto, adicione uma função dentro dele. Por exemplo, para criar uma função HTTP:

## func new --name MinhaFuncaoHttp --template "HTTP trigger"

Esse comando cria uma função que é ativada por requisições HTTP.



## 3. Configurar o Arquivo local.settings.json:

Esse arquivo contém configurações locais da aplicação. Para desenvolvimentos iniciais, a configuração padrão costuma funcionar bem.

## Exemplo de conteúdo:

## {
  ## "IsEncrypted": false,
 ##  "Values": {
   ##  "AzureWebJobsStorage": "UseDevelopmentStorage=true",
  ##   "FUNCTIONS_WORKER_RUNTIME": "node"
 ##  }
## }



## Exemplo de Código para uma Função HTTP

A função gerada estará no diretório MeuProjetoFunc/MinhaFuncaoHttp. Abaixo, um exemplo em JavaScript de uma função HTTP que responde com uma mensagem personalizada:

## module.exports = async function (context, req) {
   ##  const name = req.query.name || (req.body && req.body.name);
   ##  context.res = {
        status: 200,
        body: `Hello, ${name || 'World'}!`
   ## };
## };

Essa função lê o nome de uma query string ou do corpo da requisição HTTP e responde com uma saudação.

## 4. Executar a Função Localmente:

No terminal, navegue até o diretório do projeto e execute o comando:

## func start

A função será executada localmente e você verá uma URL como http://localhost:7071/api/MinhaFuncaoHttp. Você pode acessar essa URL no navegador ou por ferramentas como o Postman para testar a função.

## 4. Publicando no Azure

1. Criar um Grupo de Recursos e um Plano de Hospedagem:

No terminal, execute o comando para criar um grupo de recursos:

## az group create --name MeuGrupoFunc --location eastus

## Crie um Plano de Funções no Azure:

## az functionapp plan create --name MeuPlanoFunc --resource-group MeuGrupoFunc --location eastus --consumption-plan-location eastus --sku Dynamic

## 2. Criar o Function App no Azure:

Execute o comando abaixo para criar o Function App, onde as funções serão hospedadas:

## az functionapp create --resource-group MeuGrupoFunc --consumption-plan-location eastus --runtime node --runtime-version 16 --functions-version 4 --name MeuFunctionApp --storage-account NomeDaSuaContaDeStorage


## 3. Publicar a Função no Azure:

No diretório do projeto, execute:

func azure functionapp publish MeuFunctionApp

Após a publicação, o Azure gera uma URL para a função. Você pode acessar essa URL diretamente ou utilizar ferramentas para testá-la.

5. Automatizando Tarefas com Azure Functions e Exemplo de Timer Trigger

Além de funções HTTP, você pode criar funções que respondem a outros tipos de eventos, como cron jobs. Um exemplo de função que roda a cada 5 minutos:

## module.exports = async function (context, myTimer) {
  ##  var timeStamp = new Date().toISOString();
    if (myTimer.isPastDue) {
        context.log('A execução está atrasada!');
    }
  ##  context.log('Funcão Timer disparada!', timeStamp);
## };

## Para criar uma função Timer, use:

## func new --name FuncaoTimer --template "Timer trigger"

Esse exemplo é configurado para disparar a cada 5 minutos, e o código registra o timestamp cada vez que é executado.

## 6. Benefícios do Modelo Serverless com Azure Functions

## Escalabilidade Automática: O Azure Functions escala automaticamente para lidar com picos de carga.

## Custo por Uso: Você só paga pelo tempo de execução do código, o que pode ser bem mais econômico.

## Desenvolvimento Ágil: Concentre-se no código sem se preocupar com a infraestrutura.

## Conclusão

Azure Functions são uma excelente maneira de implementar aplicações Serverless. Elas permitem criar soluções ágeis e escaláveis, ideais para microserviços, automação e processamento de dados em tempo real. Experimente implementar diferentes tipos de gatilhos e explore a flexibilidade do modelo Serverless! 


