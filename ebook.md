
# Python (E-BOOK)

## O que é Python

Python é uma linguagem de programação de alto nível, versátil e de fácil leitura. Desenvolvida por Guido van Rossum, ela se destaca pela sua sintaxe clara e expressiva. 

## Conhecendo o interpretador Python e o seu ecossistema. 

Para executar um programa em python, você digita python prog.py (.py é a extensão do arquivo de um programa em python) na linha de comando, e o programa é executado. Mas o que é esse python que você digitou?

Se você parar para pensar, ele é um programa que esta instalado em seu computador. Mas ele é um programa que executou outro programa (o que estava no arquivo prog.py). 

Veja bem: um programa que executa outro programa!

O programa Python, que tem esta capacidade de executar programas escritos na linguagem de programação Python, é o que chamamos de interpretador Python. Ele lê programas escritos em Python e os interpreta (executa), daí o nome interpretador.

Agora que já sabemos o que é o interpretador Python, chegou a hora de entendermos melhor como ele funciona. Uma das grandes vantagens de linguagens interpretadas, como Python, é a interatividade que o interpretador oferece.

Essa interatividade consiste basicamente no fato de que, ao abrir o interpretador, você verá um "prompt" (um sinal de >>>), pronto para receber, avaliar, e executar seus comandos.

Para abrir o interpretador, digite:  "python" na linha de comando.

O interpretador opera sempre em um ciclo: ele lê (read) um comando, avalia (eval) o comando, imprime (print) a saída, e fica a postos para receber o próximo comando. Por essa razão, algumas pessoas se referem ao modo como interpretadores funcionam como um ciclo read-eval-print.

O interpretador trabalha de forma semelhante a uma shell de Unix: quando chamado com a saída padrão conectada a um console de terminal, ele lê e executa comandos interativamente.

Fontes -> https://algoritmosempython.com.br, https://docs.python.org

## Python é só interpretada?
A resposta é: Não!

Ela é uma junção de uma linguagem interpretada comum e uma linguagem compilada comum.

Em Python, o interpretador e compilador estão relacionados e coexistem. O interpretador CPython, que é a implementação de referência da linguagem Python, realiza ambos os papéis em conjunto. Isso é conhecido como interpretação just-in-time (JIT) e compilação.

Quando você executa um script Python, o interpretador CPython realiza as seguintes etapas:

### Compilação para Bytecode (Modo de Compilação)

O código-fonte Python (.py) é compilado para bytecode Python (.pyc) pelo compilador embutido em tempo de execução. Esse bytecode é uma representação intermediária.

### Execução do Bytecode na Máquina Virtual Python (Modo de Interpretação)

O bytecode gerado é interpretado e executado pela Python Virtual Machine (PVM). Durante a execução, o interpretador pode otimizar certas partes do código para melhor desempenho.

Essa combinação de compilação para bytecode e interpretação em tempo real proporciona uma abordagem flexível e portável para a execução de código Python. O bytecode é armazenado em arquivos .pyc para otimizar o tempo de carregamento e execução subsequente do script.

### Conclusão

Portanto, não é necessário que os desenvolvedores executem explicitamente um processo de compilação separado antes de executar um script Python. O interpretador CPython cuida disso automaticamente. Essa abordagem simplifica o desenvolvimento, pois os desenvolvedores podem se concentrar no código-fonte sem se preocupar com o processo de compilação.

O Python utiliza um processo de compilação just-in-time (JIT), onde o código fonte é compilado para um bytecode em tempo de execução.

- É correto falar que o Python é compilado linha por linha em execução em tempo real?
- Sim!

## Ciclo de Vida do Código em Python Em Scripts
O ciclo de vida do código Python pode ser dividido em três fases principais.

### Nascimento
Criação do Código: Desenvolvedores escrevem o código em um editor de texto ou IDE.
Salvamento do Arquivo: O código é salvo em um arquivo .py.

### Execução
Interpretação e Compilação para Bytecode: O interpretador Python lê e converte o código-fonte em bytecode durante a interpretação.

Execução do Bytecode: A Máquina Virtual Python executa diretamente o bytecode gerado, realizando as instruções do programa, assim se tornando uma linguagem multiplataforma. 

### Término
Conclusão da Execução: O código termina quando todas as instruções são executadas ou ocorre um evento que interrompe a execução.

Liberação de Recursos: Recursos alocados, como memória, são liberados.

Fechamento do Interpretador: Após a conclusão, o interpretador Python é encerrado, finalizando o ciclo de vida do código.

## Vantagens
**Produtividade:** A sintaxe concisa e as bibliotecas extensas permitem que os desenvolvedores alcancem resultados rapidamente.

**Comunidade Ativa:** Uma comunidade grande e colaborativa oferece suporte e recursos valiosos.

**Versatilidade:** Pode ser usado em uma ampla gama de domínios, desde projetos simples até complexos.

## Desvantagens
**Desempenho:** Em comparação com linguagens de baixo nível, Python pode ser mais lento em situações críticas de desempenho.

**Mobilidade Limitada:** Não é a escolha ideal para desenvolvimento móvel.

## Ambiente de Desenvolvimento

Suportado por IDEs populares como PyCharm, VSCode e Jupyter, proporcionando um ambiente robusto.
Características para Iniciantes

## Sintaxe Simples: Python tem uma sintaxe fácil de aprender, próxima à linguagem falada.

**Multiparadigma:** Suporta diferentes estilos de programação, como procedural, funcional e orientado a objetos.

**Semântica Dinâmica:** Não é necessário declarar previamente o tipo de dado usado.
Esses pontos resumem o que torna Python uma escolha poderosa e acessível para programadores iniciantes e experientes.

## Usando o modo interativo para aprender a sintaxe básica do python.

### Primeiro vamos entender o que é o modo interativo.

O modo interativo do Python é uma forma de interagir com o interpretador Python de maneira direta.

Pense no modo interativo do Python como uma conversa direta com o computador. É como se você estivesse dizendo coisas para o computador e ele respondesse imediatamente.

### Conversa com o Computador

Digite python no shell do seu computador.

Digite algo como "2 + 3" e o computador responde "5".

Agora você digita, nome = “joão” é o equivalente de dizer "crie uma variável chamada 'nome' e coloque o valor “joão”.

Variáveis são valores que precisam de um tipo específico, python automaticamente consegue relacionar os valores ao tipo da variável. Mais a frente iremos detalhar melhor sobre os tipos de dados em python.

Você digita “nome”, equivale a uma pergunta "qual é o valor de 'nome'?" e o computador responde "João".

É como se você estivesse experimentando com pedaços pequenos de código para ver como eles funcionam.

Por exemplo, você pode querer descobrir o resultado de uma expressão matemática ou testar como uma função específica se comporta.

O Feedback Imediato é uma vantagem, pois cada vez que você digita uma linha de código, o computador lê, executa instantaneamente, e talvez aponte algum erro.

Isso permite que você veja imediatamente o que acontece, facilitando a aprendizagem e a depuração (identificação e correção de erros).

Quando você terminar sua "conversa" e não quiser mais interagir, você pode dizer "tchau" (digitar exit()), e o modo interativo se fecha.

Então, é como ter uma conversa curta com o computador, onde você faz perguntas ou dá comandos e obtém respostas instantâneas. Isso é útil para aprender, testar ideias e entender como o Python funciona.

## Sintaxe básica

### O que é uma variável?

Primeiramente vamos supor que a memória ram é dividida em várias caixas com etiquetas, cada caixa tem uma etiqueta com um identificador único, que é chamado de endereço de memória.

A variável é o conteúdo desta caixa, com três informações: O nome da variável, o tipo e o valor.

### Como a variável funciona na memória?

Quando você cria uma variável, você basicamente está reservando um lugar na memória do 
computador.

Se você muda o valor da variável, está apenas trocando o que está dentro dessa caixa na memória.

Exemplo Prático no PowerShell, cmd ou terminal.

```                                                     						           
python # abrindo o modo interativo

# Declarando variáveis
idade = 25 # tipo inteiro

# Exibindo informações
print("Idade: ", idade)

# Modificando variáveis
idade = 26

# Exibindo informações
print("Idade: ", idade)
```

Tipos

Tipo é a abstração da característica de um dado. 

Se um dado tem a característica numeral, ele poderá ser do tipo inteiro, real…
Se tiver a característica de caracteres poderá ser uma string, um caráter único… 
Se a característica for de um valor verdadeiro ou falso o tipo será booleano. 

Desta forma o tipo de dado altera o comportamento do interpretador, para realizar operações com o determinado valor. 

Exemplos de tipos de dados em python:                                                                   

Em Python, os tipos de dados são essenciais para representar diferentes tipos de valores e realizar operações específicas. Abaixo estão alguns dos tipos de dados mais comuns em Python, juntamente com suas usuabilidades:

Inteiro (int):
Representa números inteiros.
Usado em operações aritméticas.
idade = 25

Ponto Flutuante (float):
Representa números decimais ou de ponto flutuante.
Utilizado em cálculos que envolvem números fracionários.
altura = 1.75

String (str):
Representa sequências de caracteres.
Usado para manipulação de texto.
nome = "João"

Booleano (bool):
Representa valores lógicos (True ou False).
Usado em expressões condicionais e controle de fluxo.
esta_chovendo = False

Lista (list):
Armazena uma coleção ordenada de elementos mutáveis.
Útil para armazenar e manipular conjuntos de dados.
numeros = [1, 2, 3, 4, 5]

Tupla (tuple):
Similar a uma lista, mas é imutável (não pode ser alterada após a criação).
Usada quando se deseja garantir que os dados não sejam modificados.
coordenadas = (10, 20)

Dicionário (dict):
Armazena pares chave-valor.
Útil para representar dados estruturados e acessar valores por meio de chaves.
pessoa = {"nome": "Maria", "idade": 30}

Conjunto (set):
Armazena elementos únicos e não ordenados.
Útil para operações de conjunto, como união e interseção.
cores = {"vermelho", "verde", "azul"}

NoneType (None):
Representa a ausência de valor.
Usado para indicar a falta de um valor em variáveis ou funções.
resultado = None

Esses são alguns dos tipos de dados fundamentais em Python. A escolha do tipo de dado depende do contexto e da tarefa que você está realizando. Python é uma linguagem dinamicamente tipada, o que significa que você não precisa declarar explicitamente o tipo de uma variável; o interpretador faz isso automaticamente.
Função type
Podemos saber o tipo de determinada variável com a função type, na qual determina o tipo da variável.


```
python # para abrir o modo interativo no seu shell

idade = 22

print(type(idade)) # A função print serve para imprimir no console uma saída de um script, como estamos no modo interativo ela não é necessária nesse contexto.
type(idade) # Contém o mesmo retorno no modo interativo

```
O resultado será:  <class 'int'> 

A função pode ser utilizada para descobrir qualquer tipo de variável.

Para podermos brincar mais com a linguagem vamos introduzir

Prática -> Faça operações aritméticas no modo interativo do python de dois inteiros.
Exemplo: 

[ powershell ou terminal   

python #Entra no modo interativo

anoDeNascimento = 2001
anoAtual = 2023

minhaIdade = anoAtual - anoDeNascimento

print(minhaIdade) # print é uma função que imprime os dados no console.
minhaIdade # Sem o print também é possível visualizar o resultado.

]

Python

O que é Python
Python é uma linguagem de programação de alto nível, versátil e de fácil leitura. 

Desenvolvida por Guido van Rossum, ela se destaca pela sua sintaxe clara e expressiva. 
Conhecendo o interpretador Python e o seu ecossistema. 
Para executar seu programa, você digitou python prog.py na linha de comando, e o programa foi executado. Mas o que é esse python que você digitou?

Se você parar para pensar, ele é um programa que você instalou em seu computador. Mas ele é um programa que executou outro programa (o que estava no arquivo prog.py que você criou). Veja bem: um programa que executa outro programa!

O programa Python, que tem esta capacidade de executar programas escritos na linguagem de programação Python, é o que chamamos de interpretador Python. Ele lê programas escritos em Python e os interpreta (executa), daí o nome interpretador.

Agora que já sabemos o que é o interpretador Python, chegou a hora de entendermos melhor como ele funciona. Uma das grandes vantagens de linguagens interpretadas, como Python, é a interatividade que o interpretador oferece.

Essa interatividade consiste basicamente no fato de que, ao abrir o interpretador, você verá um "prompt" (um sinal de >>>), pronto para receber, avaliar, e executar seus comandos.

Para abrir o interpretador, digite python na linha de comando.

O interpretador opera sempre em um ciclo: ele lê (read) um comando, avalia (eval) o comando, imprime (print) a saída, e fica a postos para receber o próximo comando. Por essa razão, algumas pessoas se referem ao modo como interpretadores funcionam como um ciclo read-eval-print.

O interpretador trabalha de forma semelhante a uma shell de Unix: quando chamado com a saída padrão conectada a um console de terminal, ele lê e executa comandos interativamente; quando chamado com um nome de arquivo como argumento, ou com redirecionamento da entrada padrão para ler um arquivo, o interpretador lê e executa o script contido no arquivo.

Fontes -> https://algoritmosempython.com.br, https://docs.python.org

Python é só interpretada?
A resposta é: Não!

Ela é uma junção de uma linguagem interpretada comum e uma linguagem compilada comum.

Em Python, o interpretador e compilador estão relacionados e coexistem. O interpretador CPython, que é a implementação de referência da linguagem Python, realiza ambos os papéis em conjunto. Isso é conhecido como interpretação just-in-time (JIT) e compilação.

Quando você executa um script Python, o interpretador CPython realiza as seguintes etapas:

Compilação para Bytecode (Modo de Compilação)

O código-fonte Python (.py) é compilado para bytecode Python (.pyc) pelo compilador embutido em tempo de execução. Esse bytecode é uma representação intermediária.

Execução do Bytecode na Máquina Virtual Python (Modo de Interpretação)

O bytecode gerado é interpretado e executado pela Python Virtual Machine (PVM). Durante a execução, o interpretador pode otimizar certas partes do código para melhor desempenho.

Essa combinação de compilação para bytecode e interpretação em tempo real proporciona uma abordagem flexível e portável para a execução de código Python. O bytecode é armazenado em arquivos .pyc para otimizar o tempo de carregamento e execução subsequente do script.

Portanto, não é necessário que os desenvolvedores executem explicitamente um processo de compilação separado antes de executar um script Python. O interpretador CPython cuida disso automaticamente. Essa abordagem simplifica o desenvolvimento, pois os desenvolvedores podem se concentrar no código-fonte sem se preocupar com o processo de compilação.

O Python utiliza um processo de compilação just-in-time (JIT), onde o código fonte é compilado para um bytecode em tempo de execução.

É correto falar que o Python é compilado linha por linha em execução em tempo real?
Sim!
Ciclo de Vida do Código em Python Em Scripts
O ciclo de vida do código Python pode ser dividido em três fases principais.

Nascimento
Criação do Código: Desenvolvedores escrevem o código em um editor de texto ou IDE.
Salvamento do Arquivo: O código é salvo em um arquivo .py.

Execução
Interpretação e Compilação para Bytecode: O interpretador Python lê e converte o código-fonte em bytecode durante a interpretação.

Execução do Bytecode: A Máquina Virtual Python executa diretamente o bytecode gerado, realizando as instruções do programa, assim se tornando uma linguagem multiplataforma. 

Término
Conclusão da Execução: O código termina quando todas as instruções são executadas ou ocorre um evento que interrompe a execução.

Liberação de Recursos: Recursos alocados, como memória, são liberados.

Fechamento do Interpretador: Após a conclusão, o interpretador Python é encerrado, finalizando o ciclo de vida do código.
Vantagens
Produtividade: A sintaxe concisa e as bibliotecas extensas permitem que os desenvolvedores alcancem resultados rapidamente.

Comunidade Ativa: Uma comunidade grande e colaborativa oferece suporte e recursos valiosos.

Versatilidade: Pode ser usado em uma ampla gama de domínios, desde projetos simples até complexos.
Desvantagens
Desempenho: Em comparação com linguagens de baixo nível, Python pode ser mais lento em situações críticas de desempenho.

Mobilidade Limitada: Não é a escolha ideal para desenvolvimento móvel.
Ambiente de Desenvolvimento
Suportado por IDEs populares como PyCharm, VSCode e Jupyter, proporcionando um ambiente robusto.
Características para Iniciantes
Sintaxe Simples: Python tem uma sintaxe fácil de aprender, próxima à linguagem falada.

Multiparadigma: Suporta diferentes estilos de programação, como procedural, funcional e orientado a objetos.

Semântica Dinâmica: Não é necessário declarar previamente o tipo de dado usado.
Esses pontos resumem o que torna Python uma escolha poderosa e acessível para programadores iniciantes e experientes.
Usando o modo interativo para aprender a sintaxe básica do python.
Primeiro vamos entender o que é o modo interativo.
O modo interativo do Python é uma forma de interagir com o interpretador Python de maneira direta.

Pense no modo interativo do Python como uma conversa direta com o computador. É como se você estivesse dizendo coisas para o computador e ele respondesse imediatamente.

Conversa com o Computador:

Digite python no shell do seu computador.

Digite algo como "2 + 3" e o computador responde "5".

Agora você digita, nome = “joão” é o equivalente de dizer "crie uma variável chamada 'nome' e coloque o valor “joão”.

Variáveis são valores que precisam de um tipo específico, python automaticamente consegue relacionar os valores ao tipo da variável. Mais a frente iremos detalhar melhor sobre os tipos de dados em python.

Você digita “nome”, equivale a uma pergunta "qual é o valor de 'nome'?" e o computador responde "João".

É como se você estivesse experimentando com pedaços pequenos de código para ver como eles funcionam.

Por exemplo, você pode querer descobrir o resultado de uma expressão matemática ou testar como uma função específica se comporta.

Feedback Imediato, cada vez que você digita uma linha de código, o computador lê e executa instantaneamente, e talvez aponte algum erro.

Isso permite que você veja imediatamente o que acontece, facilitando a aprendizagem e a depuração (identificação e correção de erros).

Saída Fácil:
Quando você terminar sua "conversa" e não quiser mais interagir, você pode dizer "tchau" (digitar exit()), e o modo interativo se fecha.

Então, é como ter uma conversa curta com o computador, onde você faz perguntas ou dá comandos e obtém respostas instantâneas. Isso é útil para aprender, testar ideias e entender como o Python funciona.

Sintaxe básica

O que é uma variável?

Primeiramente vamos supor que a memória ram é dividida em várias caixas com etiquetas, cada caixa tem uma etiqueta com um identificador único, que é chamado de endereço de memória.

A variável é o conteúdo desta caixa, com três informações: O nome da variável, o tipo e o valor.

Como a variável funciona na memória?

Quando você cria uma variável, você basicamente está reservando um lugar na memória do 
computador.

Se você muda o valor da variável, está apenas trocando o que está dentro dessa caixa na memória.

Exemplo Prático:

```                                                     						           
python

# Declarando variável
idade = 25 # tipo inteiro

# Exibindo informações
print("Idade: ", idade) # A função print serve para imprimir no console uma saída de um script, como estamos no modo interativo pode ser que não seja necessária em alguns contextos. 

# Modificando variável
idade = 26

# Exibindo informações
print("Idade: ", idade)
```
Resultado 1: Idade: 25
Resultado 2: Idade 26

## Tipos

Tipo é a abstração da característica de um dado. 

- Se um dado tem a característica numeral, o tipo poderá ser do tipo inteiro, real…
- Se tiver a característica de uma cadeia de caracteres o tipo será ser uma string.
- Se a característica é de um valor verdadeiro ou falso o tipo será booleano. 

Desta forma o tipo de dado altera o comportamento do interpretador, para realizar operações com o determinado valor da variável. 

### Exemplos de tipos de dados em python:                                                                   

Em Python, os tipos de dados são essenciais para representar diferentes tipos de valores e realizar operações específicas. Abaixo estão alguns dos tipos de dados mais comuns em Python, juntamente com suas usuabilidades:

Inteiro (int):
Representa números inteiros.
Usado em operações aritméticas.
```
idade = 25
```
Ponto Flutuante (float):
Representa números decimais ou de ponto flutuante.
Utilizado em cálculos que envolvem números fracionários.
```
altura = 1.75
```
String (str):
Representa sequências de caracteres.
Usado para manipulação de texto.
```
nome = "João"
```
Booleano (bool):
Representa valores lógicos (True ou False).
Usado em expressões condicionais e controle de fluxo.
```
esta_chovendo = False
```
Lista (list):
Armazena uma coleção ordenada de elementos mutáveis.
Útil para armazenar e manipular conjuntos de dados.
```
numeros = [1, 2, 3, 4, 5]
```
Tupla (tuple):
Similar a uma lista, mas é imutável (não pode ser alterada após a criação).
Usada quando se deseja garantir que os dados não sejam modificados.
```
coordenadas = (10, 20)
```
Dicionário (dict):
Armazena pares chave-valor.
Útil para representar dados estruturados e acessar valores por meio de chaves.
```
pessoa = {"nome": "Maria", "idade": 30}
```
Conjunto (set):
Armazena elementos únicos e não ordenados.
Útil para operações de conjunto, como união e interseção.
```
cores = {"vermelho", "verde", "azul"}
```
NoneType (None):
Representa a ausência de valor.
Usado para indicar a falta de um valor em variáveis ou funções.
```
resultado = None
```
Esses são alguns dos tipos de dados fundamentais em Python. A escolha do tipo de dado depende do contexto e da tarefa que você está realizando. Python é uma linguagem dinamicamente tipada, o que significa que você não precisa declarar explicitamente o tipo de uma variável; o interpretador faz isso automaticamente.
Função type
Podemos saber o tipo de determinada variável com a função type, na qual determina o tipo da variável.


```
python # para abrir o modo interativo no seu shell

idade = 22

print(type(idade))
type(idade) # Contém o mesmo retorno no modo interativo

```
O resultado será:  **<class 'int'>**

A função pode ser utilizada para descobrir qualquer tipo de variável.

Para podermos brincar mais com a linguagem vamos introduzir

Prática -> Faça operações aritméticas no modo interativo do python de dois inteiros.
Exemplo: 

[ powershell ou terminal   

python #Entra no modo interativo

anoDeNascimento = 2001
anoAtual = 2023

minhaIdade = anoAtual - anoDeNascimento

print(minhaIdade) # print é uma função que imprime os dados no console.
minhaIdade # Sem o print também é possível visualizar o resultado.

]
