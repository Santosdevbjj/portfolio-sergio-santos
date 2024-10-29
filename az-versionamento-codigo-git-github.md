## Versionamento de código

![Screenshot_20241029-001305](https://github.com/user-attachments/assets/2de0e887-e30c-444c-a6b2-c80cc8f4933a)


Um conhecimento paralelo às linguagens de programação, mas muito importante para o trabalho do desenvolvedor, é o versionamento de código. Como o nome sugere, é o conhecimento em versionar e salvar versões de uma aplicação. 

Resumindo dessa maneira, parece algo comum, como salvar vários arquivos com versões diferentes. Porém, na prática, o versionamento de código é algo ainda mais organizado e ágil 一 e um pouco mais complexo de ser feito. 

Veja tudo o que você precisa saber sobre o versionamento de código e quais ferramentas são as mais importantes para isso! 

## O que é versionamento de código?

O versionamento é o processo de criar novas versões de um código toda vez que existir uma mudança significativa nele.

De maneira geral, todo projeto de desenvolvimento é feito por etapas, sendo que as funcionalidades são incrementadas aos poucos. Por isso, é preciso criar versões que possam ser retomadas sempre que necessário. 

Em outras palavras, o versionamento de código é como ter vários arquivos, sendo que cada um conta com melhorias em comparação com o anterior. 

Porém, em vez de ter que salvar muitos arquivos (o que é inviável para a computação e para a organização), são feitas essas versões, direto no código.  

Assim, enquanto o código está sendo desenvolvido, o programador vai criando as versões conforme melhora, muda ou implementa algo. Depois, é possível voltar às versões anteriores caso seja necessário. 

Por conta disso, o versionamento de código faz parte das boas práticas de programação e se torna importante para a organização do projeto, consegue contribuir com o trabalho em equipe e também criar um “backup” de todas as mudanças. 

## Como fazer o versionamento?

O versionamento de código é feito durante o processo de construção de código, utilizando o terminal da IDE (ambiente de desenvolvimento integrado, onde se escreve o código) escolhida ou o terminal da própria máquina, dependendo da necessidade e da etapa do processo. 

Para fazer o versionamento, são utilizadas ferramentas específicas para isso, chamadas de sistema de controle de versão. O Git é a mais conhecida, contando com várias funcionalidades que auxiliam nessa organização. Mas também existem outras, como SVN e CVS.  

No caso do Git, ele precisa ser instalado e configurado na sua máquina para funcionar localmente. Não tem uma interface visual, originalmente, por isso a necessidade de utilizar o terminal para criar suas versões.  

Assim, para conseguir fazer o versionamento de código é preciso conhecer os comandos do terminal, que criam os repositórios, os commits e revertem as versões. Nos próximos tópicos você confere os principais comandos do Git e como utilizá-los.  

Além disso, o próprio versionamento também é feito em etapas, pois considera tanto o repositório local quanto um remoto. Assim, o Git tem a função de contribuir com a organização do código e também por enviá-lo para um repositório remoto.  

## O que é Git?

Como vimos, o Git é a ferramenta de controle de versões mais completa, popular e utilizada no mundo da programação. Com ela, é possível criar versões detalhadas, além de outras funções presentes que são úteis no dia a dia. 

É uma ferramenta tão importante que muitas empresas incluem o conhecimento em Git e versionamento de código como pré-requisito para vagas em desenvolvimento. 

O Git funciona localmente, ou seja, na máquina do programador e organiza o código e suas versões enquanto o desenvolvimento está sendo feito. Assim, oferece diferentes ferramentas e ações que o programador utiliza para tornar suas versões mais organizadas.   

Depois, é possível subir toda essa organização para um repositório remoto, o que é bastante comum no dia a dia empresarial. Isso porque, na prática, são vários programadores mexendo no mesmo código, cada um em sua máquina. Depois, reúne-se tudo remotamente. 

## O que é Github?

Muita gente acha que Git e Github são a mesma coisa, mas não são. O Github é uma ferramenta para reunir repositórios de forma remota. A partir do Git é possível enviar as alterações do código direto para o Github. 

Ou seja, o Github funciona como um local remoto para armazenar o código e suas versões. Assim, é muito utilizado em equipes, já que todos conseguem enviar o que for feito remotamente e reunir tudo em um mesmo repositório remoto do Github. 

É uma ferramenta muito utilizada pois sua organização é igual ao do Git. Ou seja, também mostra o código principal, as branches (entenda a seguir o que são), as versões numeradas conforme o Git, entre outras funções.  

Também é visto como uma interface visual do Git, já que mostra as branches e outros detalhes de maneira mais simplificada do que no terminal. Na prática, é como “salvar” sua versão na nuvem. 

Por reunir os repositórios de um programador, o Github se tornou também uma rede social e um portfólio, já que os repositórios públicos podem ser acessados pelas pessoas. Por isso, é interessante que todo programador tenha um Github e treine o versionamento do código com ele. 

No mercado, nem sempre a empresa utiliza o Github como repositório remoto, já que existem outras ferramentas focadas em empresas, que não podem colocar seus códigos de maneira pública ou precisam de alguma proteção a mais. Alguns exemplos são GitLab, BitBucket, SourceForge, Launchpad e Apache Allura. Porém, a lógica do funcionamento é a mesma.   

 ## Conheça os principais comandos Git
 
No dia a dia do trabalho do programador os comandos são utilizados com muito frequência. Veja, a seguir, os principais comandos do Git para fazer seu versionamento. 

## Git init 
Se você deseja começar um novo projeto e repositório, o comando é o de iniciar, em que você cria um projeto em sua máquina e, posteriormente, se quiser, envia para um repositório remoto. 

## git init nome do repositório 

## Git clone
É um comando feito no terminal e que clona um repositório remoto para sua máquina. Por exemplo, você tem um repositório no Github e deseja alterar algo nele. Para isso, você o clona em alguma pasta do seu computador. 

## git clone link do repositório 
## Git pull
Quando você tem um repositório remoto e deseja alterá-lo, é preciso primeiro trazer as alterações mais recentes para sua máquina. 

É diferente do Git Clone, pois é utilizado quando o repositório remoto já está clonado na máquina e você irá continuar trabalhando nele. Ou seja, depois dos momentos iniciais do projeto. 

Ao escrever o comando Git Pull no terminal (Bash), você “puxa” todas as alterações feitas no repositório remoto e suas branches, considerando todos que trabalharam no código. 

## git pull nome do repositório remoto 
## Git branch
As branches são ramificações de um código principal, que podem ser criadas pelos desenvolvedores que irão mexer naquele projeto. Utilizar as branches permite que mais de uma pessoa trabalhe em paralelo em um mesmo projeto. 

Depois, o que foi feito é verificado e aceito pela pessoa responsável, geralmente o líder do projeto. O próprio Git consegue organizar e mostrar as mudanças feitas. No próximo tópico, você irá entender como entrar no repositório antes de criar a branch. 

## git branch nome da branch (cria a branch)

## git branch -d nome da branch (deleta a branch) 

## git push -u local remoto nome da branch (manda a branch para o repositório remoto)

## git branch –list (para ver as branches)

## Git checkout
É o comando utilizado para entrar na branch que você quer trabalhar e atualizar. Muito útil tanto para entrar em sua branch quanto para trocar de branch no meio do processo.

Antes de mudar de branch, dê o commit (veremos a seguir) para salvar as alterações. Depois faça a troca. 

## git checkout nome-da-branch 

## Git status
Mostra os status dos arquivos, ou seja, quais foram modificados, quais não foram, o que foi criado ou deletado. 

Também mostra seu estágio, por exemplo, se já foi feito commit, se está salvo no local, entre outras informações. É muito utilizado no dia a dia.  

## Git add
Adiciona as alterações que foram feitas para ser feito o commit (salvamento). Basicamente, as alterações, quando feitas, não estão sendo “acompanhadas” pelo Git (o que pode ser visto pelo Git Status, as alterações não acompanhadas ficam em vermelho). 

Para que o Git “perceba” essas alterações, é preciso adicioná-las e, só depois, fazer o commit. Aqui, você consegue adicionar e “commitar” todas as alterações de uma só vez ou separadamente, adicionando arquivo por arquivo. 

## git add nome do arquivo

## git add . (todas as alterações)

## Git commit
É o comando mais utilizado e também um dos mais importantes. É o commit que salva as alterações feitas, ou seja, cria uma versão daquele código.

O ideal é que o commit seja utilizado durante a produção do código. Toda vez que você fizer uma mudança significativa no código, que esteja dando certo, dê um commit. 

Assim, você pode mexer no código com mais tranquilidade pois, mesmo se der algo errado, alguma versão anterior estará correta. É só voltar para ela, seja qual for o qualquer motivo. 

Na hora de fazer o commit, também é preciso escrever um comentário, falando o que foi feito naquela alteração. Precisa ser algo direto e específico, pois é com essa mensagem que você consegue reconhecer os commits depois. 

## git commit -m “mensagem do commit“ 

## Git revert
É o comando utilizado para voltar a versões antigas ou desfazer uma alteração, ou seja, voltar para a versão anterior. 

Por isso, também é um dos mais importantes do Git. Afinal, é por essa possibilidade que o versionamento existe. É um comando que exige atenção, pois mexe diretamente com todas as versões, podendo levar a exclusão caso seja colocado o código errado.  

Antes de tudo é preciso ver o histórico de versões de commits daquele código. 

## git log – oneline

Depois, é só colocar o número da versão que deseja desfazer.

## git revert XxXxXxX 

## Git push
Até o momento, tudo isso foi feito em seu repositório local, ou seja, na máquina. Para salvar tudo o que foi feito em um repositório remoto, é preciso utilizar o Git Push. 

Este comando envia, “empurra”, as alterações para o repositório remoto configurado no seu Git. Um dos mais utilizados, sem dúvida, é o GitHub, mas existem outras opções também, como GitLab, BitBucket, entre outros.

## git push nome do repositório nome da branch 



