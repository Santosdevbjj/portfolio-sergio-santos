# Hash: Conceitos, Características e Aplicações

## O que é um Hash?

Um hash é uma função matemática que transforma uma entrada (dados de qualquer tamanho, como texto ou arquivos) em uma saída fixa de comprimento específico.

A saída gerada é chamada de valor de hash ou resumo de hash. Hashes são amplamente usados em diversas áreas da computação, como segurança, verificação de integridade e armazenamento eficiente de dados.

## Características de uma função hash

1. **Determinística**: Para uma mesma entrada, sempre retorna o mesmo valor de hash.

2. **Unidirecional**: É fácil calcular o hash de uma entrada, mas muito difícil (praticamente impossível) reverter o processo para descobrir a entrada original.

3. **Sensível a alterações**: Qualquer mudança na entrada, mesmo mínima, gera um valor de hash completamente diferente.

4. **Eficiência**: Deve ser rápida para calcular o hash, mesmo para entradas grandes.

5. **Resistência a colisões**: Duas entradas diferentes dificilmente geram o mesmo valor de hash.

## Exemplos práticos

### Exemplo 1: Verificação de integridade

Imagine que você faça o download de um arquivo. O site fornece o valor de hash do arquivo para que você possa verificar se o arquivo não foi corrompido durante o download.

1. Antes de enviar o arquivo, o site calcula o hash, por exemplo, usando o algoritmo SHA-256, e informa o valor:
   - Hash do arquivo original: d2d2d2a5678e098f23d... (64 caracteres)

2. Após o download, você usa um programa para calcular o hash do arquivo baixado. Se o hash for idêntico ao informado, o arquivo está íntegro. Caso contrário, ele foi alterado ou corrompido.

### Exemplo 2: Armazenamento seguro de senhas

Em sistemas de autenticação, senhas dos usuários não são armazenadas diretamente, mas sim seus valores de hash:

1. Usuário escolhe a senha "senha123"

2. O sistema calcula o hash da senha usando, por exemplo, o algoritmo bcrypt:
   - Hash gerado: $2a$12$J9vJbODv/aW... (código complexo)

3. Quando o usuário tenta fazer login, o sistema recalcula o hash da senha fornecida e compara com o hash armazenado. Se forem iguais, o acesso é concedido.

### Exemplo 3: Estruturas de dados - Tabelas Hash

Hashes são usados em tabelas hash para armazenar e acessar dados rapidamente:

1. Imagine uma tabela de telefones:
   - Nome: Alice Veiga
   - Telefone: (37) 9999-9999

2. O sistema calcula o hash do nome (por exemplo, A1B2C3)

3. O hash é usado como índice para localizar rapidamente o telefone na tabela.

## Algoritmos de hash comuns

- MD5: Antigo e rápido, mas inseguro para uso em segurança
- SHA-1: Também obsoleto devido a vulnerabilidades
- SHA-256: Amplamente usado em segurança e blockchain
- SHA-512 (512 bits): Ainda mais seguro
- bcrypt e Argon2: Projetados especificamente para proteger senhas

Para segurança de senhas, é recomendado usar algoritmos específicos como bcrypt, Argon2 ou PBKDF2, que são mais lentos propositalmente para dificultar ataques de força bruta.

## Exemplo em Python

```python
import hashlib

# Entrada
texto = "Exemplo de hash"

# Gerar hash usando SHA-256
hash_obj = hashlib.sha256(texto.encode())
hash_hex = hash_obj.hexdigest()

print(f"Texto original: {texto}")
print(f"Hash gerado: {hash_hex}")
```

Saída:
```
Texto original: Exemplo de hash
Hash gerado: 769a70ce9b5b2ab68de8b372b7517a2f9f59c718d9d9b0fa8dcd508f95c7ac21
```

## Hashes na Criptografia

### Hashes e Criptografia: Uma Dupla Dinâmica

Os hashes desempenham um papel fundamental na criptografia, garantindo segurança e integridade da informação através de:

- Armazenamento seguro de senhas
- Verificação de integridade de arquivos
- Assinaturas digitais
- Tecnologia blockchain

### Como Funcionam os Algoritmos de Hash

1. **Entrada**: O algoritmo recebe um conjunto de dados de qualquer tamanho
2. **Processamento**: Os dados passam por operações matemáticas complexas
3. **Saída**: Resulta em um hash de tamanho fixo em formato hexadecimal

## Colisões em Hash

### O que são colisões?

Uma colisão ocorre quando dois dados diferentes geram o mesmo valor de hash. Isso pode ser explorado por invasores através de:

- Falsificação de dados
- Ataques de "homem no meio"
- Ataques de pré-imagem

### Mitigando riscos de colisões

- Usar algoritmos seguros (SHA-256, SHA-3)
- Implementar salting
- Utilizar verificações adicionais

## Assinaturas Digitais

### Funcionamento

1. **Criação da assinatura**:
   - Cálculo do hash do documento
   - Criptografia do hash com chave privada
   - Anexação da assinatura ao documento

2. **Verificação**:
   - Descriptografia da assinatura com chave pública
   - Comparação dos hashes

### Aplicações

- Contratos eletrônicos
- Verificação de software
- Segurança de email
- Transações financeiras

### Benefícios

- Autenticidade garantida
- Integridade dos dados
- Não repúdio
- Possibilidade de confidencialidade adicional 
