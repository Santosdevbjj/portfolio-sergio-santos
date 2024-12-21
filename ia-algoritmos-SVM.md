# O que são Algoritmos de SVM (Support Vector Machine)?

![Screenshot_20241220-190228](https://github.com/user-attachments/assets/efc672d4-20dc-42c2-af64-3a16c463563a)


Uma máquina de vetores de suporte (SVM) é um algoritmo de aprendizado de máquina supervisionado que classifica dados encontrando uma linha ou hiperplano ideal que maximize a distância entre cada classe em um espaço n-dimensional.

As SVMs foram desenvolvidas na década de 1990 por Vladimir N. Vapnik e seus colegas, e eles publicaram esse trabalho em um artigo intitulado "Support Vector Method for Function Approximation, Regression Estimation, and Signal Processing" em 1995. 

As SVMs são comumente usadas em problemas de classificação. Eles distinguem duas classes encontrando o hiperplano ideal que maximiza a margem entre os pontos de dados mais próximos de classes opostas. O número de atributos dos dados de entrada determina se o hiperplano é uma linha em um espaço 2D ou um plano em um espaço n-dimensional.

Como vários hiperplanos podem ser encontrados para diferenciar as classes, maximizar a margem entre os pontos permite que o algoritmo encontre o melhor limite de decisão entre as classes. Isso, por sua vez, permite uma boa generalização dos novos dados e a realização de previsões de classificação precisas.

As linhas adjacentes ao hiperplano ideal são conhecidas como vetores de suporte, pois esses vetores percorrem os pontos de dados que determinam a margem máxima. 

O algoritmo SVM é amplamente usado no aprendizado de máquina, pois é capaz de lidar com tarefas de classificação linear e não linear. No entanto, quando os dados não são linearmente separáveis, as funções kernel são usadas para transformar os dados em um espaço de dimensão superior para permitir a separação linear.

Essa aplicação de funções kernel pode ser conhecida como "truque de kernel", e a escolha da função kernel, como kernels lineares, kernels polinomiais, kernels de função de base radial (RBF) ou kernels sigmoides, depende das características dos dados e do caso de uso específico. 

## Tipos de classificadores SVM

### SVMs lineares

As SVMs lineares são usadas com dados linearmente separáveis; isso significa que os dados não precisam passar por nenhuma transformação para separá-los em classes diferentes.

O limite de decisão e os vetores de suporte formam a aparência de uma rua, e o professor Patrick Winston, do MIT, usa a analogia do "ajuste da rua mais larga possível" para descrever esse problema de otimização quadrática.

Matematicamente, esse hiperplano de separação pode ser representado como: 

wx + b = 0

em que w é o vetor de peso, x é o vetor de entrada e b é o termo de viés. 

Há duas abordagens para calcular a margem, ou a distância máxima entre as classes, que são a classificação com margem rígida e a classificação com margem flexível.

Se usarmos uma SVM de margem rígida, os pontos de dados serão perfeitamente separados fora dos vetores de suporte, ou "fora da rua" segundo a analogia do professor Hinton. 

## Isso é representado pela fórmula:

(wxj + b) yj ≥ a

e, em seguida, a margem é maximizada, o que é representado como: máx ɣ= a / ||w||, onde a é a margem projetada em w.

A classificação de margem flexível, como o próprio nome diz, é mais flexível, permitindo alguns erros de classificação por meio do uso de variáveis de folga ('ξ'). O hiperparâmetro, C, ajusta a margem; um valor C maior estreita a margem para a classificação incorreta mínima, enquanto um valor C menor a amplia, permitindo a classificação incorreta de mais dados. 

### SVMs não lineares

Grande parte dos dados em cenários do mundo real não são separáveis de forma linear, e é aí que as SVMs não lineares entram em ação. A fim de tornar os dados separáveis de forma linear, métodos de pré-processamento são aplicados aos dados de treinamento para transformá-los em um espaço de atributos de maior dimensão. 

Dito isso, os espaços dimensionais superiores são capazes de criar mais complexidade, aumentando o risco de sobreajuste dos dados e aumentando a exigência computacional. 

O "truque do kernel" ajuda a reduzir parte dessa complexidade, tornando a computação mais eficiente, e faz isso substituindo os cálculos de produto escalar por uma função de kernel equivalente.

Há vários tipos diferentes de kernel que podem ser aplicados para classificar dados. Algumas funções populares do kernel incluem: 

- Kernel polinomial
- Kernel de função de base radial (também conhecido como kernel gaussiano ou RBF)
- Kernel Sigmoide 

### Regressão por vetores de suporte (SVR)

A regressão por vetores de suporte (SVR) é uma extensão das SVMs, aplicada a problemas de regressão (ou seja, o resultado é contínuo). 

De modo semelhante às SVMs lineares, o SVR encontra um hiperplano com a margem máxima entre os pontos de dados e é normalmente usado para a previsão de séries temporais.

A SVR difere da regressão linear porque você precisa especificar a relação que você deseja entender entre as variáveis independentes e dependentes.

Compreender as relações entre variáveis e suas direções é valioso ao usar a regressão linear. Isso é desnecessário nas SVRs, pois elas determinam esses relacionamentos sozinhas. 

## Como criar um classificador SVM

### Divida seus dados

Como em outros modelos de aprendizado de máquina, comece dividindo seus dados em um conjunto de treinamento e um conjunto de teste. Observação: pressupõe-se que você já tenha realizado uma análise exploratória em seus dados.

Embora isso não seja tecnicamente necessário para criar um classificador SVM, é uma boa prática antes de usar qualquer modelo de aprendizado de máquina, pois isso ajudará na compreensão de quaisquer dados ausentes ou valores discrepantes.

### Gere e avalie o modelo

Importe um módulo SVM da biblioteca de sua escolha, como scikit-learn. Treine suas amostras de treinamento no classificador e preveja a resposta.

Você pode avaliar o desempenho comparando a precisão do conjunto de testes com os valores previstos. É recomendável usar outras métricas de avaliação, como f1-score, precisão ou recall. 

### Ajuste de hiperparâmetros

Os hiperparâmetros podem ser ajustados para melhorar o desempenho de um modelo SVM.

Os hiperparâmetros ideais podem ser encontrados usando métodos de pesquisa de grade e validação cruzada, que irão iterar diferentes valores de kernel, regularização (C) e gama para encontrar a melhor combinação.

## SVMs x outros classificadores de aprendizado supervisionado

Diferentes classificadores de aprendizado de máquina podem ser usados para o mesmo caso de uso.

É importante testar e avaliar diferentes modelos para entender quais funcionam melhor. Dito isso, pode ser útil entender os pontos fortes e fracos de cada um para avaliar sua aplicação em seu caso de uso. 

### SVMs x Naive-Bayes

Os classificadores Naive Bayes e SVM são comumente usados em tarefas de classificação de texto. As SVMs tendem a ter um desempenho melhor do que o Naive Bayes quando os dados não são separáveis de forma linear.

Dito isso, as SVMs precisam se ajustar a diferentes hiperparâmetros e podem ser mais custosas em termos computacionais. 

### SVMs x regressão logística

As SVMs geralmente têm um desempenho melhor com conjuntos de dados de alta dimensão e não estruturados, como dados de imagem e texto, em comparação com a regressão logística.

As SVMs também são menos sensíveis ao overfitting e mais fáceis de interpretar. Dito isso, elas podem ser mais custosas em termos computacionais.

### SVMs x árvores de decisão

As SVMs têm melhor desempenho com dados de alta dimensão e são menos propensas a sobreajustes em comparação às árvores de decisão.

Dito isso, as árvores de decisão geralmente são mais rápidas de treinar, principalmente com conjuntos de dados menores, e geralmente são mais fáceis de interpretar. 

### SVM x redes neurais

Semelhante a outras comparações de modelos, as SVMs são mais caras computacionalmente para treinar e menos propensas ao sobreajuste, mas as redes neurais são consideradas mais flexíveis e escaláveis.

## Aplicações de SVMs

Embora as SVMs possam ser aplicadas a diversas tarefas, estas estão entre as aplicações mais populares das SVMs em todos os setores.  

### Classificação de texto

A SVMs são comumente usadas em processamento de linguagem natural (NLP) para tarefas como análise de sentimento, detecção de spam e modelagem de tópicos. Elas se adequam bem a esses dados porque têm um bom desempenho com dados de alta dimensão.

### Classificação de imagens

As SVMs são aplicadas em tarefas de classificação de imagens, como detecção de objetos e recuperação de imagens.

Também podem ser úteis em domínios de segurança, classificando uma imagem como adulterada, por exemplo.

### Bioinformática

As SVMs também são usadas na classificação de proteínas, análise de expressão gênica e diagnóstico de doenças. As SVMs são frequentemente aplicadas na pesquisa de câncer porque podem detectar tendências sutis em conjuntos de dados complexos. 

### Sistema de informação geográfica (GIS)

As SVMs podem analisar estruturas geofísicas em camadas no subsolo, filtrando o "ruído" dos dados eletromagnéticos. Eles também ajudaram a prever o potencial de liquefação sísmica do solo, o que é relevante para o campo da engenharia civil. 



