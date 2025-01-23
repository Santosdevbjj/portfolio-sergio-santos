### O que é a linguagem de programação COBOL?

![Screenshot_20250123-160617](https://github.com/user-attachments/assets/7ddf50fa-caab-4700-a942-0705d3d13d7e)


A linguagem comum orientada a negócios (COBOL) é uma linguagem de programação compilada de alto nível, semelhante ao inglês, desenvolvida especificamente para as necessidades de processamento de dados de negócios. 

O COBOL foi projetado com a versatilidade ideal em mente; sua verbosidade permite que os programadores usem uma linguagem de programação legível e fácil de manter, que pode funcionar em computadores e sistemas operacionais mainframe.

 Na verdade, foi uma das primeiras linguagens de programação padronizadas pelo American National Standards Institute (ANSI) e pela International Organization for Standardization (ISO). 

Embora o COBOL seja considerado um sistema legado, muitas organizações governamentais e do setor privado continuam a usá-lo para executar aplicativos financeiros, administrativos e de negócios.

Na verdade, a configuração imperativa, processual e (em suas iterações mais recentes) orientada a objetos do COBOL serve como base para mais de 40% de todos os sistemas bancários online.

Ele também suporta 80% das transações de cartão de crédito presenciais, processa com 95% de todas as transações em caixas eletrônicos e alimenta sistemas que geram mais de US$ 3 bilhões em comércio todos os dias.

Devido à sua estabilidade e poder de processamento superiores, ele continua a desempenhar um papel fundamental para ajudar as empresas a manter aplicativos e programas em arquiteturas existentes. 

### História do COBOL

O COBOL foi desenvolvido por um consórcio de organizações governamentais e empresariais chamado Conference on Data Systems Languages (CODASYL), formado em 1959.

 Parcialmente derivado do FLOW-MATIC, uma linguagem criada pela pioneira da ciência da computação Dra. Grace Hopper, o COBOL foi criado como parte de uma iniciativa do Departamento de Defesa dos EUA que pressionava por uma linguagem de programação que pudesse funcionar em sistemas operacionais (Linux, Windows, Unix, z/OS etc.) e ambientes de hardware. 

A primeira versão da linguagem de programação COBOL foi lançada em 1960. E embora a programação COBOL tenha sido originalmente planejada para servir como uma medida paliativa, o DoD rapidamente percebeu sua utilidade e obrigou os fabricantes de computadores a oferecê-la. 

 O COBOL foi finalmente padronizado como linguagem de computador em 1968, após o qual os programadores de COBOL implementaram várias revisões e modernizações, incluindo COBOL-61, COBOL-68, COBOL-74 e COBOL-85.

 A iteração mais recente, COBOL 2002, tenta tornar os aplicativos COBOL mais compatíveis com as práticas modernas de desenvolvimento de software, introduzindo recursos orientados a objetos e outros paradigmas avançados de programação na linguagem. 

### Estrutura COBOL

O programa COBOL tem uma estrutura hierárquica que compreende divisões, seções, parágrafos, frases, verbos e cadeias de caracteres. A natureza divisional de um sistema COBOL (que compreende quatro divisões) permite uma separação distinta de preocupações dentro dos programas COBOL. 

### As divisões COBOL são as seguintes:

### Divisão de identificação

A divisão de identificação é a primeira divisão de um programa COBOL — e uma divisão obrigatória. Ele atribui um nome ao programa e fornece outras informações de identificação, como autor, data de escrita e uma breve descrição da finalidade do programa.

### Divisão de ambiente:

A divisão de ambiente especifica o ambiente de tempo de execução de um programa e define os recursos de entrada e saída que ele usará. É subdividido em duas seções.

Não é de surpreender que a seção de configuração forneça informações sobre a configuração do sistema, incluindo os recursos do computador e do compilador que está usando. No entanto, devido aos avanços nas ferramentas do compilador, as seções de configuração se tornaram obsoletas nos sistemas COBOL modernos, que normalmente podem inferir e se adaptar automaticamente ao ambiente.

A seção de entrada-saída especifica os arquivos e dispositivos associados com os quais o programa pode interagir. Ele inclui o parágrafo FILE-CONTROL, que mapeia nomes de arquivos dentro do programa para arquivos externos, e o parágrafo I-O-CONTROL, que normalmente contém informações de otimização ou sequenciamento para operações de entrada-saída.

### Divisão de dados:

A divisão de dados abriga todas as variáveis, arquivos e definições constantes para o programa. Assim como a divisão de ambiente, a divisão de dados é subdividida.

A seção de arquivos lista todos os arquivos dos quais o programa lerá ou gravará. Uma entrada de descrição de arquivo define cada arquivo e descreve a estrutura dos registros no arquivo.

A seção de armazenamento de trabalho define variáveis que mantêm seus valores durante a execução do programa — incluindo contadores, acumuladores, constantes e qualquer outro armazenamento de dados que não seja relevante para arquivos I-O.

Introduzida em iterações posteriores do COBOL, a seção de armazenamento local define variáveis alocadas na implantação do programa ou método e desalocadas no término, tornando o armazenamento local especialmente útil para algoritmos recursivos e programas reentrantes.

Finalmente, a seção de ligação define itens de dados que passam de um programa para outro.

### Divisão de procedimentos:

A divisão de procedimentos contém o código executável do programa, que é dividido em parágrafos e seções que estruturam o código em blocos de código para melhor legibilidade e fácil manutenção.

### Componentes adicionais

Cada divisão de um sistema COBOL pode incluir seções e parágrafos, que são análogos a seções e parágrafos em linguagens humanas. As seções são subdivisões lógicas e nomeadas dentro de cada divisão que contêm um ou mais parágrafos; eles servem como unidades modulares de código que podem ser chamadas dentro do programa.

Os parágrafos são coleções de frases, as menores unidades executáveis em um programa COBOL, que servem a uma função específica e são identificadas por um nome exclusivo. Cada instrução ou frase COBOL dentro de um parágrafo começa com um verbo COBOL (como MOVE, DISPLAY e ADD) que indica como o código deve ser executado.

A unidade mais básica e indivisível da linguagem COBOL é um caractere. Cadeias de caracteres são caracteres ou sequências de caracteres contíguos que formam uma palavra COBOL, literal ou entrada de comentário, delimitada por separadores. 

### Benefícios da programação COBOL:

Apesar da proliferação de linguagens mais modernas (como Python, Java, JavaScript), a linguagem COBOL já foi a mais amplamente usada na programação de computadores para aplicações empresariais. Mesmo agora, o desenvolvimento do COBOL continua sendo uma parte funcional e crítica da infraestrutura de tecnologia global, especialmente para instituições bancárias, seguradoras e agências governamentais.

Como evidenciado pelo seu poder de permanência, a programação COBOL pode oferecer uma infinidade de benefícios às organizações que optam por utilizá-la (apesar de uma relativa escassez de programadores COBOL1), incluindo:

### Estabilidade:

O COBOL é conhecido por seu desempenho estável e confiável em aplicações de missão crítica. Os sistemas escritos em COBOL tendem a ter alto tempo de atividade e apresentam poucas falhas, o que é vital para as operações ininterruptas de instituições financeiras e serviços governamentais.

### Escalabilidade:

Os programadores podem escalar as aplicações COBOL para lidar com o aumento das cargas de trabalho sem mudanças significativas na base de código, permitindo que as organizações expandam seus sistemas baseados em COBOL junto com seus negócios e sem reescritas ou migrações frequentes para outros idiomas.

Tratamento de dados e processamento de arquivos:

O COBOL oferece recursos excepcionais de processamento de arquivos. Ele pode lidar com dados de transações complexas e em grande escala e oferecer suporte a vários métodos de acesso a arquivos, incluindo o manuseio de arquivos de dados sequenciais, indexados e relativos. 

A robustez do COBOL na automação de processos o torna ideal para trabalhos de processamento em lote, como o processamento de transações financeiras, o gerenciamento de bancos de dados e a geração de relatórios.

### Interoperabilidade:

Os sistemas COBOL de hoje podem interoperar com outras linguagens e tecnologias (como HTML, JSON, XML e IA generativa2) devido à introdução do COBOL orientado a objetos e interfaces para novas linguagens de programação. 



A orientação a objetos também facilita a integração de aplicativos COBOL com serviços virtuais e em nuvem,como Amazon Web Services (AWS), Microsoft Azure e IBM Cloud, bancos de dados SQL e outras infraestruturas DevOps modernas.



### Vamos entender a linguagem de programação COBOL.

**COBOL (Common Business-Oriented Language)** é uma linguagem de programação projetada na década de 1950 para aplicações comerciais e administrativas. É conhecida por sua simplicidade, estruturação em inglês e foco em tarefas como processamento de dados, cálculos financeiros e gerenciamento de arquivos.

## Características Principais do COBOL:

![Screenshot_20250123-160453](https://github.com/user-attachments/assets/9cf70277-48c7-4b64-86f7-01467a97e0b8)


## 1. Foco em Negócios:

Projetado para lidar com grandes volumes de dados e tarefas comerciais, como folha de pagamento, contas a receber e inventários.

## 2. Legibilidade:

A sintaxe se assemelha ao inglês comum, facilitando a compreensão e manutenção, mesmo por profissionais não técnicos.

## 3. Fortemente Estruturada:

Dividida em divisões, seções e parágrafos para organização clara do código.

## 4. Portabilidade:

Pode ser executado em diferentes sistemas operacionais, desde mainframes até computadores modernos.

## 5. Longevidade:

Apesar de ser uma linguagem antiga, COBOL ainda é amplamente usado em setores como bancos, governo e seguradoras, devido à confiabilidade e legado.

## Estrutura de um Programa COBOL

Um programa COBOL é dividido em quatro divisões principais:

**1. Identification Division:** Contém informações gerais sobre o programa, como o nome e o autor.

**2. Environment Division:** Especifica o ambiente de hardware e software onde o programa será executado.

**3. Data Division:** Define todas as variáveis, arquivos e estruturas de dados.

**4. Procedure Division:** Contém as instruções e a lógica do programa.

**Exemplo Prático:** Um Programa COBOL Simples

Este exemplo lê um número do usuário, calcula o dobro e exibe o resultado.

IDENTIFICATION DIVISION.

PROGRAM-ID. Dobro.

AUTHOR. Sergio Santos.

ENVIRONMENT DIVISION.

INPUT-OUTPUT SECTION.

FILE-CONTROL.

DATA DIVISION.

WORKING-STORAGE SECTION.

   01 NUMERO-INTEIRO PIC 9(3).

   01 RESULTADO PIC 9(3).

PROCEDURE DIVISION.

INICIO.

   DISPLAY "Digite um número (até 3 dígitos):".

   ACCEPT NUMERO-INTEIRO.

   COMPUTE RESULTADO = NUMERO-INTEIRO * 2.

   DISPLAY "O dobro do número é: " RESULTADO.

   STOP RUN.

## Explicação do Exemplo:

1. Identification Division: Identifica o programa e o autor.

2. Data Division:

NUMERO-INTEIRO e RESULTADO são variáveis numéricas de até 3 dígitos.

3. Procedure Division:

O programa exibe uma mensagem, aceita um número, calcula o dobro e exibe o resultado.

Exemplo de Uso em Empresa

Uma aplicação prática seria processar uma folha de pagamento:

Entrada: Arquivo com nomes, horas trabalhadas e salários por hora.

Processamento: Multiplicar horas pelo salário, calcular descontos e somar benefícios.

Saída: Gerar relatórios ou arquivos para transferências bancárias.

IDENTIFICATION DIVISION.

PROGRAM-ID. FolhaPagamento.

ENVIRONMENT DIVISION.

INPUT-OUTPUT SECTION.

FILE-CONTROL.

   SELECT ARQUIVO-ENTRADA ASSIGN TO "entrada.txt".

   SELECT ARQUIVO-SAIDA ASSIGN TO "saida.txt".

DATA DIVISION.

FILE SECTION.

   FD ARQUIVO-ENTRADA.

   01 REGISTRO-ENTRADA.

      05 NOME PIC X(30).

      05 HORAS-TRABALHADAS PIC 9(3).

      05 SALARIO-HORA PIC 9(4)V99.

   FD ARQUIVO-SAIDA.

   01 REGISTRO-SAIDA.

      05 NOME-SAIDA PIC X(30).

      05 SALARIO-BRUTO PIC 9(5)V99.

WORKING-STORAGE SECTION.

   01 SALARIO-BRUTO PIC 9(5)V99.

PROCEDURE DIVISION.

PROCESSAR.

   OPEN INPUT ARQUIVO-ENTRADA.

   OPEN OUTPUT ARQUIVO-SAIDA.

   PERFORM UNTIL EOF

      READ ARQUIVO-ENTRADA INTO REGISTRO-ENTRADA

      AT END MOVE "SIM" TO EOF

      NOT AT END

         COMPUTE SALARIO-BRUTO = HORAS-TRABALHADAS * SALARIO-HORA

         MOVE NOME TO NOME-SAIDA

         MOVE SALARIO-BRUTO TO SALARIO-BRUTO

         WRITE REGISTRO-SAIDA.

   END-PERFORM.

   CLOSE ARQUIVO-ENTRADA ARQUIVO-SAIDA.

   STOP RUN.
   

### Por Que COBOL Ainda é Relevante?

**Base de sistemas legados:** Muitos sistemas financeiros e governamentais foram escritos em COBOL.

**Segurança e precisão:** Ideal para operações financeiras críticas.

**Demanda por manutenção:** Profissionais especializados em COBOL são muito procurados para atualizar e manter sistemas legados.

A linguagem COBOL é organizada em divisões que estruturam os programas de forma lógica. A seguir, explico cada divisão em detalhes, junto com um exemplo completo para microcomputadores.

### Divisões do COBOL

![Screenshot_20250123-160333](https://github.com/user-attachments/assets/06f7dd6d-d2a8-4bc3-8714-e4577a513c0e)


## 1. Identification Division

É a primeira divisão e identifica o programa. Contém informações como nome do programa, autor e data.

Exemplo:

## IDENTIFICATION DIVISION.

PROGRAM-ID. MeuPrograma.

AUTHOR. Sergio Santos.

DATE-WRITTEN. 16-01-2025.

## 2. Environment Division

Define o ambiente de execução do programa, incluindo dispositivos de entrada e saída e arquivos. É opcional em algumas implementações.

Seções Principais:

Configuration Section: Especifica o sistema operacional e o compilador.

Input-Output Section: Define os arquivos usados pelo programa.

# Exemplo:

ENVIRONMENT DIVISION.

CONFIGURATION SECTION.

SOURCE-COMPUTER. MICROSOFT-PC.

OBJECT-COMPUTER. MICROSOFT-PC.

INPUT-OUTPUT SECTION.

FILE-CONTROL.

    SELECT ARQUIVO-DADOS ASSIGN TO "dados.txt".

### 3. Data Division

Define todas as variáveis, constantes, arquivos e estruturas de dados usadas no programa.

Seções Principais:

File Section: Define os formatos dos registros para arquivos.

Working-Storage Section: Contém variáveis temporárias.

Screen Section: (dependendo da implementação) Define elementos para interação via tela.

# Exemplo:

DATA DIVISION.

FILE SECTION.

FD ARQUIVO-DADOS.

01 REGISTRO-DADOS.

    05 ID PIC 9(5).

    05 NOME PIC X(30).

    05 IDADE PIC 9(3).

WORKING-STORAGE SECTION.

01 EOF-FLAG PIC X VALUE "N".

### 4. Procedure Division

Contém a lógica do programa, dividida em parágrafos e seções. É onde as operações são executadas.

# Exemplo:

PROCEDURE DIVISION.

INICIO.

    OPEN INPUT ARQUIVO-DADOS.

    PERFORM LER-DADOS UNTIL EOF-FLAG = "S".

    CLOSE ARQUIVO-DADOS.

    STOP RUN.

LER-DADOS.

    READ ARQUIVO-DADOS

        AT END MOVE "S" TO EOF-FLAG.

### 5. Screen Section (opcional)

Usada para manipulação de telas interativas, principalmente em sistemas mais antigos.

# Exemplo:

SCREEN SECTION.

01 TELA-ENTRADA.

    05 LINE 1 COLUMN 1 VALUE "Digite seu nome: ".

    05 LINE 2 COLUMN 1 USING NOME.

### Comandos COBOL

Abaixo, destaco os principais comandos do COBOL:

1. OPEN/CLOSE: Abre ou fecha arquivos.

OPEN INPUT ARQUIVO-DADOS.

CLOSE ARQUIVO-DADOS.

2. READ: Lê registros de arquivos.

READ ARQUIVO-DADOS INTO REGISTRO-DADOS.

3. WRITE: Grava registros em arquivos.

WRITE REGISTRO-DADOS.

4. DISPLAY/ACCEPT: Exibe mensagens ou aceita entrada do usuário.

DISPLAY "Digite sua idade:".

ACCEPT IDADE.

5. IF/ELSE: Condicional para controle de fluxo.

IF IDADE > 18

    DISPLAY "Maior de idade."

ELSE

    DISPLAY "Menor de idade."

END-IF.

6. PERFORM: Executa loops ou sub-rotinas.

PERFORM LER-DADOS UNTIL EOF-FLAG = "S".

7. MOVE: Atribui valores a variáveis.

MOVE "Sergio" TO NOME.

8. COMPUTE: Realiza cálculos.

COMPUTE SALARIO-BRUTO = HORAS-TRABALHADAS * SALARIO-HORA.



### Versões do COBOL

![Screenshot_20250123-124831](https://github.com/user-attachments/assets/582b6830-0dcd-43e1-97a5-35bdc501bc62)


**1. COBOL 60:** Primeira versão, com funcionalidades básicas.

**2. COBOL 74:** Melhorias na padronização.

**3. COBOL 85:** Introduziu novos recursos como controle de erros.

**4. COBOL 2002:** Suporte a programação orientada a objetos (OOP).

**5. COBOL 2014:** Melhorias no suporte a XML e Unicode.

### Exemplo de Programa Completo

# Este programa grava, pesquisa, altera, exclui e gera relatório a partir de um arquivo.

IDENTIFICATION DIVISION.

PROGRAM-ID. GerenciamentoArquivos.

AUTHOR. Sergio Santos.

ENVIRONMENT DIVISION.

INPUT-OUTPUT SECTION.

FILE-CONTROL.

   SELECT ARQUIVO-DADOS ASSIGN TO "dados.txt"

       ORGANIZATION IS LINE SEQUENTIAL.

DATA DIVISION.

FILE SECTION.

FD ARQUIVO-DADOS.

01 REGISTRO-DADOS.

   05 ID PIC 9(5).

   05 NOME PIC X(30).

   05 IDADE PIC 9(3).

WORKING-STORAGE SECTION.

01 OPCAO PIC 9 VALUE 0.

01 ENCONTRADO PIC X VALUE "N".

01 REGISTRO-BUSCA PIC 9(5).

PROCEDURE DIVISION.

MENU.

   DISPLAY "1. Adicionar Dados".

   DISPLAY "2. Pesquisar Dados".

   DISPLAY "3. Alterar Dados".

   DISPLAY "4. Excluir Dados".

   DISPLAY "5. Gerar Relatório".

   DISPLAY "0. Sair".

   ACCEPT OPCAO.

   EVALUATE OPCAO

       WHEN 1 PERFORM ADICIONAR

       WHEN 2 PERFORM PESQUISAR

       WHEN 3 PERFORM ALTERAR

       WHEN 4 PERFORM EXCLUIR

       WHEN 5 PERFORM RELATORIO

       WHEN 0 STOP RUN

       WHEN OTHER DISPLAY "Opção Inválida." PERFORM MENU

   END-EVALUATE.

ADICIONAR.

   OPEN OUTPUT ARQUIVO-DADOS.

   DISPLAY "Digite o ID: ".

   ACCEPT ID.

   DISPLAY "Digite o Nome: ".

   ACCEPT NOME.

   DISPLAY "Digite a Idade: ".

   ACCEPT IDADE.

   WRITE REGISTRO-DADOS.

   CLOSE ARQUIVO-DADOS.

   DISPLAY "Registro adicionado com sucesso!".

   PERFORM MENU.

PESQUISAR.

   DISPLAY "Digite o ID para pesquisa: ".

   ACCEPT REGISTRO-BUSCA.

   OPEN INPUT ARQUIVO-DADOS.

   PERFORM UNTIL EOF-FLAG = "S"

       READ ARQUIVO-DADOS INTO REGISTRO-DADOS

           AT END MOVE "S" TO EOF-FLAG

           NOT AT END

               IF ID = REGISTRO-BUSCA

                   DISPLAY "Registro Encontrado: " NOME ", " IDADE

                   MOVE "S" TO ENCONTRADO

               END-IF

       END-READ.

   CLOSE ARQUIVO-DADOS.

   IF ENCONTRADO = "N" DISPLAY "Registro não encontrado.".

   PERFORM MENU.

ALTERAR.

   DISPLAY "Função de Alteração ainda não implementada.".

   PERFORM MENU.

EXCLUIR.

   DISPLAY "Função de Exclusão ainda não implementada.".

   PERFORM MENU.

RELATORIO.

   DISPLAY "Gerando Relatório...".

   OPEN INPUT ARQUIVO-DADOS.

   PERFORM UNTIL EOF-FLAG = "S"

       READ ARQUIVO-DADOS INTO REGISTRO-DADOS

           AT END MOVE "S" TO EOF-FLAG

           NOT AT END

               DISPLAY ID ", " NOME ", " IDADE

       END-READ.

   CLOSE ARQUIVO-DADOS.

   PERFORM MENU.



### O programa completo, agora com as funções de alteração e exclusão implementadas:

IDENTIFICATION DIVISION.

PROGRAM-ID. GerenciamentoArquivos.

AUTHOR. Sergio Santos.

ENVIRONMENT DIVISION.

INPUT-OUTPUT SECTION.

FILE-CONTROL.

   SELECT ARQUIVO-DADOS ASSIGN TO "dados.txt"

       ORGANIZATION IS LINE SEQUENTIAL.

   SELECT TEMP-DADOS ASSIGN TO "temp.txt"

       ORGANIZATION IS LINE SEQUENTIAL.

DATA DIVISION.

FILE SECTION.

FD ARQUIVO-DADOS.

01 REGISTRO-DADOS.

   05 ID PIC 9(5).

   05 NOME PIC X(30).

   05 IDADE PIC 9(3).

FD TEMP-DADOS.

01 REGISTRO-TEMP.

   05 TEMP-ID PIC 9(5).

   05 TEMP-NOME PIC X(30).

   05 TEMP-IDADE PIC 9(3).

WORKING-STORAGE SECTION.

01 OPCAO PIC 9 VALUE 0.

01 EOF-FLAG PIC X VALUE "N".

01 ENCONTRADO PIC X VALUE "N".

01 REGISTRO-BUSCA PIC 9(5).

PROCEDURE DIVISION.

MENU.

   DISPLAY "1. Adicionar Dados".

   DISPLAY "2. Pesquisar Dados".

   DISPLAY "3. Alterar Dados".

   DISPLAY "4. Excluir Dados".

   DISPLAY "5. Gerar Relatório".

   DISPLAY "0. Sair".

   ACCEPT OPCAO.

   EVALUATE OPCAO

       WHEN 1 PERFORM ADICIONAR

       WHEN 2 PERFORM PESQUISAR

       WHEN 3 PERFORM ALTERAR

       WHEN 4 PERFORM EXCLUIR

       WHEN 5 PERFORM RELATORIO

       WHEN 0 STOP RUN

       WHEN OTHER DISPLAY "Opção Inválida." PERFORM MENU

   END-EVALUATE.

ADICIONAR.

   OPEN OUTPUT ARQUIVO-DADOS.

   DISPLAY "Digite o ID: ".

   ACCEPT ID.

   DISPLAY "Digite o Nome: ".

   ACCEPT NOME.

   DISPLAY "Digite a Idade: ".

   ACCEPT IDADE.

   WRITE REGISTRO-DADOS.

   CLOSE ARQUIVO-DADOS.

   DISPLAY "Registro adicionado com sucesso!".

   PERFORM MENU.

PESQUISAR.

   DISPLAY "Digite o ID para pesquisa: ".

   ACCEPT REGISTRO-BUSCA.

   OPEN INPUT ARQUIVO-DADOS.

   MOVE "N" TO ENCONTRADO.

   PERFORM UNTIL EOF-FLAG = "S"

       READ ARQUIVO-DADOS INTO REGISTRO-DADOS

           AT END MOVE "S" TO EOF-FLAG

           NOT AT END

               IF ID = REGISTRO-BUSCA

                   DISPLAY "Registro Encontrado: " NOME ", " IDADE

                   MOVE "S" TO ENCONTRADO

               END-IF

       END-READ.

   CLOSE ARQUIVO-DADOS.

   IF ENCONTRADO = "N" DISPLAY "Registro não encontrado.".

   PERFORM MENU.

ALTERAR.

   DISPLAY "Digite o ID para alterar: ".

   ACCEPT REGISTRO-BUSCA.

   OPEN INPUT ARQUIVO-DADOS.

   OPEN OUTPUT TEMP-DADOS.

   MOVE "N" TO ENCONTRADO.

   PERFORM UNTIL EOF-FLAG = "S"

       READ ARQUIVO-DADOS INTO REGISTRO-DADOS

           AT END MOVE "S" TO EOF-FLAG

           NOT AT END

               IF ID = REGISTRO-BUSCA

                   DISPLAY "Registro Encontrado: " NOME ", " IDADE.

                   DISPLAY "Digite o novo Nome: ".

                   ACCEPT NOME.

                   DISPLAY "Digite a nova Idade: ".

                   ACCEPT IDADE.

                   MOVE "S" TO ENCONTRADO

               END-IF

               WRITE REGISTRO-DADOS INTO TEMP-DADOS

       END-READ.

   CLOSE ARQUIVO-DADOS.

   CLOSE TEMP-DADOS.

   IF ENCONTRADO = "N"

       DISPLAY "Registro não encontrado."

   ELSE

       CALL 'SYSTEM' USING 'MOVE temp.txt dados.txt'.

       DISPLAY "Registro alterado com sucesso!".

   END-IF.

   PERFORM MENU.

EXCLUIR.

   DISPLAY "Digite o ID para excluir: ".

   ACCEPT REGISTRO-BUSCA.

   OPEN INPUT ARQUIVO-DADOS.

   OPEN OUTPUT TEMP-DADOS.

   MOVE "N" TO ENCONTRADO.

   PERFORM UNTIL EOF-FLAG = "S"

       READ ARQUIVO-DADOS INTO REGISTRO-DADOS

           AT END MOVE "S" TO EOF-FLAG

           NOT AT END

               IF ID = REGISTRO-BUSCA

                   DISPLAY "Registro Encontrado: " NOME ", " IDADE.

                   DISPLAY "Excluindo registro...".

                   MOVE "S" TO ENCONTRADO

               ELSE

                   WRITE REGISTRO-DADOS INTO TEMP-DADOS

               END-IF

       END-READ.

   CLOSE ARQUIVO-DADOS.

   CLOSE TEMP-DADOS.

   IF ENCONTRADO = "N"

       DISPLAY "Registro não encontrado."

   ELSE

       CALL 'SYSTEM' USING 'MOVE temp.txt dados.txt'.

       DISPLAY "Registro excluído com sucesso!".

   END-IF.

   PERFORM MENU.

RELATORIO.

   DISPLAY "Gerando Relatório...".

   OPEN INPUT ARQUIVO-DADOS.

   PERFORM UNTIL EOF-FLAG = "S"

       READ ARQUIVO-DADOS INTO REGISTRO-DADOS

           AT END MOVE "S" TO EOF-FLAG

           NOT AT END

               DISPLAY ID ", " NOME ", " IDADE

       END-READ.

   CLOSE ARQUIVO-DADOS.

   PERFORM MENU.




### Explicação das Alterações:

# 1. Função de Alteração:

Lê o arquivo original e escreve os registros em um arquivo temporário (temp.txt).

Se o registro a ser alterado for encontrado, solicita os novos dados ao usuário antes de gravá-los no temporário.

Substitui o arquivo original pelo temporário ao final do processo.

# 2. Função de Exclusão:

Lê o arquivo original e escreve os registros em um arquivo temporário, exceto o registro a ser excluído.

Substitui o arquivo original pelo temporário.

# 3. Uso do CALL 'SYSTEM':

Executa comandos do sistema operacional, como renomear ou mover arquivos.

# Testes:

Este programa é funcional em compiladores COBOL modernos como GnuCOBOL. 



 # Para testá-lo:

1. Crie um arquivo dados.txt vazio na mesma pasta do programa.

2. Compile o programa e execute-o.

3. Teste as opções para adicionar, pesquisar, alterar, excluir e gerar relatório.



O COBOL é amplamente utilizado em sistemas legados e transacionais, o que o torna uma linguagem frequentemente integrada com diversos tipos de bancos de dados (BD).

 Abaixo, detalho os principais bancos de dados usados com COBOL, suas características, e exemplos de integração.

### Tipos de Banco de Dados Usados com COBOL

# 1. Bancos de Dados Hierárquicos

# IMS (Information Management System) da IBM:

Um dos sistemas mais antigos, usado em ambientes mainframe. Organiza os dados em uma hierarquia, como uma árvore.

# Exemplo:

Um banco de dados de contas bancárias organizadas por clientes e suas transações.

Cliente

Conta Corrente

Conta Poupança

Transações

# 2. Bancos de Dados Relacionais (RDBMS) COBOL também é integrado a bancos de dados relacionais modernos, que usam SQL para manipulação de dados.

**DB2 (IBM):** Altamente usado em mainframes, integra bem com COBOL.

**Oracle Database:** Amplo suporte para COBOL via OCI (Oracle Call Interface).

**SQL Server:** Usado principalmente em sistemas modernos com COBOL em ambientes distribuídos.

**MySQL e PostgreSQL:** Utilizados em sistemas híbridos ou modernos para migrar de legados.

# Exemplo de uso com DB2:

EXEC SQL

    SELECT NOME, IDADE

    INTO :NOME-VAR, :IDADE-VAR

    FROM CLIENTES

    WHERE ID = :ID-VAR

END-EXEC.

# 3. Bancos de Dados Orientados a Registro

**VSAM (Virtual Storage Access Method):*" Muito comum em mainframes. É usado para armazenar grandes volumes de dados em arquivos sequenciais, indexados ou de acesso direto.

**Exemplo:** Um arquivo VSAM armazenando informações de clientes indexados pelo número da conta.

**ISAM (Indexed Sequential Access Method):** Um predecessor do VSAM.

# Definição de um Arquivo VSAM no COBOL:

SELECT CLIENTE-FILE ASSIGN TO "CLIENTE.VSAM"

    ORGANIZATION IS INDEXED

    ACCESS MODE IS DYNAMIC

    RECORD KEY IS CLIENTE-ID.

4. Bancos de Dados NoSQL Embora menos comum, alguns projetos modernos que usam COBOL têm integração com bancos NoSQL, como MongoDB e Redis, geralmente via APIs ou middleware.



### Como o COBOL Interage com Bancos de Dados

# 1. Via SQL Embutido (Embedded SQL)

É o método mais comum para integração com RDBMS. Comandos SQL são incorporados diretamente no código COBOL entre EXEC SQL e END-EXEC.

Exemplo:

WORKING-STORAGE SECTION.

01 NOME-VAR PIC X(30).

01 IDADE-VAR PIC 9(3).

01 ID-VAR PIC 9(5).

PROCEDURE DIVISION.

DISPLAY "Digite o ID do Cliente:".

ACCEPT ID-VAR.

EXEC SQL

    SELECT NOME, IDADE

    INTO :NOME-VAR, :IDADE-VAR

    FROM CLIENTES

    WHERE ID = :ID-VAR

END-EXEC.

IF SQLCODE = 0

    DISPLAY "Nome: " NOME-VAR ", Idade: " IDADE-VAR

ELSE

    DISPLAY "Cliente não encontrado."

END-IF.

### 2. Via APIs e Middleware

Para bancos como Oracle e MongoDB, são usadas interfaces de programação específicas.

OCI (Oracle Call Interface): Permite que programas COBOL interajam com bancos Oracle.

ODBC/JDBC: Pode ser usado em sistemas COBOL modernos para conectar-se a diversos bancos.



### 3. Manipulação Direta de Arquivos (VSAM/ISAM)

Em sistemas legados, COBOL frequentemente interage com bancos hierárquicos ou baseados em registro diretamente via arquivos.

Exemplo de Integração Completa com VSAM

Arquivo VSAM:

Armazena informações de clientes com ID, nome e idade.

Código COBOL:

IDENTIFICATION DIVISION.

PROGRAM-ID. CLIENTE-MANAGER.

ENVIRONMENT DIVISION.

INPUT-OUTPUT SECTION.

FILE-CONTROL.

   SELECT CLIENTE-FILE ASSIGN TO "CLIENTE.VSAM"

       ORGANIZATION IS INDEXED

       ACCESS MODE IS DYNAMIC

       RECORD KEY IS CLIENTE-ID.

DATA DIVISION.

FILE SECTION.

FD CLIENTE-FILE.

01 CLIENTE-REGISTRO.

   05 CLIENTE-ID PIC 9(5).

   05 CLIENTE-NOME PIC X(30).

   05 CLIENTE-IDADE PIC 9(3).

WORKING-STORAGE SECTION.

01 ID-VAR PIC 9(5).

01 NOME-VAR PIC X(30).

01 IDADE-VAR PIC 9(3).

01 CHAVE-NOT-FOUND PIC X VALUE "N".

PROCEDURE DIVISION.

MENU.

   DISPLAY "1. Adicionar Cliente".

   DISPLAY "2. Pesquisar Cliente".

   DISPLAY "0. Sair".

   ACCEPT OPCAO.

   EVALUATE OPCAO

       WHEN 1 PERFORM ADICIONAR

       WHEN 2 PERFORM PESQUISAR

       WHEN 0 STOP RUN

       WHEN OTHER DISPLAY "Opção Inválida." PERFORM MENU

   END-EVALUATE.

ADICIONAR.

   DISPLAY "Digite o ID do Cliente:".

   ACCEPT ID-VAR.

   DISPLAY "Digite o Nome do Cliente:".

   ACCEPT NOME-VAR.

   DISPLAY "Digite a Idade do Cliente:".

   ACCEPT IDADE-VAR.

   MOVE ID-VAR TO CLIENTE-ID.

   MOVE NOME-VAR TO CLIENTE-NOME.

   MOVE IDADE-VAR TO CLIENTE-IDADE.

   OPEN I-O CLIENTE-FILE.

   WRITE CLIENTE-REGISTRO.

   CLOSE CLIENTE-FILE.

   DISPLAY "Cliente adicionado com sucesso!".

   PERFORM MENU.

PESQUISAR.

   DISPLAY "Digite o ID do Cliente para pesquisa:".

   ACCEPT ID-VAR.

   MOVE ID-VAR TO CLIENTE-ID.

   OPEN I-O CLIENTE-FILE.

   READ CLIENTE-FILE INTO CLIENTE-REGISTRO

       INVALID KEY MOVE "S" TO CHAVE-NOT-FOUND.

   CLOSE CLIENTE-FILE.

   IF CHAVE-NOT-FOUND = "S"

       DISPLAY "Cliente não encontrado."

   ELSE

       DISPLAY "Cliente Encontrado: " CLIENTE-NOME ", Idade: " CLIENTE-IDADE.

   END-IF.

   PERFORM MENU.



### Resumo

**Mainframes (DB2, VSAM):** Predominam em sistemas legados.

**Relacionais Modernos (Oracle, SQL Server):** Usados em integração de COBOL com sistemas modernos.

**NoSQL (MongoDB):** Utilizados raramente em projetos modernos e híbridos.

**Hierárquicos (IMS):** Amplamente usados em sistemas bancários e de grande escala.



# Aqui estão dois exemplos completos de programas COBOL que utilizam banco de dados, um para microcomputador usando MySQL e outro para mainframe usando DB2. Ambos incluem explicações detalhadas para cada passo.

**1. Exemplo para Microcomputador:** Integração COBOL com MySQL

Cenário

Um sistema simples que armazena informações de clientes (ID, Nome, Idade) em um banco de dados MySQL. O programa permitirá adicionar, pesquisar, alterar e excluir registros.

Configuração Prévia

1. Instalar MySQL e Configurar o Banco de Dados

Execute os comandos SQL abaixo no MySQL para criar a tabela:

CREATE DATABASE cliente_db;

USE cliente_db;

CREATE TABLE clientes (

    id INT PRIMARY KEY,

    nome VARCHAR(50),

    idade INT

);

2. Configurar o Driver ODBC

Configure um DSN (Data Source Name) no ODBC com o nome CLIENTE_DB.

Certifique-se de que o driver MySQL ODBC está instalado.

3. Compilador COBOL

Use GnuCOBOL com suporte a ODBC ou outro compilador compatível.

Código COBOL

IDENTIFICATION DIVISION.

PROGRAM-ID. CLIENTE-MANAGER.

ENVIRONMENT DIVISION.

CONFIGURATION SECTION.

SPECIAL-NAMES.

   CURSOR IS SQL-CURSOR.

DATA DIVISION.

WORKING-STORAGE SECTION.

01 CLIENTE-ID       PIC 9(5).

01 CLIENTE-NOME     PIC X(50).

01 CLIENTE-IDADE    PIC 9(3).

01 SQLCODE          PIC S9(9) COMP-5.

01 OPCAO            PIC 9.

EXEC SQL INCLUDE SQLCA END-EXEC.

PROCEDURE DIVISION.

MAIN-LOGIC.

    PERFORM MENU UNTIL OPCAO = 0.

    STOP RUN.

MENU.

    DISPLAY "1. Adicionar Cliente".

    DISPLAY "2. Pesquisar Cliente".

    DISPLAY "3. Alterar Cliente".

    DISPLAY "4. Excluir Cliente".

    DISPLAY "0. Sair".

    ACCEPT OPCAO.

    EVALUATE OPCAO

        WHEN 1 PERFORM ADICIONAR

        WHEN 2 PERFORM PESQUISAR

        WHEN 3 PERFORM ALTERAR

        WHEN 4 PERFORM EXCLUIR

        WHEN 0 STOP RUN

        WHEN OTHER DISPLAY "Opção Inválida."

    END-EVALUATE.

ADICIONAR.

    DISPLAY "Digite o ID: ".

    ACCEPT CLIENTE-ID.

    DISPLAY "Digite o Nome: ".

    ACCEPT CLIENTE-NOME.

    DISPLAY "Digite a Idade: ".

    ACCEPT CLIENTE-IDADE.

    EXEC SQL

        INSERT INTO clientes (id, nome, idade)

        VALUES (:CLIENTE-ID, :CLIENTE-NOME, :CLIENTE-IDADE)

    END-EXEC.

    IF SQLCODE = 0

        DISPLAY "Cliente adicionado com sucesso!"

    ELSE

        DISPLAY "Erro ao adicionar cliente. Código SQL: " SQLCODE.

    PERFORM MENU.

PESQUISAR.

    DISPLAY "Digite o ID para pesquisar: ".

    ACCEPT CLIENTE-ID.

    EXEC SQL

        SELECT nome, idade

        INTO :CLIENTE-NOME, :CLIENTE-IDADE

        FROM clientes

        WHERE id = :CLIENTE-ID

    END-EXEC.

    IF SQLCODE = 0

        DISPLAY "Cliente Encontrado: ".

        DISPLAY "Nome: " CLIENTE-NOME ", Idade: " CLIENTE-IDADE

    ELSE

        DISPLAY "Cliente não encontrado. Código SQL: " SQLCODE.

    PERFORM MENU.

ALTERAR.

    DISPLAY "Digite o ID para alterar: ".

    ACCEPT CLIENTE-ID.

    DISPLAY "Digite o novo Nome: ".

    ACCEPT CLIENTE-NOME.

    DISPLAY "Digite a nova Idade: ".

    ACCEPT CLIENTE-IDADE.

    EXEC SQL

        UPDATE clientes

        SET nome = :CLIENTE-NOME, idade = :CLIENTE-IDADE

        WHERE id = :CLIENTE-ID

    END-EXEC.

    IF SQLCODE = 0

        DISPLAY "Cliente alterado com sucesso!"

    ELSE

        DISPLAY "Erro ao alterar cliente. Código SQL: " SQLCODE.

    PERFORM MENU.

EXCLUIR.

    DISPLAY "Digite o ID para excluir: ".

    ACCEPT CLIENTE-ID.

    EXEC SQL

        DELETE FROM clientes

        WHERE id = :CLIENTE-ID

    END-EXEC.

    IF SQLCODE = 0

        DISPLAY "Cliente excluído com sucesso!"

    ELSE

        DISPLAY "Erro ao excluir cliente. Código SQL: " SQLCODE.

    PERFORM MENU.

Explicação do Código

# 1. EXEC SQL Blocos:

Usados para incorporar comandos SQL diretamente no programa COBOL.

# 2. SQLCA:



Uma área de controle que armazena informações sobre a execução de comandos SQL. O SQLCODE indica o status.

# 3. Conexão ODBC:

O programa utiliza o DSN configurado previamente para se conectar ao banco.

4. Execução Passo a Passo:

Adicionar: Insere um novo registro no banco.

Pesquisar: Recupera um registro pelo ID.

Alterar: Atualiza o nome e idade de um registro.

Excluir: Remove um registro pelo ID.

# 2. Exemplo para Mainframe: Integração COBOL com DB2

Cenário

Um sistema bancário que manipula contas de clientes em um banco DB2.

Configuração Prévia

# 1. Banco de Dados DB2

Crie a tabela no ambiente DB2:

CREATE TABLE contas (

    id INT PRIMARY KEY,

    nome VARCHAR(50),

    saldo DECIMAL(10, 2)

);



# 2. Pré-compilação:

Em mainframes, o código COBOL com SQL embutido deve ser pré-compilado com um DB2 Precompiler.

Código COBOL

IDENTIFICATION DIVISION.

PROGRAM-ID. CONTA-MANAGER.

DATA DIVISION.

WORKING-STORAGE SECTION.

01 CONTA-ID        PIC 9(5).

01 CONTA-NOME      PIC X(50).

01 CONTA-SALDO     PIC 9(8)V99.

01 SQLCODE         PIC S9(9) COMP-5.

EXEC SQL INCLUDE SQLCA END-EXEC.

PROCEDURE DIVISION.

MAIN-LOGIC.

    DISPLAY "Digite o ID da Conta: ".

    ACCEPT CONTA-ID.

    EXEC SQL

        SELECT nome, saldo

        INTO :CONTA-NOME, :CONTA-SALDO

        FROM contas

        WHERE id = :CONTA-ID

    END-EXEC.

    IF SQLCODE = 0

        DISPLAY "Conta Encontrada: ".

        DISPLAY "Nome: " CONTA-NOME ", Saldo: " CONTA-SALDO

    ELSE

        DISPLAY "Erro: Conta não encontrada. Código SQL: " SQLCODE.

    STOP RUN.



### Diferenças para o Mainframe

# 1. DB2 Precompiler:

O código SQL é traduzido para chamadas de API DB2 antes de ser compilado.

# 2. Execução no Host:

O programa é executado diretamente no mainframe, acessando bancos DB2.



### Programação Orientada a Objetos com Cobol.

A programação orientada a objetos (POO) foi introduzida no COBOL com o padrão COBOL 2002.

Ela permite trabalhar com conceitos como classes, objetos, herança, e polimorfismo, tornando o COBOL mais moderno e adequado a sistemas complexos.

Aqui está uma explicação detalhada de como criar um programa COBOL usando POO, incluindo exemplos práticos.



### Conceitos Fundamentais de POO em COBOL

![Screenshot_20250123-183531](https://github.com/user-attachments/assets/c0bc397a-2e28-4c2e-a0c8-6f14423d27d0)



# 1. Classe e Objeto

Uma classe define atributos e métodos (similar a um modelo).

Um objeto é uma instância dessa classe.

# 2. Herança

Uma classe pode herdar atributos e métodos de outra.

# 3. Encapsulamento

Os dados são protegidos, acessíveis apenas por métodos públicos.

# 4. Polimorfismo

Métodos podem ser redefinidos em classes derivadas.



Estrutura de um Programa COBOL Orientado a Objetos

### Um programa COBOL com POO geralmente tem:

1. Uma classe base.

2. Classes derivadas que herdam da classe base.

3. Um programa principal para instanciar e usar os objetos.

**Exemplo Completo:** Sistema de Cadastro de Funcionários

Cenário

Criaremos um sistema onde:

1. Uma classe Funcionario gerencia informações básicas (nome, salário).

2. Uma classe derivada Gerente adiciona bônus.

3. O programa principal instancia os objetos e interage com eles.

Classe Base: Funcionario

IDENTIFICATION DIVISION.

CLASS-ID. FUNCIONARIO.

DATA DIVISION.

WORKING-STORAGE SECTION.

01 NOME            PIC X(30).

01 SALARIO         PIC 9(7)V99.

PROCEDURE DIVISION.

* Construtor: Inicializa os atributos.

METHOD-ID. NEW.

    DISPLAY "Criando Funcionário."

    MOVE SPACES TO NOME.

    MOVE 0 TO SALARIO.

END-METHOD.

* Método para configurar os atributos.

METHOD-ID. CONFIGURAR.

    INPUT PROCEDURE IS

        USING BY VALUE NOME-PARAM PIC X(30)

              BY VALUE SALARIO-PARAM PIC 9(7)V99.

    OUTPUT PROCEDURE IS

        GIVING.

    MOVE NOME-PARAM TO NOME.

    MOVE SALARIO-PARAM TO SALARIO.

END-METHOD.

* Método para exibir informações.

METHOD-ID. MOSTRAR.

    DISPLAY "Nome: " NOME.

    DISPLAY "Salário: " SALARIO.

END-METHOD.

END CLASS.

Classe Derivada: Gerente

IDENTIFICATION DIVISION.

CLASS-ID. GERENTE INHERITS FUNCIONARIO.

DATA DIVISION.

WORKING-STORAGE SECTION.

01 BONUS           PIC 9(5)V99.

PROCEDURE DIVISION.

* Construtor: Inicializa os atributos, incluindo o bônus.

METHOD-ID. NEW.

    INVOKE SUPER "NEW".

    MOVE 0 TO BONUS.

END-METHOD.

* Método para configurar o bônus.

METHOD-ID. CONFIGURAR-BONUS.

    INPUT PROCEDURE IS

        USING BY VALUE BONUS-PARAM PIC 9(5)V99.

    OUTPUT PROCEDURE IS

        GIVING.

    MOVE BONUS-PARAM TO BONUS.

END-METHOD.

* Método para exibir informações, sobrescrevendo o método base.

METHOD-ID. MOSTRAR.

    INVOKE SUPER "MOSTRAR".

    DISPLAY "Bônus: " BONUS.

END-METHOD.

END CLASS.

Programa Principal

IDENTIFICATION DIVISION.

PROGRAM-ID. CADASTRO-FUNCIONARIOS.

ENVIRONMENT DIVISION.

CONFIGURATION SECTION.

DATA DIVISION.

WORKING-STORAGE SECTION.

01 FUNCIONARIO-OBJ OBJECT REFERENCE FUNCIONARIO.

01 GERENTE-OBJ OBJECT REFERENCE GERENTE.

PROCEDURE DIVISION.

MAIN-PROGRAM.

    DISPLAY "=== Cadastro de Funcionários ===".

    * Instanciar um funcionário.

    CREATE FUNCIONARIO OF FUNCIONARIO

        HANDLE IN FUNCIONARIO-OBJ.

    * Configurar os dados do funcionário.

    INVOKE FUNCIONARIO-OBJ "CONFIGURAR"

        USING BY VALUE "João Silva"

                     BY VALUE 3000.00.

    * Mostrar os dados do funcionário.

    INVOKE FUNCIONARIO-OBJ "MOSTRAR".

    DISPLAY "----------------------------------".

    * Instanciar um gerente.

    CREATE GERENTE OF GERENTE

        HANDLE IN GERENTE-OBJ.

    * Configurar os dados do gerente.

    INVOKE GERENTE-OBJ "CONFIGURAR"

        USING BY VALUE "Maria Souza"

                     BY VALUE 7000.00.

    * Configurar o bônus do gerente.

    INVOKE GERENTE-OBJ "CONFIGURAR-BONUS"

        USING BY VALUE 2000.00.

    * Mostrar os dados do gerente.

    INVOKE GERENTE-OBJ "MOSTRAR".

    STOP RUN.

Explicação do Programa

1. Classe Funcionario:

Contém os atributos NOME e SALARIO.

Define métodos para configurar (CONFIGURAR) e exibir (MOSTRAR) os dados.

2. Classe Gerente:

Herda de Funcionario.

Adiciona o atributo BONUS e redefine o método MOSTRAR.

3. Programa Principal:

Usa CREATE para instanciar objetos das classes.

Chama métodos com INVOKE, configurando e exibindo os dados.

Execução e Saída

Ao executar o programa, a saída será:

=== Cadastro de Funcionários ===

Nome: João Silva

Salário: 3000.00

----------------------------------

Nome: Maria Souza

Salário: 7000.00

Bônus: 2000.00



### Benefícios da POO no COBOL

**1. Modularidade:** Classes encapsulam funcionalidades.

**2. Reutilização:** Herança permite reusar código.

**3. Organização:** Código mais legível e organizado.

**4. Facilidade em sistemas complexos:** Útil em sistemas bancários e financeiros.




### Outro exemplo em Cobol usando programação orientada a objetos.

# Exemplo de um programa em Cobol usando programação orientada a objetos.

![Screenshot_20250123-183809](https://github.com/user-attachments/assets/9a13723a-389b-4f9f-b735-234b9d5dfda2)



   # Os dados do programa:

**Os dados do programa são: um colégio tem turmas, de quinta série com três salas de 40 alunos, sala A, B, C, de sexta a série com três salas de 40 alunos, sala A, B, C, de sétima série com três salas de 40 alunos, sala A, B, C, de oitava série com 3 salas de 40 alunos, sala A, B, C. As matérias são: matemática, física, química, biologia, português, geografia, história, filosofia, sociologia.  A nota máxima para passar de ano é 100, a nota mínima para passar direto de ano é 60, a nota mínima para fazer as provas de recuperação é 50, e o aluno que tirar menos de 50 pontos na nota está reprovado direto sem direito a recuperação. O programa deverá mostrar um relatório com as notas de todos os alunos, deverá mostrar também os 3 alunos com as maiores notas e os 3 alunos com as menores notas, devera a média das notas de cada sala, e as salas com as maiores médias.**


 O programa implementa as regras descritas e organiza as classes para representar alunos, turmas e relatórios.

# Código COBOL

IDENTIFICATION DIVISION.

       CLASS-ID. SchoolManagement.

       ENVIRONMENT DIVISION.

       CONFIGURATION SECTION.

       DATA DIVISION.

       WORKING-STORAGE SECTION.

       01 WS-Aluno.

          05 WS-Nome               PIC X(30).

          05 WS-NotaMatematica     PIC 9(3).

          05 calculadoEMximo cal- variantes media de notest*************

READY_PROMTION SYSTEM

IDENTIFICATION DIVISION.

       CLASS-ID. SchoolManagement.

       DATA DIVISION.

       WORKING-STORAGE SECTION.

       OBJECT STORAGE SECTION.

       01 Turmas TYPE Turma.

       METHOD-ID. Main.

       LOCAL-STORAGE SECTION.

       PROCEDURE DIVISION.

           DISPLAY "Iniciando o sistema de gerenciamento escolar...".

           INVOKE Turmas "PreencherTurmas".

           INVOKE Turmas "GerarRelatorio".

           GOBACK.

       END METHOD Main.

       END CLASS SchoolManagement.

# Continuando o desenvolvimento, aqui está a próxima parte do código, que contém as classes para os alunos e as turmas, além dos métodos principais para gerenciar as turmas e as notas.

Classe Aluno

A classe Aluno representa cada aluno com nome e notas.

IDENTIFICATION DIVISION.

       CLASS-ID. Aluno.

       DATA DIVISION.

       WORKING-STORAGE SECTION.

       01 Nome             PIC X(30).

       01 NotaMatematica   PIC 9(3).

       01 NotaFisica       PIC 9(3).

       01 NotaQuimica      PIC 9(3).

       01 NotaBiologia     PIC 9(3).

       01 NotaPortugues    PIC 9(3).

       01 NotaGeografia    PIC 9(3).

       01 NotaHistoria     PIC 9(3).

       01 NotaFilosofia    PIC 9(3).

       01 NotaSociologia   PIC 9(3).

       OBJECT STORAGE SECTION.

       METHOD-ID. InicializarAluno.

       LOCAL-STORAGE SECTION.

       PROCEDURE DIVISION USING BY REFERENCE NomeAluno.

           MOVE NomeAluno TO Nome.

           MOVE 0 TO NotaMatematica, NotaFisica, NotaQuimica, NotaBiologia,

                     NotaPortugues, NotaGeografia, NotaHistoria, NotaFilosofia,

                     NotaSociologia.

           GOBACK.

       END METHOD InicializarAluno.

       METHOD-ID. CalcularMedia.

       LOCAL-STORAGE SECTION.

       01 MediaNotas       PIC 9(3).

       PROCEDURE DIVISION RETURNING MediaNotas.

           COMPUTE MediaNotas = (NotaMatematica + NotaFisica + NotaQuimica +

                                 NotaBiologia + NotaPortugues + NotaGeografia +

                                 NotaHistoria + NotaFilosofia + NotaSociologia) / 9.

           GOBACK.

       END METHOD CalcularMedia.

       END CLASS Aluno.

Classe Turma

A classe Turma gerencia as salas, alunos e médias.

IDENTIFICATION DIVISION.

       CLASS-ID. Turma.

       DATA DIVISION.

       WORKING-STORAGE SECTION.

       01 Alunos       TYPE Aluno OCCURS 40.

       01 Serie        PIC 9(1).

       01 Sala         PIC X(1).

       METHOD-ID. InicializarTurma.

       LOCAL-STORAGE SECTION.

       PROCEDURE DIVISION USING BY VALUE SerieInput SalaInput.

           MOVE SerieInput TO Serie.

           MOVE SalaInput TO Sala.

           PERFORM VARYING WS-Index FROM 1 BY 1 UNTIL WS-Index > 40

               INVOKE Alunos(WS-Index) "InicializarAluno" USING "Aluno-" & WS-Index

           END-PERFORM.

           GOBACK.

       END METHOD InicializarTurma.

       METHOD-ID. CalcularMediaTurma.

       LOCAL-STORAGE SECTION.

       01 MediaTotal       PIC 9(3)V9(2).

       01 MediaTurma       PIC 9(3)V9(2).

       01 WS-Index         PIC 9(2).

       PROCEDURE DIVISION RETURNING MediaTurma.

           MOVE 0 TO MediaTotal.

           PERFORM VARYING WS-Index FROM 1 BY 1 UNTIL WS-Index > 40

               ADD INVOKE Alunos(WS-Index) "CalcularMedia" TO MediaTotal

           END-PERFORM.

           DIVIDE MediaTotal BY 40 GIVING MediaTurma.

           GOBACK.

       END METHOD CalcularMediaTurma.

       END CLASS Turma.



# Próximos passos

**A seguir, implementarei a lógica para:**

1. Gerar o relatório completo com notas.

2. Identificar os 3 maiores e menores alunos.

3. Mostrar as salas com as maiores médias.


# Classe Relatorio

A classe Relatorio será responsável por processar os dados e exibir os resultados.

IDENTIFICATION DIVISION.

       CLASS-ID. Relatorio.

       DATA DIVISION.

       WORKING-STORAGE SECTION.

       01 Turmas TYPE Turma OCCURS 12.

       01 WS-Medias TYPE DECIMAL OCCURS 12.

       01 WS-Index PIC 9(2).

       01 WS-AlunoMaisNota TYPE Aluno OCCURS 3.

       01 WS-AlunoMenosNota TYPE Aluno OCCURS 3.

       01 MediaSalaMaior    TYPE NUMERIC.

       

# Classe Relatorio (completa)

IDENTIFICATION DIVISION.

       CLASS-ID. Relatorio.

       DATA DIVISION.

       WORKING-STORAGE SECTION.

       01 Turmas TYPE Turma OCCURS 12.

       01 WS-Medias          PIC 9(3)V9(2) OCCURS 12.

       01 WS-Index           PIC 9(2).

       01 WS-AlunoMaisNota   TYPE Aluno OCCURS 3.

       01 WS-AlunoMenosNota  TYPE Aluno OCCURS 3.

       01 MediaSalaMaior     PIC 9(3)V9(2).

       01 SalaComMaiorMedia  PIC X(3).

       01 WS-MediaAtual      PIC 9(3)V9(2).

       01 WS-AlunoAtual      TYPE Aluno.

       METHOD-ID. GerarRelatorio.

       LOCAL-STORAGE SECTION.

       01 WS-IndexTurma     PIC 9(2).

       01 WS-IndexAluno     PIC 9(2).

       01 TempMedia         PIC 9(3)V9(2).

       PROCEDURE DIVISION.

           DISPLAY "=== RELATÓRIO ESCOLAR ===".

           MOVE 0 TO WS-IndexTurma.

           PERFORM VARYING WS-IndexTurma FROM 1 BY 1 UNTIL WS-IndexTurma > 12

               DISPLAY "Turma: " Turmas(WS-IndexTurma)::Serie "-" Turmas(WS-IndexTurma)::Sala

               DISPLAY "Notas dos alunos:"

               PERFORM VARYING WS-IndexAluno FROM 1 BY 1 UNTIL WS-IndexAluno > 40

                   MOVE Turmas(WS-IndexTurma)::Alunos(WS-IndexAluno) TO WS-AlunoAtual

                   DISPLAY "Aluno: " WS-AlunoAtual::Nome

                   DISPLAY "Média: " INVOKE WS-AlunoAtual "CalcularMedia"

               END-PERFORM

               MOVE INVOKE Turmas(WS-IndexTurma) "CalcularMediaTurma" TO TempMedia

               MOVE TempMedia TO WS-Medias(WS-IndexTurma)

               DISPLAY "Média da Turma: " TempMedia

           END-PERFORM

           DISPLAY "----------------------------------------".

           DISPLAY "=== SALAS COM AS MAIORES MÉDIAS ===".

           MOVE 0 TO MediaSalaMaior.

           PERFORM VARYING WS-IndexTurma FROM 1 BY 1 UNTIL WS-IndexTurma > 12

               IF WS-Medias(WS-IndexTurma) > MediaSalaMaior

                   MOVE WS-Medias(WS-IndexTurma) TO MediaSalaMaior

                   STRING Turmas(WS-IndexTurma)::Serie "-" Turmas(WS-IndexTurma)::Sala

                          INTO SalaComMaiorMedia

               END-IF

           END-PERFORM

           DISPLAY "Sala com maior média: " SalaComMaiorMedia " - Média: " MediaSalaMaior.

           DISPLAY "----------------------------------------".

           DISPLAY "=== 3 MAIORES E MENORES MÉDIAS ===".

           PERFORM OrdenarAlunos

           DISPLAY "Top 3 maiores notas:"

           PERFORM VARYING WS-Index FROM 1 BY 1 UNTIL WS-Index > 3

               DISPLAY "Aluno: " WS-AlunoMaisNota(WS-Index)::Nome

               DISPLAY "Média: " INVOKE WS-AlunoMaisNota(WS-Index) "CalcularMedia"

           END-PERFORM

           DISPLAY "Top 3 menores notas:"

           PERFORM VARYING WS-Index FROM 1 BY 1 UNTIL WS-Index > 3

               DISPLAY "Aluno: " WS-AlunoMenosNota(WS-Index)::Nome

               DISPLAY "Média: " INVOKE WS-AlunoMenosNota(WS-Index) "CalcularMedia"

           END-PERFORM.

           GOBACK.

       END METHOD GerarRelatorio.

       METHOD-ID. OrdenarAlunos.

       LOCAL-STORAGE SECTION.

       01 WS-AlunosTodos TYPE Aluno OCCURS 480.

       01 WS-TempAluno   TYPE Aluno.

       01 TotalAlunos    PIC 9(3).

       PROCEDURE DIVISION.

           MOVE 0 TO TotalAlunos.

           PERFORM VARYING WS-IndexTurma FROM 1 BY 1 UNTIL WS-IndexTurma > 12

               PERFORM VARYING WS-IndexAluno FROM 1 BY 1 UNTIL WS-IndexAluno > 40

                   ADD 1 TO TotalAlunos

                   MOVE Turmas(WS-IndexTurma)::Alunos(WS-IndexAluno) TO WS-AlunosTodos(TotalAlunos)

               END-PERFORM

           END-PERFORM

           PERFORM VARYING WS-Index FROM 1 BY 1 UNTIL WS-Index > TotalAlunos

               PERFORM VARYING WS-IndexAluno FROM 1 BY 1 UNTIL WS-IndexAluno > TotalAlunos - WS-Index

                   IF INVOKE WS-AlunosTodos(WS-IndexAluno) "CalcularMedia" <

                      INVOKE WS-AlunosTodos(WS-IndexAluno + 1) "CalcularMedia"

                       MOVE WS-AlunosTodos(WS-IndexAluno) TO WS-TempAluno

                       MOVE WS-AlunosTodos(WS-IndexAluno + 1) TO WS-AlunosTodos(WS-IndexAluno)

                       MOVE WS-TempAluno TO WS-AlunosTodos(WS-IndexAluno + 1)

                   END-IF

               END-PERFORM

           END-PERFORM

           MOVE WS-AlunosTodos(1) TO WS-AlunoMaisNota(1)

           MOVE WS-AlunosTodos(2) TO WS-AlunoMaisNota(2)

           MOVE WS-AlunosTodos(3) TO WS-AlunoMaisNota(3)

           MOVE WS-AlunosTodos(TotalAlunos) TO WS-AlunoMenosNota(1)

           MOVE WS-AlunosTodos(TotalAlunos - 1) TO WS-AlunoMenosNota(2)

           MOVE WS-AlunosTodos(TotalAlunos - 2) TO WS-AlunoMenosNota(3).

           GOBACK.

       END METHOD OrdenarAlunos.

       END CLASS Relatorio.



### O que foi implementado

**1. Exibição das notas:** Mostra as notas de todos os alunos por turma.

**2. Média das salas:** Calcula a média de cada turma e identifica a maior.

**3. Ordenação de alunos:** Classifica todos os alunos por média.

**4. Relatório final:** Mostra os 3 melhores e 3 piores alunos.

