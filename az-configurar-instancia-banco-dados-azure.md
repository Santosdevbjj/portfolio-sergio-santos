Criando uma instância de banco de dados no Azure

Pré-requisitos

Uma assinatura do Azure. Se você não tem uma assinatura do Azure, crie uma conta gratuita

O módulo Az.SQL mais recente para a versão atual do PowerShell ou a versão mais recente da CLI do Azure.


Você pode criar uma implantação de Instância Gerenciada de SQL do Azure usando o portal do Azure, o PowerShell ou a CLI do Azure.

Considere o seguinte:

Cancele o processo de provisionamento por meio do portal do Azure, do PowerShell, da CLI do Azure ou de outras ferramentas usando a API REST.

A implantação da instância será atrasada se for afetada por outras operações na mesma sub-rede, como uma restauração de longa duração ou o dimensionamento de uma instância.

As permissões de leitura para o grupo de recursos são necessárias para ver a instância gerenciada no grupo de recursos.


Importante

A implantação de uma instância gerenciada é uma operação de longa duração. A implantação da primeira instância na sub-rede normalmente demora muito mais do que a implantação em uma sub-rede com instâncias existentes. 

Entre no Portal do Azure

Para criar sua instância no portal do Azure, primeiro você precisará entrar no portal do Azure e preencher as informações na página Criar Instância Gerenciada de SQL do Azure.

Para sua instância, siga estas etapas:

1. Entre no portal do Azure.

2. No menu esquerdo do portal do Azure, selecione SQL do Azure. Se SQL do Azure não estiver na lista, selecione Todos os serviços e, em seguida, digite SQL do Azure na caixa de pesquisa.

3. Selecione + Criar para abrir a página Selecionar opção de implantação do SQL. Veja mais informações sobre a Instância Gerenciada de SQL do Azure selecionando Mostrar detalhes no bloco Instâncias gerenciadas de SQL.

4. Escolha Instância única na lista suspensa e depois selecione Criar para abrir a página Criar instância Gerenciada de SQL do Azure. 



Guia Básico

Preencha as informações obrigatórias exigidas na guia Básico, que é o requisito mínimo para provisionar uma Instância Gerenciada de SQL.

A tabela a seguir fornece detalhes para as informações necessárias na guia Básico: 

<table border="1" style="width: 70%; table-layout: fixed;">
  <tr>
    <th style="width: 30%;">Configuração</th>
    <th style="width: 20%;">Valor sugerido</th>
    <th style="width: 50%;">Descrição</th>
  </tr>
  <tr>
    <td>Assinatura</td>
    <td>Sua assinatura.</td>
    <td>Uma assinatura que concede a você permissão para criar recursos.</td>
  </tr>
  <tr>
    <td>Grupo de recursos</td>
    <td>Um grupo de recursos novo ou existente.</td>
    <td>Para ver os nomes do grupo de recursos válidos, consulte Regras e restrições de nomenclatura.</td>
  </tr>
  <tr>
    <td>Nome da instância gerenciada</td>
    <td>Qualquer nome válido.</td>
    <td>Para ver os nomes válidos, consulte Regras e restrições de nomenclatura.</td>
  </tr>
  <tr>
    <td>Região</td>
    <td>A região na qual você deseja criar a instância gerenciada.</td>
    <td>Para obter mais informações sobre as regiões, confira Regiões do Azure.</td>
  </tr>
  <tr>
    <td>Pertence a um pool de instâncias?</td>
    <td>Selecione Sim para que essa instância seja criada dentro de um pool de instâncias.</td>
    <td></td>
  </tr>
  <tr>
    <td>Método de autenticação</td>
    <td>Usar a autenticação do SQL</td>
    <td>Para fins deste guia de início rápido, use a autenticação SQL. Você também pode optar por usar a autenticação do SQL e do Microsoft Entra.</td>
  </tr>
  <tr>
    <td>Logon de administrador da Instância Gerenciada</td>
    <td>Qualquer nome de usuário válido.</td>
    <td>Para ver os nomes válidos, consulte Regras e restrições de nomenclatura. Não use serveradmin, pois essa é uma função reservada no nível de servidor.</td>
  </tr>
  <tr>
    <td>Senha</td>
    <td>Qualquer senha válida.</td>
    <td>A senha deve ter no mínimo 16 caracteres e atender a requisitos de complexidade definidos.</td>
  </tr>
</table>  


Em Detalhes da instância gerenciada, selecione Configurar instância gerenciada na seção Computação + armazenamento para abrir a página Computação + armazenamento. 


