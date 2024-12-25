# Modelo OSI

![Screenshot_20241225-194724](https://github.com/user-attachments/assets/de5a1955-5c46-495f-a412-18cfae816e9a)


O Modelo OSI (Open Systems Interconnection) é um modelo teórico que descreve como diferentes sistemas de redes se comunicam uns com os outros.

Ele divide essa comunicação em sete camadas que vão desde o hardware físico até o software de aplicação, facilitando a compreensão, padronização e solução de problemas em redes.

## As Sete Camadas do Modelo OSI

### 1. Camada Física

**Função:** Transmite os dados como sinais elétricos, ópticos ou de rádio no meio físico (cabos, fibras ópticas, ar).

**Exemplos:**
- Cabo Ethernet
- Modem DSL
- Bluetooth

**Ataques:**
- Cortar ou manipular fisicamente o cabo de rede
- Jamming (interferência de sinais)

### 2. Camada de Enlace de Dados (Data Link)

**Função:** Garante a transferência de dados livre de erros entre dois dispositivos diretamente conectados. Usa endereços MAC (Media Access Control).

**Exemplos:**
- Switches de rede
- Protocolo Ethernet

**Ataques:**
- Spoofing de MAC Address: Um invasor imita o endereço MAC de outro dispositivo
- Ataques ARP Poisoning (envenenamento de cache ARP)

### 3. Camada de Rede (Network)

**Função:** Define como os dados são roteados de um dispositivo para outro por diferentes redes. Trabalha com endereços IP.

**Exemplos:**
- Roteadores
- Protocolo IP (IPv4 e IPv6)

**Ataques:**
- IP Spoofing: Usar um endereço IP falso
- Ataques de roteamento, como redirecionamento de tráfego malicioso

### 4. Camada de Transporte (Transport)

**Função:** Garante a entrega confiável e ordenada de dados entre sistemas. Utiliza protocolos como TCP e UDP.

**Exemplos:**
- Protocolo TCP (orientado à conexão, confiável)
- Protocolo UDP (não orientado à conexão, rápido, mas menos confiável)

**Ataques:**
- Ataques DoS (Denial of Service): Enviar tráfego massivo para sobrecarregar um serviço
- TCP SYN Flooding: Exploração da conexão inicial do TCP

### 5. Camada de Sessão (Session)

**Função:** Gerencia, estabelece e termina conexões entre dois dispositivos.

**Exemplos:**
- Protocolos NetBIOS e RPC
- Gerenciamento de sessões HTTPS em servidores web

**Ataques:**
- Session Hijacking: Sequestrar sessões autenticadas
- Exploração de vulnerabilidades em protocolos de gerenciamento de sessão

### 6. Camada de Apresentação (Presentation)

**Função:** Tradução e formatação de dados para que possam ser lidos pela aplicação (por exemplo, codificação/decodificação).

**Exemplos:**
- SSL/TLS (encriptação de dados)
- Formatos de arquivos como JPEG, MP3, ou JSON

**Ataques:**
- Exploração de falhas em implementações SSL/TLS, como ataques Man-in-the-Middle (MITM)

### 7. Camada de Aplicação (Application)

**Função:** Interage diretamente com os usuários e fornece serviços como e-mails, navegação web e transferência de arquivos.

**Exemplos:**
- HTTP/HTTPS (navegação web)
- SMTP (e-mail)
- FTP (transferência de arquivos)

**Ataques:**
- Injeção de SQL (manipulação de dados em aplicações web)
- Exploração de vulnerabilidades em software como navegadores ou servidores web

## Resumo e Relação com Cibersegurança

Cada camada do modelo OSI apresenta potenciais riscos e pontos de vulnerabilidade que podem ser explorados por hackers.

A cibersegurança atua em todas essas camadas para:
- Monitorar tráfego
- Identificar anomalias
- Garantir encriptação e autenticação

## Exemplo Prático

Imagine que você está acessando um site bancário:

1. **Camada Física:** Os dados viajam pelos cabos de rede até o roteador
2. **Camada de Enlace:** Seu computador utiliza o endereço MAC para se comunicar com o roteador
3. **Camada de Rede:** Os pacotes de dados são roteados até o servidor do banco utilizando endereços IP
4. **Camada de Transporte:** O protocolo TCP garante que os pacotes cheguem de forma ordenada
5. **Camada de Sessão:** Uma sessão é estabelecida entre o cliente e o servidor
6. **Camada de Apresentação:** Os dados sensíveis, como credenciais, são criptografados com SSL/TLS
7. **Camada de Aplicação:** Você vê a página web no navegador e realiza transações

Ao proteger cada camada, mitigamos os riscos de ataques, como o roubo de dados financeiros ou manipulação de tráfego.
