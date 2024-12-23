# O Protocolo TCP/IP

![Screenshot_20241223-102849](https://github.com/user-attachments/assets/c0150f75-3a19-4e51-91ed-49eaedc01d86)


O protocolo TCP/IP (Transmission Control Protocol/Internet Protocol) é um conjunto de protocolos que formam a base da comunicação na internet e em redes locais. Ele define como os dispositivos se conectam, trocam dados e garantem que essas trocas sejam confiáveis e organizadas.

## Estrutura do TCP/IP

O modelo TCP/IP é composto por 4 camadas, cada uma com funções específicas:

### 1. Camada de Aplicação

Permite que aplicações e serviços acessem a rede.

**Exemplos de protocolos:** HTTP, HTTPS, FTP, SMTP, DNS, SSH.

**Exemplo prático:** Quando você acessa um site, o navegador usa o protocolo HTTP/HTTPS para solicitar as páginas web ao servidor.

### 2. Camada de Transporte

Responsável por garantir a comunicação confiável entre os dispositivos.

**Principais protocolos:**
* TCP (Transmission Control Protocol): Conexão confiável (confirmação de entrega)
* UDP (User Datagram Protocol): Comunicação rápida, sem garantia de entrega

**Exemplo prático:** Durante uma videoconferência (como no Zoom), o UDP é usado para priorizar a velocidade, mesmo que alguns pacotes sejam perdidos.

### 3. Camada de Rede (ou Internet)

Determina a melhor rota para os dados viajarem entre o emissor e o receptor.

**Protocolo principal:** IP (Internet Protocol)

**Exemplo prático:** Quando você envia um e-mail, o IP escolhe a rota pela qual ele chegará ao servidor do destinatário.

### 4. Camada de Acesso à Rede (ou Física)

Trata da transmissão dos dados pelos meios físicos (cabos, Wi-Fi, etc.).

**Protocolos:** Ethernet e Wi-Fi

**Exemplo prático:** O cabo Ethernet ou a rede Wi-Fi transporta os dados de um computador até o roteador.

## Principais Protocolos

### TCP (Transmission Control Protocol)

Protocolo confiável que garante a entrega dos dados na ordem correta.

**Realiza a transmissão em três etapas:**

1. Estabelecimento de conexão (Three-Way Handshake):
   * O cliente envia um pacote SYN
   * O servidor responde com um pacote SYN-ACK
   * O cliente confirma com um ACK

2. Transferência de dados:
   * Os pacotes são numerados e confirmados

3. Encerramento da conexão:
   * Ambos os lados concordam em encerrar a comunicação

**Exemplo prático:** Uma transferência de arquivo via FTP usa TCP para garantir que o arquivo seja entregue corretamente.

### IP (Internet Protocol)

* Define os endereços IP (v4 ou v6) e controla o roteamento dos pacotes
* Não garante a entrega (por isso depende do TCP ou UDP)
* Cada dispositivo conectado tem um endereço IP único

**Exemplo prático:**
* O endereço IPv4 pode ser algo como 192.168.1.1
* O IPv6 é mais longo, como 2001:0db8:85a3:0000:0000:8a2e:0370:7334

### UDP (User Datagram Protocol)

* Alternativa ao TCP, é mais rápido, mas não confiável
* Usado em aplicações onde a velocidade é mais importante que a precisão

**Exemplo prático:** Serviços de streaming de vídeo (como Netflix) ou jogos online usam UDP.

### DNS (Domain Name System)

* Converte nomes de domínio (como www.google.com) em endereços IP

**Exemplo prático:** Quando você digita "www.google.com" no navegador, o DNS encontra o IP do servidor para conectar.

## Funcionamento de uma Comunicação

### Cenário: Acessando um site (www.google.com)

1. **Camada de Aplicação:** O navegador usa HTTP para solicitar a página
2. **Camada de Transporte:** O TCP divide os dados em pacotes, garantindo a ordem correta
3. **Camada de Rede:** O IP define a melhor rota para os pacotes alcançarem o servidor
4. **Camada de Acesso:** A rede Wi-Fi ou cabo Ethernet transporta os dados fisicamente

### Exemplo Prático: Download de Arquivo

1. **Solicitação:** O cliente usa o protocolo FTP para pedir o arquivo

2. **Divisão:** O TCP divide o arquivo em pacotes

3. **Envio:** O IP roteia os pacotes pela internet

4. **Recebimento:** O TCP confirma a entrega e reordena os pacotes

5. **Entrega:** O FTP conclui o download 


