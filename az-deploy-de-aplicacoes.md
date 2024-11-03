## Deploy de Aplicações no Azure


## Definição

Deploy consiste no processo de colocar no ar uma aplicação já concluída. Ele pode ocorrer durante várias fases do projeto, bem como após a sua conclusão. 

Além disso, pode haver modificações no código e outras atualizações necessárias, como uma função no aplicativo ou website que ainda não existia. Para essas situações, é preciso fazer o deploy. 

Em inglês, o termo significa “implantar”. Portanto, ele pode ocorrer em diferentes fases de vida do projeto. 

Mas porque esse item é tão importante na área de desenvolvimento? Porque, justamente, ele é a prova final de que o seu aplicativo está rodando bem. 

É na hora de colocar a funcionalidade no ar que podem aparecer bugs ou então falhas de UX, que podem causar uma experiência não muito satisfatória no usuário. 

Quando um site é concluído por um desenvolvedor, após os devidos testes, ele é finalmente hospedado e colocado no ar, ele passa pelo processo de deploy.

Por isso, os DEVs ficam atentos a esse momento. Sendo assim, se você está iniciando na área, fique atento a essa etapa tão importante do seu projeto.  


Principais tipos de Deploy

Mas você sabia que existem 3 tipos principais de deploy, conforme o seu processo de desenvolvimento? Veja a seguir quais são elas. 

Manual

É trabalhoso, mas também muito utilizado ainda hoje. O processo é manual e, por conta disso, mais demorado. 

O principal exemplo de deploy manual é o FTP (Protocolo de Transferência de Arquivo). Ele possibilita que arquivos sejam transferidos de um computador para outro por meio da internet. Mas, de qualquer jeito, ele precisa da interferência humana. 

Suas desvantagens são o tempo maior que se usa na mesma tarefa e ainda a falta de mais recursos disponíveis que facilitem o trabalho. Além disso, corre-se o risco de mais de uma pessoa desenvolvedora subir o mesmo arquivo.  

Parcialmente automatizado

Por mais que a aplicação desenvolva automaticamente os comandos, ainda é necessária a intervenção da pessoa desenvolvedora. 

É o caso, por exemplo, da atualização de um repositório GIT. Mesmo que haja alguns comandos humanos, outros são automatizados. É o caso do push do branch master, que atualiza o servidor de forma automática.  


Completamente automatizado

O deploy completamente automatizado é o que traz mais vantagens à rotina da pessoa desenvolvedora. Isso porque ele representa mais eficiência, rapidez e segurança na hora da atualização. 

Assim, ele pode ser usado em qualquer aplicação, website, plataforma digital, aplicativo, entre outros. 

Entre os mais habituais na atualidade estão o Azure, Circle CI, Gitlab, Jenkins e Pipelines.  



Melhores práticas de implantação


Componentes de implantação
Origem da implantação
A origem da implantação é o local do código do aplicativo. Para aplicativos de produção, a origem da implantação geralmente é um repositório hospedado pelo software de controle de versão, como o GitHub, o BitBucket ou o Azure Repos. Para cenários de desenvolvimento e teste, a origem da implantação pode ser um projeto em seu computador local. 



Pipeline de build
Depois de decidir sobre a origem da implantação, a próxima etapa é escolher um pipeline de build. Um pipeline de build lê o código-fonte da origem da implantação e executa uma série de etapas (como compilar código, minificar HTML e JavaScript, executar testes e empacotar componentes) para obter o aplicativo em um status executável. Os comandos específicos executados pelo pipeline de build dependem da pilha de linguagem. Essas operações podem ser executadas em um servidor de build, como Azure Pipelines, ou executadas localmente. 



Mecanismo de implantação
O mecanismo de implantação é a ação usada para colocar seu aplicativo interno no diretório /home/site/wwwroot do seu aplicativo Web. O diretório /wwwroot é um local de armazenamento montado compartilhado por todas as instâncias do aplicativo Web. Quando o mecanismo de implantação coloca seu aplicativo nesse diretório, as instâncias recebem uma notificação para sincronizar os novos arquivos. O Serviço de Aplicativo dá suporte às seguintes opções de implantação:

Pontos de extremidade Kudu: o Kudu é a ferramenta de produtividade para desenvolvedores de software livre que é executada como um processo separado no Serviço de Aplicativo do Windows e como um segundo contêiner no Serviço de Aplicativo do Linux. O Kudu lida com implantações contínuas e fornece pontos de extremidade HTTP para implantação, como o zipdeploy/.
FTP e WebDeploy: usando suas credenciais de site ou de usuário, é possível carregar arquivos via FTP ou WebDeploy. Esses mecanismos não passam pelo Kudu.
As ferramentas de implantação, como o Azure Pipelines, o Jenkins e os plugins de editor usam um desses mecanismos de implantação. 



Usar slots de implantação
Sempre que possível, use os slots de implantação ao implantar um novo build de produção. Ao usar uma camada de Plano do Serviço de Aplicativo Padrão ou melhor, você pode implantar seu aplicativo em um ambiente de preparo, validar suas alterações e fazer teste de aceitação do build. Quando estiver pronto, você poderá trocar os slots de preparação e produção. A operação de troca ativa as instâncias de trabalho necessárias para corresponder à escala de produção, eliminando assim o tempo de inatividade. 



Código de implantação contínua
Se o projeto tiver branches designados para teste, garantia de qualidade e de preparo, cada um desses branches deverá ser implantado continuamente em um slot de preparo. (Isso é conhecido como o Design do Gitflow). Ele permite que os stakeholders avaliem e testem facilmente o branch implantado.

A implantação contínua nunca deve ser habilitada para o slot de produção. Em vez disso, seu branch de produção (geralmente a principal) deve ser implantado em um slot de não produção. Quando estiver pronto para liberar o branch de base, troque-o no slot de produção. Trocar para produção, em vez de implantar na produção, evita o tempo de inatividade e permite reverter as alterações trocando novamente. 


Contêineres de implantação contínua
Para contêineres personalizados do Docker ou de outros registros de contêiner, implante a imagem em um slot de preparo e troque para o de produção para evitar o tempo de inatividade. A automação é mais complexa do que a implantação de código, pois você deve enviar por push a imagem para um registro de contêiner e atualizar a marca de imagem no webapp.

Para cada branch que você deseja implantar em um slot, configure a automação para fazer os passos a seguir em cada commit com o branch.

Crie e marque a imagem. Como parte do pipeline de build, marque a imagem com a ID de git commit, o carimbo de data/hora ou outras informações de identificação. É melhor não usar a marca padrão "mais recente". Caso contrário, é difícil fazer o rastreamento do código que está implantado no momento, o que torna a depuração muito mais difícil.
Envie por push a imagem marcada. Depois que a imagem é criada e marcada, o pipeline a envia por push para o registro de contêiner. Na próxima etapa, o slot de implantação vai efetuar pull da imagem marcada do registro de contêiner.
Atualize o slot de implantação com a nova marca de imagem. Quando essa propriedade for atualizada, o site vai reiniciar automaticamente e efetuar pull da nova imagem de contêiner. 



Usar o Azure DevOps
O Serviço de Aplicativo tem entrega contínua interna para contêineres por meio da Central de Implantação. Navegue até seu aplicativo no portal do Azure e selecione Centro de Implantação em Implantação. Siga as instruções para selecionar o repositório e o branch. Isso vai configurar um pipeline de lançamento e de build do DevOps para criar, marcar e implantar automaticamente o contêiner quando novas confirmações forem enviadas por push para o branch selecionado. 



Usar o GitHub Actions
Você também pode automatizar a implantação de contêiner com o GitHub Actions. O arquivo de fluxo de trabalho abaixo vai criar e marcar o contêiner com a ID de commit, enviar por push a um registro de contêiner e atualizar o aplicativo Web especificado com a nova marca de imagem. 

on:
  push:
    branches:
    - <your-branch-name>

name: Linux_Container_Node_Workflow

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    # checkout the repo
    - name: 'Checkout GitHub Action'
      uses: actions/checkout@main

    - uses: azure/docker-login@v1
      with:
        login-server: contoso.azurecr.io
        username: ${{ secrets.REGISTRY_USERNAME }}
        password: ${{ secrets.REGISTRY_PASSWORD }}

    - run: |
        docker build . -t contoso.azurecr.io/nodejssampleapp:${{ github.sha }}
        docker push contoso.azurecr.io/nodejssampleapp:${{ github.sha }} 

    - uses: azure/webapps-deploy@v2
      with:
        app-name: 'node-rnc'
        publish-profile: ${{ secrets.azureWebAppPublishProfile }}
        images: 'contoso.azurecr.io/nodejssampleapp:${{ github.sha }}' 





Usar outros provedores de automação
As etapas listadas anteriormente se aplicam a outros utilitários de automação, como o CircleCI ou o Travis CI. No entanto, você precisa usar a CLI do Azure para atualizar os slots de implantação com as novas marcas de imagem na etapa final. Para usar a CLI do Azure em seu script de automação, gere uma Entidade de Serviço usando o comando a seguir. 



az ad sp create-for-rbac --name "myServicePrincipal" --role contributor --scopes /subscriptions/{subscription}/resourceGroups/{resource-group} --sdk-auth 



Em seu script, faça logon usando az login --service-principal e fornecendo as informações da entidade de segurança. Você pode usar az webapp config container set para definir o nome do contêiner, a marca, a URL do registro e a senha do registro. Abaixo estão alguns links úteis para construir o processo de CI de contêiner. 



Considerações específicas a linguagens
Java
Use a API zipdeploy/ do Kudu para implantar aplicativos JAR e a wardeploy/ para aplicativos WAR. Se você está usando o Jenkins, pode usar essas APIs diretamente na fase de implantação. Para obter mais informações, consulte este artigo.

Nó
Por padrão, o Kudu executa as etapas de build para o seu aplicativo do Node (npm install). Se você está usando um serviço de build como o Azure DevOps, o build do Kudu é desnecessário. Para desabilitar o build do Kudu, crie uma configuração de aplicativo SCM_DO_BUILD_DURING_DEPLOYMENT com um valor de false.

.NET
Por padrão, o Kudu executa as etapas de build para o aplicativo .NET (dotnet build). Se você está usando um serviço de build como o Azure DevOps, o build do Kudu é desnecessário. Para desabilitar o build do Kudu, crie uma configuração de aplicativo SCM_DO_BUILD_DURING_DEPLOYMENT com um valor de false. 




Outras considerações de implantação
Cache Local
O conteúdo do Serviço de Aplicativo do Azure é armazenado no Armazenamento do Microsoft Azure e exibido de forma duradoura como um compartilhamento de conteúdo. No entanto, alguns aplicativos precisam apenas de um repositório de conteúdo somente leitura de alto desempenho que podem ser executados com alta disponibilidade. Esses aplicativos podem se beneficiar do uso do cache local. O cache local não é recomendado para sites de gerenciamento de conteúdo, como o WordPress.

Sempre use o cache local junto com os slots de implantação para evitar o tempo de inatividade. Consulte esta seção para obter informações sobre como usar esses recursos juntos. 


CPU ou memória altas
Se o Plano do Serviço de Aplicativo estiver usando mais de 90% da memória ou da CPU disponível, a máquina virtual subjacente poderá ter problemas para processar a implantação. Quando isso acontece, escale verticalmente de maneira temporária a contagem de instâncias para executar a implantação. Depois que a implantação for concluída, retorne a contagem de instâncias para o valor anterior.

Para obter mais informações sobre as melhores práticas, visite Diagnóstico do Serviço de Aplicativo para as melhores práticas acionáveis específicas ao seu recurso.

Navegue até o seu aplicativo Web no portal do Azure.
Selecione Diagnosticar e resolver problemas no painel de navegação à esquerda, o que abre o Diagnóstico do Serviço de Aplicativo.
Escolha a peça da página inicial de Melhores Práticas.
Selecione Melhores Práticas para Disponibilidade e Desempenho ou Melhores Práticas para a Configuração Ideal para exibir o status atual do aplicativo em relação a essas melhores práticas. 


Implantação contínua no Serviço de Aplicativo do Azure 



O Serviço de Aplicativo do Azure permite a implantação contínua de repositórios GitHub, Bitbucket e Azure Repos ao efetuar pull das atualizações mais recentes.

Preparar o repositório
Para obter builds automáticos do servidor de build do Serviço de Aplicativo do Azure, verifique se a raiz do repositório tem os arquivos adequados no projeto. 


Configurar a fonte de implantação
No portal do Azure, vá para a página de gerenciamento do seu aplicativo do serviço de aplicativo.

No painel esquerdo, selecione Centro de Implantação. Em seguida, selecione Configurações.

Na caixa Origem, selecione uma das opções de CI/CD: 



Selecione a guia que corresponde ao seu provedor de compilação para continuar. 


O GitHub Actions é o provedor de compilação padrão. Para alterar o provedor, selecione Alterar provedor>Serviço de compilação do Serviço de Aplicativo>OK.

Ao realizar a primeira implantação pelo GitHub, selecione Autorizar e siga os prompts de autorização. Para usar o repositório de um usuário diferente, selecione Alterar conta.

Depois de autorizar sua conta do Azure com o GitHub, selecione a Organização, o Repositório e o Branch desejados.

Quando não é possível localizar uma organização ou um repositório, pode ser necessário habilitar mais permissões no GitHub. Para obter mais informações, consulte Gerenciamento do acesso aos repositórios de sua organização.

Em Tipo de autenticação, selecione Identidade atribuída pelo usuário para obter uma melhor segurança. Para obter mais informações, confira as perguntas frequentes. 


A integração do Bitbucket usa os serviços de compilação do Serviço de Aplicativo para automação de compilação.

Ao realizar a primeira implantação pelo Bitbucket, selecione Autorizar e siga os prompts de autorização. Para usar o repositório de um usuário diferente, selecione Alterar conta.

Para o Bitbucket, selecione a Equipe, o Repositório e a Ramificação que você deseja implantar continuamente.

Selecione Salvar.

Novas confirmações no repositório e no branch selecionados agora são implantadas continuamente em seu aplicativo do Serviço de Aplicativo. É possível acompanhar as confirmações e implantações na guia Logs. 


Azure Repos

O serviço de compilação do Serviço de Aplicativo é o provedor de compilação padrão.

 Observação

Para usar o Azure Pipelines como o provedor de compilação para seu aplicativo do Serviço de Aplicativo, configure-o diretamente do Azure Pipelines. Não o configure no Serviço de Aplicativo. A opção Azure Pipelines apenas o direciona adequadamente. 


Selecione a Organização do Azure DevOps, o Projeto, o Repositório e a Ramificação que você deseja implantar continuamente.

Quando sua organização do DevOps não está listada, há possibilidade de ela ainda não ter sido vinculada à sua assinatura do Azure.  


Desabilitar a implantação contínua
No portal do Azure, vá para a página de gerenciamento do seu aplicativo do serviço de aplicativo.

No painel esquerdo, selecione Centro de Implantação. Em seguida, selecione Configurações>Desconectar: 


Por padrão, o arquivo do fluxo de trabalho do GitHub Actions está preservado no seu repositório, mas continua a disparar a implantação no seu aplicativo. Para excluir o arquivo do repositório, selecione Excluir arquivo de fluxo de trabalho.

Selecione OK. 




Quais são os provedores de compilação?
Dependendo da origem da implantação no Centro de Implantação, você poderá ver algumas opções para selecionar para provedores de compilação. Os provedores de compilação ajudam você a criar uma solução de CI/CD com o Serviço de Aplicativo do Azure automatizando a compilação, o teste e a implantação.

Você não está limitado às opções de provedor de compilação encontradas no Centro de Implantação, mas o Serviço de Aplicativo permite que você as configure rapidamente e oferece uma experiência integrada de registro em log de implantação. 


Github Actions 

O provedor de compilação do GitHub Actions está disponível apenas para implantação do GitHub. Quando configurado do Centro de Implantação do aplicativo, ele conclui estas ações para configurar a CI/CD:

Ele deposita um arquivo de fluxo de trabalho do GitHub Actions no repositório do GitHub para lidar com tarefas de compilação e implantação no serviço de aplicativo.
Para autenticação básica, ele adiciona o perfil de publicação para o aplicativo como um segredo do GitHub. O arquivo de fluxo de trabalho usa esse segredo para autenticar-se no serviço de aplicativo.
Para obter a identidade atribuída pelo usuário, confira O que a opção de identidade atribuída pelo usuário faz para o GitHub Actions?
Captura informações dos logs de execução de fluxo de trabalho e as exibe na guia Logs no Centro de Implantação.
É possível personalizar o provedor de compilação GitHub Actions das formas a seguir:

Personalize o arquivo de fluxo de trabalho depois que ele for gerado no repositório GitHub. Para saber mais, consulte Sintaxe de fluxo de trabalho para o GitHub Actions. Certifique-se de que o fluxo de trabalho seja implantado no Serviço de Aplicativo com a ação azure/webapps-deploy.
Se a ramificação selecionada estiver protegida, você ainda poderá visualizar o arquivo de fluxo de trabalho sem salvar a configuração e, em seguida, adicioná-lo manualmente ao repositório. Esse método não fornece integração de log com o portal do Azure.
Em vez de usar a autenticação básica ou uma identidade atribuída pelo usuário, você também pode implantar usando uma entidade de serviço no Microsoft Entra ID. Isso não pode ser configurado no portal. 



Serviço de compilação do Serviço de Aplicativo 

Observação

O serviço de compilação do Serviço de Aplicativo requer que a autenticação básica SCM seja habilitada para que o webhook funcione. Para obter mais informações, confira Implantação sem autenticação básica.

O serviço de compilação do Serviço de Aplicativo é o mecanismo de compilação e implantação nativo do Serviço de Aplicativo, também conhecido como Kudu. Quando essa opção for selecionada, o Serviço de Aplicativo adicionará um webhook ao repositório autorizado. Qualquer push de código para o repositório dispara o webhook, e o Serviço de Aplicativo efetua pull das alterações em seu repositório e executa todas as tarefas de implantação.  


Azure Pipelines


O Azure Pipelines faz parte do Azure DevOps Services. Você pode configurar um pipeline para criar, testar e implantar seu aplicativo no Serviço de Aplicativo a partir de qualquer repositório de origem com suporte.

Para usar o Azure Pipelines como o provedor de compilação, não o configure no Serviço de Aplicativo, mas vá diretamente para o Azure DevOps. No Centro de Implantação, a opção Azure Pipelines apenas indica a direção certa. 

