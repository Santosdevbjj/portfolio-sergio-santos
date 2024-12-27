## Aprendendo sobre Windows 10, 11, Windows Server 2019/2022.

![Screenshot_20241226-220918](https://github.com/user-attachments/assets/aa4458b2-6c17-49e7-ab45-df27d6d66e5c)


O Windows é um dos sistemas operacionais mais populares do mundo, desenvolvido pela Microsoft.

Ele oferece uma ampla gama de recursos para usuários domésticos, corporativos e especializados, como profissionais de TI e cibersegurança.

Vamos explorar o sistema operacional em detalhes com foco em cibersegurança, incluindo as versões, comandos, uso em redes, internet, nuvem, PowerShell e configurações especiais.


# 1. Visão Geral das Versões do Windows

# 1.1. Versões Principais

**1. Windows XP (2001):** Amplamente usado, mas inseguro para padrões modernos.


**2. Windows 7 (2009):** Estável, com suporte encerrado em 2020.


**3. Windows 10 (2015):** Focado em segurança e integração com a nuvem.


**4. Windows 11 (2021):** Última versão, com foco em produtividade e segurança avançada.


Nota: As versões de servidor, como **Windows Server 2019/2022**, oferecem recursos adicionais para gerenciar redes corporativas e servidores.


## 2. Recursos de Segurança no Windows

## 2.1. Recursos Embutidos

**1. Windows Defender:** Antivírus integrado para proteger contra malware e spyware.


**2. BitLocker:** Criptografia de disco para proteger dados em dispositivos roubados ou perdidos.


**3. Windows Sandbox:** Ambiente isolado para executar aplicativos suspeitos.


**4. Controle de Conta de Usuário (UAC):** Protege contra alterações não autorizadas no sistema.


**5. Firewall do Windows:** Bloqueia conexões não autorizadas.


## 2.2. Ferramentas Avançadas

**Event Viewer:** Monitora logs de eventos.

**Windows Security Baseline:** Conjunto de políticas de segurança recomendado pela Microsoft.

**Group Policy (GPO):** Gerencia configurações de segurança em redes corporativas.


## 3. Principais Comandos para Cibersegurança

# 3.1. Comandos do Prompt (CMD)

# 1. Ver informações de rede:

**ipconfig:** Exibe a configuração de rede.

**ping:** Verifica a conectividade com um host.

**tracert:** Rastreia o caminho de pacotes até um host.

**netstat:** Mostra conexões de rede ativas.

**arp -a:** Lista a tabela ARP.


## 2. Gerenciamento de usuários:

**net user:** Adiciona ou modifica contas de usuários.

**net localgroup:** Gerencia grupos locais.


## 3. Segurança:

**cipher /w:C:** Apaga dados permanentemente.

**tasklist e taskkill:** Lista e encerra processos.



## 3.2. Comandos no PowerShell

## 1. Auditoria de Sistema:

Get-EventLog -LogName Security -Newest 10

Exibe os 10 eventos mais recentes do log de segurança.


## 2. Gerenciar Firewalls:

Get-NetFirewallRule | Where-Object { $_.Enabled -eq "True" }

Lista regras de firewall ativas.


## 3. Varredura de Arquivos Maliciosos:

Start-MpScan -ScanType QuickScan

Realiza uma varredura rápida usando o Windows Defender.



## 4. Uso em Rede

## 4.1. Configuração de Rede

**Definição de IP estático:** Configure IPs manualmente para maior controle.

**Active Directory (AD):** Gerenciamento centralizado de usuários e dispositivos em redes corporativas.

**Group Policy:** Impõe políticas de segurança em dispositivos conectados à rede.


## 4.2. Diagnóstico

## Ferramentas de Rede:

**Wireshark:**  Análise de pacotes.

**netsh:** Configurações de rede avançadas.


## 5. Internet e Navegação Segura

**Microsoft Edge:**  Navegador integrado com proteção contra phishing e sites maliciosos.

## Configurações DNS:

Use DNS seguros como o Google Public DNS (8.8.8.8) ou Cloudflare (1.1.1.1).


## VPN no Windows:

Configure VPNs para proteger conexões, especialmente em redes públicas.


## 6. Integração com a Nuvem

## 6.1. Microsoft Azure

**Azure Active Directory:**  Gerenciamento de identidades na nuvem.

**Windows Virtual Desktop:** Virtualização do Windows na nuvem.

## Backup e Recuperação:

Use o OneDrive para backup de dados importantes.



## 6.2. Sincronização

O Windows 10/11 sincroniza configurações e arquivos com a nuvem para acesso seguro em vários dispositivos.


## 7. PowerShell e Automação

O PowerShell é uma ferramenta poderosa para automação, com suporte para scripts avançados.


**Exemplo:** Bloquear um IP com firewall:

New-NetFirewallRule -DisplayName "Bloquear IP Malicioso" -Direction Inbound -Action Block -RemoteAddress 192.168.1.100


## 8. Configurações Especiais para Segurança

# 8.1. Configurações de Política

Configure o GPO para restringir aplicativos não confiáveis.

Ative o Windows Defender Credential Guard para proteger credenciais.


# 8.2. Proteção de Dados

Habilite o BitLocker para criptografar discos rígidos.

Use o Controlled Folder Access para proteger pastas críticas.


# Vamos detalhar os aspectos mais práticos do Windows 10, Windows 11, e o PowerShell, incluindo tutoriais básicos e avançados.

# A abordagem é focada no uso cotidiano e em aplicações relacionadas à cibersegurança.



# 1. Introdução ao Windows 10 e Windows 11

# 1.1. Semelhanças e Diferenças

## Windows 10:

Interface mais personalizável.

Suporte prolongado para uso corporativo.

Compatibilidade com hardware mais antigo.


## Windows 11:

Interface mais moderna e simplificada.

Requisitos de hardware mais rigorosos (ex.: TPM 2.0).

Melhor integração com a Microsoft Store e aplicativos Android.


# 1.2. Ferramentas de Segurança Essenciais

# Ambos incluem:

**1. Windows Defender:** Antivírus e proteção contra ameaças.


**2. Firewall do Windows:** Bloqueio de conexões maliciosas.


**3. BitLocker:** Criptografia de disco para segurança de dados.

**4. Sandbox (somente Pro e Enterprise):** Executa aplicativos suspeitos em ambiente isolado.



# 2. Configurações Básicas e Avançadas

# 2.1. Atalhos e Configurações Básicas

Windows + I: Abre as configurações.

Windows + R: Executa comandos.


# Alterar Configurações de Rede

1. Vá para Configurações > Rede e Internet.


2. Escolha entre Wi-Fi ou Ethernet e clique em Propriedades.


3. Ative o IPv4 manualmente e configure IP estático se necessário.


## Configurar Firewall

1. Acesse o Painel de Controle > Sistema e Segurança > Firewall do Windows.


2. Clique em Configurações Avançadas para criar regras personalizadas.


## 2.2. Segurança com o BitLocker

# Habilitar o BitLocker:

1. Abra o Painel de Controle > Criptografia de Unidade de Disco BitLocker.


2. Escolha a unidade e clique em Ativar BitLocker.


3. Escolha um método de autenticação (senha ou chave USB).


## 3. Introdução ao PowerShell

O PowerShell é uma ferramenta poderosa de automação e gerenciamento em sistemas Windows.

## 3.1. Abrindo o PowerShell

**1. Windows 10/11:** Clique em Iniciar e digite "PowerShell".


## 2. Execute como Administrador para acesso total.



## 3.2. Comandos Básicos do PowerShell

# Navegação pelo Sistema

## Listar arquivos em um diretório:

Get-ChildItem

## Mover para outro diretório:

Set-Location C:\Windows


## Gerenciamento de Processos

## Listar processos ativos:

Get-Process

## Encerrar processo específico:

Stop-Process -Name notepad


## Gerenciamento de Usuários

## Criar um novo usuário local:

New-LocalUser -Name "NovoUsuario" -Password (ConvertTo-SecureString "SenhaForte123" -AsPlainText -Force) -FullName "Usuário Teste"

## Adicionar ao grupo Administradores:

Add-LocalGroupMember -Group "Administradores" -Member "NovoUsuario"



## 3.3. Automação com Scripts

**Os scripts no PowerShell usam a extensão .ps1. Para criar um script básico:**

1. Abra o Bloco de Notas.


2. Escreva o seguinte código:

Write-Host "Bem-vindo ao PowerShell!"


3. Salve como script.ps1.


4. Execute no PowerShell:

.\script.ps1



## 3.4. Comandos Avançados em Cibersegurança

## Auditar Eventos de Segurança

# Listar os últimos 50 eventos de segurança:

Get-EventLog -LogName Security -Newest 50


## Configuração de Firewall

# Bloquear endereço IP:

New-NetFirewallRule -DisplayName "Bloquear IP Malicioso" -Direction Inbound -Action Block -RemoteAddress 192.168.1.100


# Varredura Rápida com Windows Defender

Executar uma verificação rápida:

Start-MpScan -ScanType QuickScan


# 3.5. Automatização com Tarefas Agendadas

Automatize uma tarefa para executar diariamente:

## 1. Crie um script backup.ps1:

Copy-Item -Path "C:\Dados" -Destination "D:\Backup" -Recurse


## 2. Agende a execução no Agendador de Tarefas:

Acesse Painel de Controle > Ferramentas Administrativas > Agendador de Tarefas.

Crie uma nova tarefa e defina a execução do script.



## 4. Tutorial Prático de Cibersegurança no Windows 10/11

# 4.1. Configuração de Proteção com GPO

1. Abra o Editor de Política de Grupo Local:

gpedit.msc no Executar.


# 2. Navegue até:

Configurações do Computador > Políticas > Configurações do Windows > Configurações de Segurança.



# 3. Configure políticas como:

Bloquear execução de programas não autorizados: Ative o AppLocker.



# 4.2. Monitoramento de Atividades

Ative o Auditing para monitorar alterações em arquivos:

AuditPol /Set /Category:"Object Access" /Success:Enable /Failure:Enable



**O Windows Server 2019/2022 é uma das plataformas mais robustas para gerenciamento de redes corporativas e servidores.**

![Screenshot_20241226-221054](https://github.com/user-attachments/assets/234c60a3-419b-4c6d-9b7f-7c89a076bdcb)


Ele oferece ferramentas avançadas para configurar redes, gerenciar usuários, proteger dados e implementar políticas de segurança em ambientes corporativos.

Aqui está uma visão detalhada com tutoriais práticos sobre como gerenciar redes, configurar servidores, usar o PowerShell, habilitar o firewall, implementar antivírus e adotar boas práticas de cibersegurança.


##1. Introdução ao Windows Server 2019/2022

# 1.1. Principais Características

# 1. Gerenciamento de Identidades:

**Active Directory (AD):** Controla usuários, grupos e políticas.

**DNS e DHCP:** Gerencia endereços IP e resolve nomes de domínio.


## 2. Virtualização:

**Hyper-V:** Cria e gerencia máquinas virtuais.


## 3. Armazenamento e Backup:

**Storage Spaces Direct (S2D):** Configuração de armazenamento distribuído.

**Windows Server Backup:** Backup de arquivos e sistemas.


## 4. Segurança:

Windows Defender Advanced Threat Protection (ATP).

**Just Enough Administration (JEA):** Limita privilégios administrativos.


## 2. Configurações Básicas do Servidor

# 2.1. Pré-requisitos

# 1. Instale o Windows Server 2019/2022.


# 2. Acesse o Server Manager (Gerenciador do Servidor) após o login inicial.


# 2.2. Configuração de Rede

# 1. Defina o IP Estático:

Abra o Gerenciador de Servidor > Ferramentas > Configurações de Rede.

Configure um IP estático para o servidor.


## PowerShell:

**New-NetIPAddress -InterfaceAlias "Ethernet"**  -IPAddress 192.168.1.100 -PrefixLength 24 -DefaultGateway 192.168.1.1


## 2. Configuração de DNS:

Configure o DNS para resolver nomes dentro da rede.

**Exemplo:** 192.168.1.10 para o domínio interno empresa.local.


## 2.3. Criar e Configurar um Domínio

1. Abra o Server Manager.

2. Instale a função Active Directory Domain Services (AD DS).

3. Promova o servidor a um Controlador de Domínio:

Escolha o nome do domínio (ex.: empresa.local).



## PowerShell:

Install-WindowsFeature -Name AD-Domain-Services -IncludeManagementTools
Install-ADDSForest -DomainName "empresa.local"


3. Gerenciamento de Redes Corporativas

3.1. Configuração do DHCP

1. Instale o recurso DHCP:

Server Manager > Adicionar Funções e Recursos.


## 2. Configure um escopo:

Intervalo de IPs: 192.168.1.100 - 192.168.1.200.

Máscara de Sub-rede: 255.255.255.0.


## PowerShell:

Add-DhcpServerv4Scope -Name "RedeLocal" -StartRange 192.168.1.100 -EndRange 192.168.1.200 -SubnetMask 255.255.255.0



# 3.2. Configuração do DNS

# 1. Instale o DNS:

Configure zonas primárias e reversas.

Adicione registros A e PTR.


## PowerShell:

Add-DnsServerPrimaryZone -Name "empresa.local" -ZoneType ActiveDirectoryIntegrated
Add-DnsServerResourceRecordA -ZoneName "empresa.local" -Name "servidor" -IPv4Address 192.168.1.100



4. Segurança com Firewall e Antivírus

4.1. Configuração do Firewall

## Habilite o Firewall do Windows:

1. Vá para Ferramentas > Configurações Avançadas do Firewall.


2. Crie regras para bloquear portas não utilizadas.


## PowerShell:

New-NetFirewallRule -DisplayName "Bloquear Porta 23 (Telnet)" -Direction Inbound -Protocol TCP -LocalPort 23 -Action Block



## 4.2. Windows Defender ATP

Configure a Proteção Avançada contra Ameaças:

1. Ative o recurso ATP.


2. Realize varreduras de segurança com o PowerShell.



## Varredura Rápida:

Start-MpScan -ScanType QuickScan

Configurar Proteção de Pastas Controladas:

Set-MpPreference -EnableControlledFolderAccess Enabled



## 5. Uso do PowerShell no Windows Server

# 5.1. Gerenciamento de Usuários

## Criar um Usuário:

New-ADUser -Name "Joao Silva" -SamAccountName "joao.silva" -UserPrincipalName "joao.silva@empresa.local" -Path "OU=Usuarios,DC=empresa,DC=local" -AccountPassword (ConvertTo-SecureString "SenhaForte123" -AsPlainText -Force) -Enabled $true

Adicionar ao Grupo Administradores:

Add-ADGroupMember -Identity "Administradores" -Members "joao.silva"


## 5.2. Monitoramento de Logs

Visualizar os 20 eventos mais recentes:

Get-EventLog -LogName System -Newest 20

Exportar logs de segurança:

Get-WinEvent -LogName Security | Export-Csv "C:\Logs\Seguranca.csv"


## 5.3. Configuração de Scripts Automáticos

# Crie um script para backup:

Copy-Item -Path "C:\Dados" -Destination "\\ServidorBackup\Backup" -Recurse

Agende o script com o Agendador de Tarefas:

1. Vá para Ferramentas Administrativas > Agendador de Tarefas.


2. Crie uma nova tarefa e adicione o script.


6. Cibersegurança no Windows Server

6.1. Just Enough Administration (JEA)

Crie configurações de administração limitada:

New-PSSessionConfigurationFile -SessionType RestrictedRemoteServer -Path "C:\Config\JEA.pssc"
Register-PSSessionConfiguration -Name "JEAConfig" -Path "C:\Config\JEA.pssc"


## 6.2. Monitoramento em Tempo Real

Use o Microsoft Defender for Endpoint para rastrear ataques.

Configure alertas de segurança no Security Compliance Toolkit.


6.3. Configuração de Políticas de Grupo (GPO)

## Configure restrições em:

1. Computador > Configurações > Políticas > Configurações de Segurança.


2. Ative Restrição de Software ou AppLocker para bloquear aplicativos.


Vamos aprofundar nos tópicos de virtualização, scripts avançados no Windows Server 2019/2022, configuração de máquinas virtuais e replicação de dados, incluindo cada etapa detalhada.



## 1. Virtualização no Windows Server com Hyper-V

## 1.1. Introdução ao Hyper-V

O Hyper-V é a tecnologia de virtualização nativa do Windows Server, permitindo a criação e gerenciamento de máquinas virtuais (VMs).

## 1.1.1. Benefícios da Virtualização

Economia de custos ao consolidar servidores.

Melhor utilização de hardware.

Isolamento de aplicações em ambientes distintos.

1.2. Configuração do Hyper-V

1.2.1. Instalação do Hyper-V

1. Acesse o Server Manager.


2. Clique em Adicionar Funções e Recursos.


3. Selecione Hyper-V e prossiga com a instalação.


4. Reinicie o servidor.



## PowerShell:

Install-WindowsFeature -Name Hyper-V -IncludeManagementTools -Restart


1.2.2. Criar uma Máquina Virtual

1. Abra o Gerenciador do Hyper-V.


2. Clique em Novo > Máquina Virtual.


3. Defina as configurações:

**Nome da VM.**

Quantidade de memória (ex.: 4 GB).

Disco virtual (ex.: 40 GB, VHDX).


4. Conecte a máquina virtual à rede.


## PowerShell:

New-VM -Name "ServidorTeste" -MemoryStartupBytes 4GB -Generation 2 -NewVHDPath "C:\VMs\ServidorTeste.vhdx" -NewVHDSizeBytes 40GB -SwitchName "RedeVirtual"


# 1.3. Gerenciamento de Máquinas Virtuais

1.3.1. Iniciar e Parar VMs

Para iniciar uma VM:

Start-VM -Name "ServidorTeste"

Para desligar:

Stop-VM -Name "ServidorTeste"


1.3.2. Exportar e Importar VMs

# Exportar uma VM:

Export-VM -Name "ServidorTeste" -Path "D:\Backup\VMs"

# Importar uma VM:

Import-VM -Path "D:\Backup\VMs\ServidorTeste\ServidorTeste.xml"


2. Scripts Avançados no Windows Server

Scripts são úteis para automatizar tarefas complexas e repetitivas.


2.1. Script para Criar e Configurar VMs

## Salve o seguinte script como CriarVMs.ps1:

# Variáveis
$VMName = "NovaVM"
$VHDPath = "C:\VMs\$VMName.vhdx"
$Memory = 2GB
$DiskSize = 50GB
$SwitchName = "RedeVirtual"

# Criar VM
New-VM -Name $VMName -MemoryStartupBytes $Memory -NewVHDPath $VHDPath -NewVHDSizeBytes $DiskSize -SwitchName $SwitchName

# Configurar Processadores
Set-VMProcessor -VMName $VMName -Count 2

# Iniciar VM
Start-VM -Name $VMName

Write-Host "Máquina Virtual '$VMName' criada e iniciada com sucesso!"

Execute o script no PowerShell:

.\CriarVMs.ps1



## 2.2. Script para Monitorar Uso de CPU

Este script monitora o uso da CPU em tempo real:

Get-Counter "\Processor(_Total)\% Processor Time" -Continuous



## 2.3. Script de Backup e Replicação

Automatize o backup de arquivos e replicação para outro servidor:

# Variáveis
$SourcePath = "C:\Dados"
$DestinationPath = "\\ServidorBackup\Backup"

# Copiar Arquivos
Copy-Item -Path $SourcePath -Destination $DestinationPath -Recurse

Write-Host "Backup concluído!"



3. Tutorial de Replicação de Dados no Hyper-V

O Hyper-V permite configurar replicação de dados para alta disponibilidade.



## 3.1. Configurar o Ambiente de Replicação

1. Pré-requisitos:

Dois servidores com Hyper-V.

Configuração de DNS para ambos os servidores.


## 2. Habilitar a Replicação no Host

Abra o Gerenciador do Hyper-V.

Clique no servidor e acesse Configurações > Configurações de Replicação.

Ative a replicação e defina as permissões.


## PowerShell:

Enable-VMReplication -VMName "ServidorTeste" -ReplicaServerName "ServidorSecundario" -AuthenticationType Kerberos



3.2. Configuração da Máquina Virtual

1. No Gerenciador do Hyper-V, selecione a VM.


## 2. Clique em Configurar Replicação.


3. Siga as etapas para definir o servidor de destino e o agendamento.



## 3.3. Testar a Replicação

1. Forçar a replicação manual:

Start-VMInitialReplication -VMName "ServidorTeste"


2. Verificar o status da replicação:

Get-VMReplication -VMName "ServidorTeste"


## 4. Cibersegurança na Virtualização

4.1. Configuração de Rede Virtual Segura

1. Isolar Redes Virtuais:

Crie switches virtuais separados para diferentes VMs.



## PowerShell:

New-VMSwitch -Name "Isolado" -SwitchType Internal

2. Habilitar Firewall para VMs:

Adicione regras de firewall específicas para proteger o tráfego.



## PowerShell:

New-NetFirewallRule -DisplayName "Permitir RDP VM" -Direction Inbound -Protocol TCP -LocalPort 3389 -Action Allow



4.2. Proteção de Dados

1. Criptografia de Discos Virtuais:

Habilite o BitLocker para discos VHDX.


## 2. Configuração de Snapshots:

Crie checkpoints para recuperação rápida em caso de falhas:

Checkpoint-VM -Name "ServidorTeste" -SnapshotName "Checkpoint1"


## Clustering, Failover e Scripts Avançados no Windows Server 2019/2022

**Clustering e Failover são componentes críticos para alcançar alta disponibilidade e continuidade de negócios em redes corporativas.**

Vamos explorar como configurar, gerenciar e automatizar essas tecnologias no Windows Server 2019/2022, além de fornecer scripts avançados.


## 1. Introdução ao Clustering e Failover

# 1.1. O Que é Clustering?

**O Failover Cluster** é um grupo de servidores interconectados (nós) que trabalham juntos para manter a disponibilidade de serviços e aplicações. Se um nó falhar, outro nó assume automaticamente.


## 1.2. Benefícios do Failover Cluster

**1. Alta Disponibilidade:** Serviços permanecem ativos mesmo em caso de falhas.


**2. Escalabilidade:** Permite adicionar nós para aumentar a capacidade.


**3. Recuperação Rápida:** Reduz o tempo de inatividade.


# 2. Configuração de Failover Cluster

# 2.1. Pré-requisitos

**1. Hardware Compatível:** Certifique-se de que os servidores compartilham acesso a um storage (iSCSI ou Fibre Channel).


## 2. Rede Configurada:

Uma rede dedicada para comunicação entre os nós.

Uma rede para comunicação com o cliente.


# 3. Função de Cluster Instalada.


# Instalar o Cluster no PowerShell:

Install-WindowsFeature -Name Failover-Clustering -IncludeManagementTools


# 2.2. Configurar Storage Compartilhado

# 1. Conectar ao Storage via iSCSI:

Abra o Iniciador iSCSI no Windows.

Configure o alvo (target) do iSCSI.


## PowerShell:

New-IscsiTargetPortal -TargetPortalAddress "192.168.1.10"
Connect-IscsiTarget -NodeAddress "iqn.2023-01.com.storage:target1"

## 2. Configurar o Disco Compartilhado:

Use o Gerenciamento de Disco para inicializar e formatar o disco.



## PowerShell:

Get-Disk | Where-Object IsOffline -eq $true | Set-Disk -IsOffline $false
Initialize-Disk -Number 2 -PartitionStyle GPT
New-Partition -DiskNumber 2 -UseMaximumSize -AssignDriveLetter
Format-Volume -DriveLetter E -FileSystem NTFS



## 2.3. Criar o Failover Cluster

## 1. Validar Configuração:

Abra o Gerenciador de Cluster de Failover.

Execute o assistente de validação para garantir que os servidores estão prontos.


## PowerShell:

Test-Cluster -Node "Servidor1", "Servidor2" -Include "Storage", "Inventory", "Network"

## o 2. Criar o Cluster:

No gerenciador de Cluster, escolha Criar Cluster e siga os passos.


## PowerShell:

New-Cluster -Name "ClusterPrincipal" -Node "Servidor1", "Servidor2" -StaticAddress 192.168.1.20



## 2.4. Configurar um Serviço ou Aplicação

1. Adicione um serviço de alta disponibilidade (ex.: servidor de arquivos):

Clique com o botão direito no cluster e escolha Configurar Função.

Selecione Servidor de Arquivos.


## PowerShell:

Add-ClusterFileServerRole -Cluster "ClusterPrincipal" -Name "FileServerHA" -StaticAddress 192.168.1.21

2. Configure compartilhamentos de arquivos:

New-SmbShare -Name "Arquivos" -Path "E:\Dados" -FullAccess "Administradores"



## 3. Gerenciamento Avançado de Clusters

3.1. Gerenciar Nós do Cluster

Adicionar um Novo Nó:

Add-ClusterNode -Cluster "ClusterPrincipal" -Name "Servidor3"

Remover um Nó:

Remove-ClusterNode -Cluster "ClusterPrincipal" -Name "Servidor2"



## 3.2. Configurar Quórum

O quórum determina quantos nós precisam estar ativos para o cluster operar.

Alterar o Modo de Quórum:

Set-ClusterQuorum -Cluster "ClusterPrincipal" -NodeMajority



## 3.3. Monitorar o Status do Cluster

Verifique o estado dos nós:

Get-ClusterNode

Verifique os recursos ativos:

Get-ClusterResource


## 4. Replicação Avançada com Storage Replica

O Storage Replica permite a replicação de dados entre servidores ou clusters, garantindo proteção contra falhas catastróficas.

4.1. Instalar o Storage Replica

1. No Server Manager, instale a função Storage Replica.


## PowerShell:

Install-WindowsFeature -Name Storage-Replica -IncludeManagementTools


## 4.2. Configurar a Replicação

1. Configure discos dedicados para replicação (um por volume replicado).


2. Crie um grupo de replicação.


## PowerShell:

New-SRPartnership -SourceComputerName "Servidor1" -SourceRGName "GrupoOrigem" -SourceVolumeName "E:" -DestinationComputerName "Servidor2" -DestinationRGName "GrupoDestino" -DestinationVolumeName "E:" -LogVolumeName "F:"



## 4.3. Monitorar a Replicação

Verifique o status da replicação:

Get-SRGroup

Verifique logs de replicação:

Get-SRPartnership


# 5. Scripts Avançados para Clusters e Failover

# 5.1. Script para Monitorar Clusters

# Variáveis
$ClusterName = "ClusterPrincipal"

# Verificar Nós
Get-ClusterNode -Cluster $ClusterName | ForEach-Object {
    Write-Host "Nó: $($_.Name) - Status: $($_.State)"
}

# Verificar Recursos
Get-ClusterResource -Cluster $ClusterName | ForEach-Object {
    Write-Host "Recurso: $($_.Name) - Status: $($_.State)"
}




## 5.2. Script para Failover Manual

# Variáveis
$ResourceName = "FileServerHA"
$TargetNode = "Servidor2"

# Mover Recurso
Move-ClusterGroup -Name $ResourceName -Node $TargetNode

Write-Host "Recurso '$ResourceName' movido para '$TargetNode'."



## 5.3. Script de Replicação Automática

# Variáveis
$SourceServer = "Servidor1"
$DestinationServer = "Servidor2"
$SourceVolume = "E:"
$DestinationVolume = "E:"
$LogVolume = "F:"

# Configurar Replicação
New-SRPartnership -SourceComputerName $SourceServer -SourceRGName "GrupoOrigem" -SourceVolumeName $SourceVolume -DestinationComputerName $DestinationServer -DestinationRGName "GrupoDestino" -DestinationVolumeName $DestinationVolume -LogVolumeName $LogVolume

Write-Host "Replicação configurada com sucesso!"


**Vamos abordar o Windows Server 2022 com foco em Cibersegurança e os principais recursos e práticas recomendadas, incluindo o Secured-Core Server, Trusted Platform Module (TPM) 2.0, Virtualization-Based Security (VBS), HTTPS e TLS 1.3, DNS Seguro, Server Message Block (SMB), e a integração com o Azure.**



## 1. Visão Geral do Windows Server 2022 e Cibersegurança

O Windows Server 2022 foi projetado com foco em segurança avançada, integração com a nuvem e desempenho.

Ele traz melhorias significativas em criptografia, autenticação e proteção contra ameaças, permitindo uma abordagem de "Zero Trust" na segurança de redes corporativas.

## Principais Recursos de Segurança:

**Secured-Core Server:** Proteção contra ameaças avançadas a nível de hardware.

**Trusted Platform Module (TPM) 2.0:** Criptografia baseada em hardware.

**Virtualization-Based Security (VBS):** Isolamento seguro de processos críticos.

**HTTPS e TLS 1.3:** Segurança aprimorada para comunicação de rede.

**DNS Seguro:** Proteção contra ataques de spoofing.

**SMB (Server Message Block):** Novas melhorias para transferência de arquivos segura.


## 2. Secured-Core Server

# 2.1. O Que é Secured-Core Server?

Essa tecnologia combina segurança de hardware, firmware e software para proteger o servidor contra ataques avançados, como malware que opera antes do sistema operacional iniciar.

# Pré-requisitos para Secured-Core Server:

1. Processadores compatíveis, como AMD EPYC ou Intel Xeon de última geração.


2. TPM 2.0 habilitado.


3. Boot Seguro e Virtualization-Based Security (VBS) ativados.


## Habilitar Secured-Core Server:

1. Acesse o Gerenciador do Servidor.


2. Navegue para Configurações de Segurança do Sistema.


3. Ative:

Secure Boot (Boot Seguro).

Device Guard.

Credential Guard.


## PowerShell:

# Habilitar Device Guard e Credential Guard
Enable-WindowsOptionalFeature -Online -FeatureName Windows-Defender-ApplicationGuard


## 3. Trusted Platform Module (TPM) 2.0

# 3.1. O Que é TPM 2.0?

É um chip físico no hardware que protege informações críticas, como chaves de criptografia e autenticação de sistema.

## Verificar TPM no Sistema:

1. No Windows Server, pressione Win + R e digite tpm.msc.


2. Confirme se o status está como Ready for use.


## PowerShell:

Get-WmiObject -Namespace "Root\CIMv2\Security\MicrosoftTpm" -Class Win32_Tpm

## Usos do TPM 2.0:

Proteção de chaves do BitLocker.

Autenticação para sistemas de boot seguro.

Armazenamento seguro de certificados.


## 4. Virtualization-Based Security (VBS)

# 4.1. O Que é VBS?

VBS isola partes críticas do sistema em uma máquina virtual protegida, impedindo que malware ou usuários mal-intencionados acessem dados sensíveis.

## Habilitar VBS no Windows Server 2022:

1. Abra o Editor de Política de Grupo (gpedit.msc).


2. Navegue para Configuração do Computador > Modelos Administrativos > Sistema > Device Guard.


3. Habilite:

Habilitar Virtualization-Based Security.

Configurar a Proteção de Credenciais.



## PowerShell:

# Ativar Virtualization-Based Security
Set-ProcessMitigation -System -Enable VirtualizationBasedSecurity



## 5. HTTPS e TLS 1.3

5.1. Configurar HTTPS e TLS 1.3 no Windows Server

**O protocolo TLS 1.3** oferece melhor segurança e desempenho, sendo obrigatório em ambientes modernos.

## Passo a Passo para Habilitar TLS 1.3:

1. No Editor de Registro (regedit), navegue para:

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols



# 2. Crie uma nova chave chamada TLS 1.3.


# 3. Adicione valores:

**DWORD (32 bits):** Enabled = 1

**DWORD (32 bits):** DisabledByDefault = 0


## PowerShell:

New-Item -Path "HKLM:\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.3" -Force
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.3" -Name "Enabled" -Value 1 -PropertyType "DWord"
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.3" -Name "DisabledByDefault" -Value 0 -PropertyType "DWord"



## 6. DNS Seguro

# 6.1. Implementar DNS Seguro

# 1. Habilitar DNS-over-HTTPS (DoH):

Configuração no servidor DNS ou diretamente no Windows Server.


2. Usar DNSSEC (DNS Security Extensions):

Protege contra falsificação de DNS e ataques de man-in-the-middle.


# PowerShell para Habilitar DNSSEC:

Add-DnsServerSigningKey -ZoneName "example.com" -KeyLength 2048 -KeyStorageProvider "Software"
Set-DnsServerZoneSetting -ZoneName "example.com" -DnsSecEnable


7. Server Message Block (SMB)

7.1. Novidades no SMB


# SMB over QUIC: Transferência de arquivos segura sobre QUIC.

# Melhorias no desempenho e na criptografia.


# Configurar SMB Encryption:

1. Abra o Gerenciador do Servidor.


2. Configure a criptografia de SMB para o compartilhamento de arquivos.


## PowerShell:

Set-SmbServerConfiguration -EncryptData $true


## 8. Conexão com o Azure

## 8.1. Introdução ao Azure Arc

**O Azure Arc** permite gerenciar servidores locais como se fossem recursos do Azure.

## Passos para Conectar o Windows Server ao Azure:

1. Instale o Azure Connected Machine Agent no servidor.


2. Registre o servidor no Azure:

azcmagent connect --resource-group "MyResourceGroup" --subscription-id "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" --location "eastus"



## 8.2. Configurar Backup e Segurança com Azure

1. Habilite o Azure Backup para recuperação de desastres.


2. Configure Azure Security Center para monitoramento de segurança.


**Vamos aprofundar no Azure Backup e no Microsoft Defender for Cloud (antigo Azure Security Center), com detalhes técnicos e exemplos práticos.**



## 1. Azure Backup

# 1.1. O que é Azure Backup?

O Azure Backup é uma solução de backup baseada em nuvem que protege dados e servidores contra falhas, perda de dados e desastres. Ele suporta backups de:

## Servidores Windows e Linux.

# Máquinas virtuais no Azure.

# Banco de dados SQL.

# Dados do SharePoint e do Exchange.



## 1.2. Configuração Prática do Azure Backup

Passo 1: Criar um Cofre dos Serviços de Recuperação

1. Acesse o Azure Portal.

2. Navegue até Todos os Serviços > Backup e Site Recovery > Cofres dos Serviços de Recuperação.


## 3. Clique em Criar:

Nome: CofreBackupEmpresa.

Região: Escolha a mesma do recurso que deseja proteger.


4. Clique em Revisar e Criar e, em seguida, Criar.


## Exemplo no PowerShell:

# Login no Azure
Connect-AzAccount

# Criar um cofre de recuperação
New-AzRecoveryServicesVault -Name "CofreBackupEmpresa" -ResourceGroupName "GrupoRecursos" -Location "East US"



## Passo 2: Configurar o Backup

1. Acesse o cofre criado no Azure Portal.


2. Clique em Backup.


3. Escolha o Tipo de Fonte:

Azure: Para máquinas virtuais no Azure.

No Local: Para servidores físicos ou máquinas virtuais fora do Azure.



## 4. Defina a política de backup:

Frequência: Diária ou semanal.

Retenção: 30 dias, 1 ano, etc.


Exemplo no PowerShell para Backup de Máquina Virtual:

# Associar cofre ao backup da VM
$vault = Get-AzRecoveryServicesVault -Name "CofreBackupEmpresa"
Set-AzRecoveryServicesVaultContext -Vault $vault

# Habilitar backup para uma VM
Enable-AzRecoveryServicesBackupProtection -ResourceGroupName "GrupoRecursos" -Name "MinhaVM" -Policy (Get-AzRecoveryServicesBackupPolicy -WorkloadType AzureVM)



# Passo 3: Restaurar Dados

1. Acesse o cofre no portal.


2. Vá para Itens de Backup > Restaurar.


3. Escolha o ponto de recuperação desejado.


## Exemplo no PowerShell:

# Restaurar uma VM a partir de um ponto de recuperação
Start-AzRecoveryServicesBackupRestoreJob -ResourceGroupName "GrupoRecursos" -VaultName "CofreBackupEmpresa" -ItemName "MinhaVM" -TargetResourceGroupName "NovoGrupoRecursos"



1.3. Monitoramento do Backup

1. Use o Azure Monitor para alertas e relatórios de falhas de backup.


2. Configure notificações para backups incompletos.



## Exemplo no PowerShell:

Get-AzRecoveryServicesBackupJob -VaultName "CofreBackupEmpresa" -Status Failed



## 2. Microsoft Defender for Cloud (Azure Security Center)

# 2.1. O que é Microsoft Defender for Cloud?

O Defender for Cloud oferece monitoramento de segurança para recursos no Azure, locais e até em outras nuvens. Ele avalia a conformidade com normas, detecta vulnerabilidades e recomenda ações para proteger o ambiente.



## 2.2. Habilitar o Defender for Cloud

# Passo 1: Ativar no Azure

1. Acesse o Azure Portal.


2. Navegue para Microsoft Defender for Cloud.


3. No painel de configurações, ative o Defender para:

Máquinas Virtuais.

Contas de Armazenamento.

Bancos de Dados SQL.


## Exemplo no PowerShell:

# Habilitar o Microsoft Defender for Cloud
Enable-AzSecurityContact -Name "seguranca@empresa.com" -NotificationEmailsEnabled $true



## 2.3. Avaliação de Segurança

# Passo 1: Revisar Recomendações

1. No Defender for Cloud, vá para Recomendações.


2. Veja insights sobre configurações incorretas, como:

Máquinas virtuais sem agentes de monitoramento.

## Redes expostas.


## Passo 2: Configurar Alertas

1. Ative notificações para alertas críticos.


2. Integre com ferramentas como Microsoft Sentinel.


## Exemplo no PowerShell:

# Listar recomendações de segurança
Get-AzSecurityRecommendation


2.4. Monitoramento e Alertas

Passo 1: Configurar Políticas de Segurança

1. No portal, acesse Políticas de Segurança.


2. Defina padrões para:

Requisitos de senha.

Controle de portas de rede.


# Exemplo no PowerShell:

# Configurar uma política de segurança para senha
Set-AzSecurityPolicyAssignment -Name "PasswordPolicy" -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/StrongPasswordPolicy"


# Passo 2: Verificar Alertas de Segurança

1. Navegue para Alertas de Segurança.


2. Analise e responda a alertas, como:

Tentativas de login não autorizadas.

Ataques de força bruta.


## Exemplo no PowerShell:

# Obter alertas de segurança
Get-AzSecurityAlert



## 2.5. Defender for Servers

O Defender for Servers adiciona camadas extras de proteção, como:

Integração com o Microsoft Defender Antivirus.

Análise de vulnerabilidades.


Habilitar o Defender for Servers:

1. No Defender for Cloud, ative a camada de servidor.


2. Configure as políticas de proteção.


## Exemplo no PowerShell:

# Habilitar Defender para Servidores
Set-AzSecurityPricing -Name VirtualMachines -PricingTier Standard



# 2.6. Conexão com Ambientes Híbridos

# 1. Instale o Azure Arc para gerenciar servidores locais.


2. Registre máquinas locais no Defender for Cloud.


## Exemplo no PowerShell:

# Conectar servidor local ao Azure Arc
azcmagent connect --resource-group "GrupoRecursos" --subscription-id "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" --location "eastus"







