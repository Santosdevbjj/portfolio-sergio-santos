## Serviços disponíveis por categorias e tipos de região

A disponibilidade de serviços em regiões do Azure depende do tipo de uma região. Há dois tipos de regiões no Azure: recomendado e alternativo.

Recomendado: essas regiões fornecem a mais ampla variedade de recursos de serviço e atualmente dão suporte a zonas de disponibilidade. Designadas no portal do Azure como Recomendado.
Alternativo: essas regiões estendem o volume do Azure dentro de um limite de residência de dados em que há, atualmente, uma região recomendada. As regiões alternativas ajudam a otimizar a latência e a fornecer uma segunda região para as necessidades de recuperação de desastre, mas não dão suporte a zona de disponibilidade. O Azure realiza avaliações regulares de regiões alternativas para determinar se elas devem se tornar regiões recomendadas. Designadas no portal do Azure como Outras. 

Categorias de serviço entre tipos de região
Os serviços do Azure estão agrupados em três categorias: serviços fundamentais, básicos e estratégicos. A política geral do Azure de implantação de serviços em qualquer região específica é controlada principalmente por tipo de região, categorias de serviço e demanda do cliente.

## Fundamental:

disponível em todas as regiões recomendadas e alternativas quando a região está disponível para o público geral ou dentro de 90 dias de um novo serviço fundamental, ficando disponível para o público geral.

## Básico:

disponível em todas as regiões recomendadas dentro de 90 dias da disponibilidade geral da região. Controlada por demanda em regiões alternativas e muitas já estão implantadas em um grande subconjunto de regiões alternativas.

## Estratégico:

(conhecido anteriormente como Especializado): ofertas de serviço direcionadas, geralmente focadas no setor ou com suporte por hardware personalizado. Disponibilidade orientada por demanda entre regiões, e muitas já estão implantadas em um grande subconjunto de regiões recomendadas. 

Em Microsoft Azure, "Localizando Serviços por Categoria" é o recurso que permite explorar os serviços disponíveis de acordo com a função ou área de aplicação deles.

Azure oferece centenas de serviços, e, para facilitar o uso e a busca, esses serviços estão organizados por categorias.

Vamos explorar em detalhes cada uma das principais categorias e ver exemplos práticos de como cada uma delas pode ser utilizada:

## 1. Computação

A categoria Computação engloba serviços que fornecem capacidade de processamento para executar aplicativos, desde máquinas virtuais até computação sem servidor (serverless).

## Azure Virtual Machines (VMs):

Você pode criar VMs para hospedar aplicativos, bancos de dados ou até mesmo simular um ambiente local na nuvem. Exemplo: uma VM com Windows Server para rodar uma aplicação empresarial.

## Azure App Service:

Ideal para hospedar sites e APIs sem se preocupar com a infraestrutura. Exemplo: uma empresa cria um aplicativo web de e-commerce e hospeda no App Service, garantindo escalabilidade automática.

## Azure Functions:

Computação serverless, onde você paga apenas pelo tempo de execução do código. Exemplo: uma função que envia notificações por e-mail quando novos dados são inseridos em um banco de dados.


## 2. Rede

A categoria Rede contém serviços para gerenciamento de redes, conectividade entre recursos e segurança.

## Azure Virtual Network (VNet):

Permite criar redes virtuais para conectar VMs e outros recursos. Exemplo: uma rede privada onde apenas usuários autenticados conseguem acessar as aplicações.

## Azure Load Balancer:

Distribui o tráfego entre várias instâncias para alta disponibilidade. Exemplo: uma aplicação web com milhões de acessos é distribuída entre várias máquinas para evitar sobrecarga.

## VPN Gateway:

Conecta redes locais a redes do Azure via uma conexão segura. Exemplo: uma empresa que usa uma VPN para permitir que funcionários se conectem de forma segura a recursos internos da empresa no Azure.

## 3. Armazenamento

A categoria Armazenamento fornece diferentes soluções de armazenamento na nuvem para arquivos, bancos de dados, backup e recuperação de desastres.

## Azure Blob Storage:

Armazena grandes quantidades de dados não estruturados, como arquivos de imagem e vídeos. Exemplo: um site de compartilhamento de fotos utiliza o Blob Storage para armazenar imagens dos usuários.

## Azure File Storage:

Armazena arquivos e permite acesso via protocolo SMB. Exemplo: um sistema de arquivos compartilhado que permite a edição colaborativa de documentos entre equipes.

## Disk Storage:

Proporciona discos de armazenamento de alta performance para VMs. Exemplo: um servidor de banco de dados que requer I/O rápido para acessar dados.

## 4. Banco de Dados

Na categoria Banco de Dados, estão os serviços que oferecem bancos de dados relacionais e não relacionais, adequados para diversos tipos de aplicações.

## Azure SQL Database:

Banco de dados relacional compatível com SQL Server. Exemplo: uma empresa de ERP utiliza Azure SQL para gerenciar os dados de seus clientes.

## Azure Cosmos DB:

Banco de dados NoSQL distribuído globalmente, ideal para aplicativos com grande volume de leitura e escrita. Exemplo: um aplicativo de redes sociais que precisa de baixa latência e alta disponibilidade.

## Azure Database for MySQL/PostgreSQL:

 Banco de dados gerenciado para MySQL ou PostgreSQL. Exemplo: uma startup de SaaS utiliza um banco MySQL gerenciado para seus dados, sem se preocupar com a manutenção.


## 5. Inteligência Artificial e Machine Learning

Para projetos de IA e Machine Learning, essa categoria contém ferramentas que permitem treinar e implantar modelos com facilidade.

## Azure Machine Learning:

 Um ambiente para desenvolvimento, treinamento e implantação de modelos de machine learning. Exemplo: uma equipe de cientistas de dados que utiliza o serviço para treinar modelos de previsão de demanda.

## Cognitive Services:

Conjunto de APIs que permite adicionar visão computacional, reconhecimento de voz, linguagem natural e muito mais. Exemplo: um aplicativo que identifica objetos em fotos enviadas pelos usuários.

## Bot Service:

Serviço para criar bots de chat. Exemplo: um bot de atendimento ao cliente que responde dúvidas sobre produtos.


## 6. Desenvolvimento e Integração

Esta categoria ajuda desenvolvedores a criar, integrar e implantar aplicativos de forma contínua e automatizada.

## Azure DevOps:

 Plataforma que oferece ferramentas para CI/CD, gerenciamento de código-fonte e automação de builds e deploys. Exemplo: uma equipe de desenvolvimento que utiliza DevOps para gerenciar o ciclo de vida do software.

## Logic Apps:

Ferramenta para automatização de workflows e integração com outros serviços. Exemplo: automatizar o envio de relatórios por e-mail toda vez que uma nova linha é adicionada em um banco de dados.

## API Management:

Facilita a publicação e gerenciamento de APIs para aplicações. Exemplo: uma empresa que disponibiliza sua API para integração com parceiros e clientes.


## 7. Gerenciamento e Governança

Esta categoria engloba serviços para monitorar, gerenciar custos e garantir a governança dos recursos na nuvem.

## Azure Monitor:

Serviço para monitoramento de aplicações e recursos. Exemplo: monitorar o desempenho de um aplicativo e receber alertas sobre falhas.

## Cost Management:

Ajuda a rastrear e otimizar os custos do Azure. Exemplo: uma empresa que deseja controlar o orçamento alocado para recursos de armazenamento e computação.

## Azure Policy:

Permite definir políticas de conformidade para os recursos. Exemplo: garantir que todas as VMs sejam criadas em regiões específicas para conformidade regulatória.


## 8. Segurança

A categoria Segurança reúne serviços que garantem a proteção dos dados e o acesso seguro aos recursos.

## Azure Security Center:

 Ajuda a monitorar e proteger os recursos no Azure, oferecendo recomendações de segurança. Exemplo: um alerta quando uma vulnerabilidade é detectada em uma VM.

#$ Azure Active Directory (AAD):

Serviço de gerenciamento de identidades, possibilita autenticação e controle de acesso. Exemplo: controle de acesso para aplicativos internos e externos com login único (SSO).

## Key Vault:

Armazena chaves, segredos e certificados de forma segura. Exemplo: armazenamento de segredos, como strings de conexão de banco de dados, para uso seguro em aplicações.

## 9. Internet das Coisas (IoT)

Serviços para dispositivos conectados e ambientes de IoT.

## IoT Hub:

Plataforma que permite a comunicação entre dispositivos IoT e o backend. Exemplo: uma rede de sensores que envia dados de temperatura e umidade para a nuvem.

## Azure Digital Twins:

Cria representações digitais de ambientes físicos. Exemplo: monitorar uma fábrica com sensores e criar um modelo virtual que permite acompanhar a produção em tempo real.


## Conclusão

Essas categorias ajudam a estruturar o ecossistema do Azure, possibilitando que cada usuário encontre facilmente o serviço adequado para suas necessidades específicas, sejam elas focadas em computação, rede, segurança ou inteligência artificial, entre outras. Essa organização é especialmente útil para explorar o potencial do Azure de maneira eficiente e objetiva.


