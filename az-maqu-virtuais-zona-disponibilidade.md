Alguns usuários agora verão a opção de criar VMs em várias zonas.

Criar máquinas virtuais em uma zona de disponibilidade do Azure.

Uso do portal do Azure para criar máquinas virtuais altamente resilientes em zonas de disponibilidade. As zonas de disponibilidade do Azure são locais fisicamente separados em cada região do Azure que são tolerantes a falhas locais. Use zonas de disponibilidade para proteger seus aplicativos e dados contra falhas improváveis do datacenter.


Para usar zonas de disponibilidade, crie as máquinas virtuais em uma região do Azure com suporte.

1. Entre no portal do Azure.

2. Clique em Criar um recurso>Computação>Máquina virtual.

3. Na página Máquinas virtuais, clique em Criar, e em seguida, selecione Máquina virtual. A página Criar uma máquina virtual é aberta.

4. Na guia Básico, em Detalhes do projeto, verifique se a assinatura correta está selecionada e escolha um grupo de recursos existente ou crie um do zero.

5. Em Detalhes da instância, digite um nome para o campo nome da máquina virtual.

6. Em Opções de disponibilidade, deixe o valor padrão da Zona de disponibilidade.

7. Em Zona de disponibilidade, o menu suspenso assume como valor padrão Zona 1. Se você escolher diversas zonas, uma nova VM será criada em cada zona. Por exemplo, se você selecionar todas as três zonas, serão criadas três VMs. Os nomes das VMs serão o nome original inserido, acrescido de -1, -2 e -3, conforme o número de zonas selecionadas. Se quiser, você poderá editar cada um dos nomes padrão das VMs.

8. Conclua o restante da página como de costume. Se você quiser criar um balanceador de carga, vá para a guia Rede, >Balanceamento de carga>Opções de balanceamento de carga. Você pode escolher um balanceador de carga do Azure ou um gateway de aplicativo.

Para um balanceador de carga do Azure:

a. Você pode escolher um balanceador de carga existente ou selecionar Criar um balanceador de carga.

b. Para criar um balanceador de carga, em Nome do balanceador de carga, digite o nome desejado.

c. Selecione o Tipo de balanceador de carga, Público ou Interno.

d. Selecione o Protocolo, TCP ou UDP.

e. Você pode deixar os valores padrão de Porta e a Porta de back-end, ou alterá-los, se necessário. A porta de back-end selecionada será aberta no NSG (Grupo de Segurança de Rede) da VM.

f. Quando terminar, selecione Criar. 


Para um Gateway de Aplicativo:

a. Selecione um gateway de aplicativo existente ou Crie um do zero.

b. Para criar um gateway de aplicativo, digite o nome desejado. O Gateway de Aplicativo pode balancear a carga de vários aplicativos. Considere a possibilidade de dar nome ao Gateway de Aplicativo de acordo com as cargas de trabalho que você deseja balancear, em vez usar um nome vinculado à máquina virtual.

c. Em Regra de roteamento, digite um nome de regra. O nome da regra deve descrever a carga de trabalho que você está balanceando.

d. Para balanceamento de carga HTTP, você pode deixar os padrões e, em seguida, selecionar Criar. Para balanceamento de carga HTTPS, você tem duas opções: 


🔹Carregue um certificado e adicione a senha (o gateway de aplicativo gerencia o armazenamento de certificados). Em nome do certificado, digite um nome amigável.

🔹Use um cofre de chaves (o gateway de aplicativo extrairá um certificado definido de um cofre de chaves definido). Escolha a Identidade gerenciada, o Key Vault e o Certificado. 


Importante

Depois que as VMs e o gateway de aplicativo são implantados, faça logon nas VMs para garantir que o certificado do gateway de aplicativo seja carregado nas VMs ou que o nome de domínio do certificado da VM corresponda ao nome de domínio do gateway de aplicativo. 


Observação

Uma sub-rede separada será definida para o Gateway de Aplicativo após a criação.  


9. Deixe os padrões restantes e, em seguida, selecione o botão Examinar + criar na parte inferior da página.

10. Na página Criar uma máquina virtual, você pode ver os detalhes sobre a VM que você está prestes a criar. Quando estiver pronto, selecione Criar.

11. Se você estiver criando uma VM do Linux e a janela Gerar novo par de chaves for aberta, selecione Baixar chave privada e criar recurso. Seu arquivo de chave será baixado como myKey.pem.

12. Depois que a implantação for concluída, selecione Ir para o recurso. 

Se desejar os benefícios de resiliência de uma Máquina Virtual Zonal e quiser ajuda para selecionar uma zona, você poderá fazer com que o Azure selecione a zona mais adequada para sua implantação. 


Observação

Revise a seção Restrições antes de implantar sua VM usando uma zona selecionada pelo Azure. 


1. Entre no portal do Azure habilitando o recurso.

2. Na guia Básico, em Detalhes do projeto, verifique se a assinatura correta está selecionada e escolha um grupo de recursos existente ou crie um do zero.

3. Em Detalhes da instância, digite um nome para o campo nome da máquina virtual.

4. Para opções de disponibilidade, certifique-se de que a zona de disponibilidade esteja selecionada.

5. Para opções de zona (versão prévia), selecione a zona selecionada pelo Azure. A seleção da zona de disponibilidade agora deve estar esmaecida.

6. Configure o restante da sua máquina virtual normalmente para implantação. 



Restrições

Regiões

A implantação de um VM numa zona selecionada pelo Azure está disponível em todas as regiões zonais, exceto nas seguintes regiões.

🔹BrasilSul

🔹CentralIndia

🔹EastUS

🔹JapanEast

🔹KoreaCentral



Discos

Atualmente, o sistema operacional e os discos de dados existentes não são suportados. O novo tipo de fonte de disco de dados deve ser "nenhum".

Tipos de disco suportados

🔹HDDs Standard (unidades de disco rígido)

🔹SSDs Premium

🔹SSD Premium V2

🔹Discos Ultra

🔹SSD Standard ZRS


Tipos de disco não suportados

🔹LRS de SSD Standard 



Outros recursos

🔹Os IPs públicos existentes não têm suporte para uma zona selecionada pelo Azure. Eles podem ser adicionados após a implantação.

🔹Os novos IPs públicos devem ser redundantes de zona ou usar uma zona selecionada pelo Azure.

🔹Os balanceadores de carga e os gateways de aplicativos devem ser resilientes por zona para serem anexados durante a implantação da VM.

🔹Não há suporte para grupos de posicionamento de proximidade, grupos de reserva de capacidade e Host Dedicado do Azure.

🔹A configuração do Site Recovery não está disponível durante a criação da VM, mas pode ser configurada após a implantação.

