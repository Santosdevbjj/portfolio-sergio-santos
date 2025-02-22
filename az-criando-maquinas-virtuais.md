## Criar uma máquina virtual

![Screenshot_20241029-121305](https://github.com/user-attachments/assets/5a60ee96-1d6f-470a-b013-031da2ffd8ae)


As máquinas virtuais (VM) do Azure podem ser criadas por meio do Portal do Azure. Esse método fornece uma interface de usuário baseada em navegador para criar as VMS seus recursos relacionados. Esse início rápido mostra como usar o portal do Azure para implantar uma máquina virtual (VM) no Azure que executa o Windows Server 2022 Datacenter. Para ver a VM em ação, você habilita o protocolo RDP na VM e instala o servidor Web do IIS. 

Se você não tiver uma assinatura do Azure, crie uma conta gratuita antes de começar. 

## Criar máquina virtual

Digite máquinas virtuais na pesquisa.

1. Em Serviços, selecione Máquinas virtuais.

2. Na página Máquinas virtuais, clique em Criar e selecione Máquina virtual do Azure.

3. A página Criar uma máquina virtual é aberta.

4. Em Detalhes da instância, insira myVM no Nome da máquina virtual e escolha Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2 na Imagem. Deixe os outros padrões. 


5. Em Conta de administrador, forneça um nome de usuário, como azureuser e uma senha. A senha deve ter no mínimo 12 caracteres e atender a requisitos de complexidade definidos.

6. Em Regras de porta de entrada, escolha Permitir portas selecionadas e, em seguida, selecione RDP (3389) e HTTP (80) na lista suspensa. 

7. Deixe os padrões restantes e, em seguida, selecione o botão Examinar + criar na parte inferior da página. 

8. Após a execução da validação, selecione o botão Criar na parte inferior da página. 

9. Após a conclusão da implantação, selecione Ir para o recurso. 

## Conectar-se à máquina virtual

Inicie uma conexão da área de trabalho remota para a máquina virtual. Estas instruções ensinam a se conectar aàsua VM de um computador com Windows. Em um Mac, você precisa de um cliente RDP, como este Cliente de Área de Trabalho Remota da Mac App Store.

1. Selecione Conectar>RDP na página de visão geral de sua máquina virtual. 

2. Na guia Conectar-se ao RDP, mantenha as opções padrão para se conectar por endereço IP pela porta 3389 e clique em Baixar arquivo RDP. 

3. Abra o arquivo RDP baixado e clique em Conectar quando solicitado. 

4. Na janela Segurança do Windows, selecione Mais opções e Usar uma conta diferente. Digite o nome de usuário como localhost\nome de usuário, insira a senha que você criou para a máquina virtual e clique em OK.  

5. Você pode receber um aviso do certificado durante o processo de logon. Clique em Sim ou em Continuar para criar a conexão.  

## Instalar servidor Web

Para ver a VM em ação, instale o servidor Web do IIS. Abra um prompt do PowerShell na VM e  execute o seguinte comando: 

## Install-WindowsFeature -name Web-Server -IncludeManagementTools 

Quando terminar, feche a conexão RDP com a VM. 

## Exibir a página de boas-vindas do IIS

No portal, selecione a VM e, na visão geral da VM, passe o mouse sobre o endereço IP para mostrar Copiar para área de transferência. Copie o endereço IP e cole-o em uma guia do navegador. A página de boas-vinda do IIS padrão será aberta e deve ter esta aparência:

 ![Screenshot_20241029-115835](https://github.com/user-attachments/assets/8ce07a2e-e794-450b-bb38-f9290d3d835f)


## Limpar os recursos

## Excluir recursos

Quando o grupo de recursos, a máquina virtual e todos os recursos relacionados não forem mais necessários, exclua-os.

1. Na página Visão geral da VM, selecione o link Grupo de recursos.

2. Selecione Excluir grupo de recursos na parte superior da página do grupo de recursos.

3. Uma página abrirá um aviso de que você está prestes a excluir recursos. Digite o nome do grupo de recursos e selecione Excluir para concluir a exclusão dos recursos e do grupo de recursos. 

## Desligamento automático

Se a VM ainda for necessária, o Azure fornecerá um recurso de desligamento automático para máquinas virtuais a fim de ajudar a gerenciar custos e garantir que você não seja cobrado por recursos não utilizados.

1. Na seção Operações da VM, selecione a opção Desligamento automático.

2. Uma página será aberta na qual você poderá configurar o tempo para o desligamento automático.
Selecione a opção Ativado para habilitar e, em seguida, defina uma hora que seja adequada para você.

3. Depois de definir a hora, selecione Salvar na parte superior para habilitar a configuração de Desligamento automático. 

## Observação

Lembre-se de configurar o fuso horário corretamente para corresponder aos seus requisitos, pois o UTC (Tempo Universal Coordenado) é a configuração padrão na lista suspensa de fuso horário. 



