# Python (E-BOOK)

## O que é Python

Python é uma linguagem de programação de alto nível, versátil e de fácil leitura. Desenvolvida por Guido van Rossum, ela se destaca pela sua sintaxe clara e expressiva. 

## Conhecendo o seu ecossistema. 

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

Ela é uma "junção" de uma linguagem compilada comum e uma linguagem interpretada comum, nesta ordem.

Mas primeiramente uma dúvida corriqueira sobre os codinomes a linguagem e o interpretador, Python e CPython:

### Python é interpretado ou compilado? A questão não é realmente bem formulada.
Dito isso, para a implementação mais comum (CPython: escrita em C, frequentemente referenciada simplesmente como 'Python', e certamente o que você está usando se você não tem ideia do que estou falando), a resposta é: interpretada , com alguma compilação . CPython compila** código fonte Python para bytecode, e depois *interpreta este bytecode, executando conforme progride.

> Nota: isto não é 'compilação' no sentido tradicional da palavra. Normalmente, diríamos que 'compilação' é pegar uma linguagem de alto nível e convertê-la para código de máquina. Mas é uma certa 'compilação'.
Em Python, o interpretador e compilador estão relacionados e coexistem. O interpretador CPython, que é a implementação de referência da linguagem Python, realiza ambos os papéis em conjunto. Isso é conhecido como interpretação just-in-time (JIT) e compilação.

### Bytecode vs. Código de Máquina

É muito importante entender a diferença entre bytecode e código de máquina (ou nativo), talvez melhor ilustrado pelo exemplo:

C compilado para código de máquina, que é depois executado diretamente no seu processador. Cada instrução instrui sua CPU a realizar coisas por toda parte.

Compilação Java para bytecode, que depois é executada na Java Virtual Machine (JVM), uma abstração de um computador que executa programas. Cada instrução é então tratada pela JVM, que interage com seu computador.

*Em termos breves: o código da máquina é muito mais rápido, mas o bytecode é mais portátil e seguro .*

O código de máquina parece diferente dependendo de sua máquina, mas o bytecode parece igual em todas as máquinas. Alguém pode dizer que o código da máquina é otimizado para sua configuração.

### Voltando ao CPython, o processo de toolchain é como segue:

> toolchain: É um conjunto de ferramentas de programação usadas para executar uma tarefa complexa de desenvolvimento de software.

- CPython compila seu código fonte Python para bytecode.
- Este bytecode foi então executado na Máquina Virtual CPython.

Iniciantes assumem que Python é compilado por causa dos arquivos .pyc. Há alguma verdade nisto: o arquivo .pyc é bytecode compilado, que é depois interpretado. Então se você rodou seu código Python antes e tem o arquivo .pyc disponível, ele vai rodar mais rápido na segunda vez, já que não precisa recompilar o bytecode.

Quando você executa um script Python, o interpretador CPython realiza as seguintes etapas:

### Compilação para Bytecode (Modo de Compilação)

O código-fonte Python (.py) é compilado para bytecode Python (.pyc) pelo compilador CPython em tempo de execução. Esse bytecode é uma representação intermediária, entre o codigo nativo e o codigo de máquina. 

### Execução do Bytecode na Máquina Virtual CPython (Modo de Interpretação)

O bytecode gerado é interpretado e executado pela máquina virtual CPython. Durante a execução, o interpretador pode otimizar certas partes do código para melhor desempenho.

Essa combinação de compilação para bytecode e interpretação em tempo real proporciona uma abordagem flexível e portável para a execução de código Python. 

### Conclusão

Portanto, não é necessário que os desenvolvedores executem explicitamente um processo de compilação separado antes de executar um script Python. O interpretador CPython cuida disso automaticamente. Essa abordagem simplifica o desenvolvimento, pois os desenvolvedores podem se concentrar no código-fonte sem se preocupar com o processo de compilação.

O Python utiliza um processo de compilação just-in-time (JIT), onde o código fonte é compilado para um bytecode em tempo de execução.

> \- É correto falar que o Python é compilado em tempo real de execução ?
\- Sim!

Fonte -> https://www.toptal.com/python/por-que-h-tantos-pythons

## Ciclo de Vida do Código em Python Em Scripts, Passo a Passo.
O ciclo de vida do código Python pode ser dividido em três fases principais.

### Nascimento
Criação do Código: Desenvolvedores escrevem o código em um editor de texto ou IDE.
Salvamento do Arquivo: O código é salvo em um arquivo .py.

### Execução
Interpretação e Compilação para Bytecode: O interpretador Python lê e converte (compila) o código-fonte em bytecode durante a interpretação.

Execução do Bytecode: A Máquina Virtual CPython executa diretamente o bytecode gerado, realizando as instruções do programa, assim se tornando uma linguagem multiplataforma. 

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

Se você muda o valor da variável, está apenas trocando o que está dentro dessa caixa na memória. Porém o indentificador da memoria permanece. 

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
Saída/Resultado:

`Idade: 25`

`Idade: 26`

## Tipos

Tipo é a abstração da característica de um dado. 

- Se um dado tem a característica numeral, ele poderá ser do tipo inteiro, real…
- Se tiver a característica de caracteres poderá ser uma string, um caráter único… 
- Se a característica for de um valor verdadeiro ou falso o tipo será booleano. 

Desta forma o tipo de dado altera o comportamento do interpretador, para realizar operações com o determinado valor. 

Exemplos de tipos de dados em python:                                                                   

Em Python, os tipos de dados são essenciais para representar diferentes tipos de valores e realizar operações específicas. Abaixo estão alguns dos tipos de dados mais comuns em Python, juntamente com suas usuabilidades:

**Inteiro (int):**
- Representa números inteiros.
- Usado em operações aritméticas.
- `idade = 25`

**Ponto Flutuante (float):**
- Representa números decimais ou de ponto flutuante.
- Utilizado em cálculos que envolvem números fracionários.
- `altura = 1.75`

**String (str):**
- Representa sequências de caracteres.
- Usado para manipulação de texto.
- `nome = "João"`

**Booleano (bool):**
- Representa valores lógicos (True ou False).
- Usado em expressões condicionais e controle de fluxo.
- `esta_chovendo = False`

**Lista (list):**
- Armazena uma coleção ordenada de elementos mutáveis.
- Útil para armazenar e manipular conjuntos de dados.
- `numeros = [1, 2, 3, 4, 5]`

**Tupla (tuple):**
- Similar a uma lista, mas é imutável (não pode ser alterada após a criação).
- Usada quando se deseja garantir que os dados não sejam modificados.
- `coordenadas = (10, 20)`

**Dicionário (dict):**
- Armazena pares chave-valor.
- Útil para representar dados estruturados e acessar valores por meio de chaves.
- `pessoa = {"nome": "Maria", "idade": 30}`

**Conjunto (set):**
- Armazena elementos únicos e não ordenados.
- Útil para operações de conjunto, como união e interseção.
- `cores = {"vermelho", "verde", "azul"}`

**NoneType (None):**
- Representa a ausência de valor.
- Usado para indicar a falta de um valor em variáveis ou funções.
- `resultado = None`

Esses são alguns dos tipos de dados fundamentais em Python. A escolha do tipo de dado depende do contexto e da tarefa que você está realizando. Python é uma linguagem dinamicamente tipada, o que significa que você não precisa declarar explicitamente o tipo de uma variável; o interpretador faz isso automaticamente.

## Função `type()`
Podemos saber o tipo de determinada variável com a função type, na qual determina o tipo da variável.
```
python # para abrir o modo interativo no seu shell

idade = 22

print(type(idade)) # A função print serve para imprimir no console uma saída de um script, como estamos no modo interativo ela não é necessária nesse contexto.

type(idade) # Contém o mesmo retorno no modo interativo

```
O resultado será:  `<class 'int'> `

A função pode ser utilizada para descobrir qualquer tipo de variável.

## **Input e Casting**

- **Input**: A função `input()` é usada para receber entrada do usuário, retornando a entrada como uma string. Por exemplo, `nome = input("Digite seu nome:")`.

- **Casting**: Para converter uma string em outro tipo de dado (por exemplo, de string para inteiro), você pode usar funções de casting como `int()`, `float()`, etc. Por exemplo, `numero_str = input("Digite um número:")` e `numero_int = int(numero_str)`.

Lembre-se de que a entrada do usuário por meio de `input()` é sempre uma string, e você precisa realizar casting para o tipo desejado, se necessário.

## Introduzindo operadores

## Operadores Aritméticos

Em Python, os operadores aritméticos são utilizados para realizar operações matemáticas em variáveis e valores. Abaixo estão alguns dos operadores aritméticos comuns:

- **Adição `+`**: Soma dois valores. Por exemplo, `operacao = 5 + 3` resulta em 8.

- **Subtração `-`**: Subtrai o valor do lado direito do valor do lado esquerdo. Por exemplo, `operacao = 5 - 3` resulta em 2.

- **Multiplicação `*`**: Multiplica dois valores. Por exemplo, `operacao = 5 * 3` resulta em 15.

- **Divisão `/`**: Divide o valor do lado esquerdo pelo valor do lado direito. Por exemplo, `operacao = 10 / 2` resulta em 5.0.

- **Divisão Inteira `//`**: Divide e retorna a parte inteira. Por exemplo, `operacao = 10 // 3` resulta em 3.

- **Módulo `%`**: Retorna o resto da divisão. Por exemplo, `operacao = 10 % 3` resulta em 1.

- **Exponenciação `**`**: Eleva um valor à potência de outro. Por exemplo, `operacao = 2 ** 3` resulta em 8.

### Ordem de Prioridade das Operações em Python

A ordem de prioridade das operações em Python segue as regras convencionais da matemática. Aqui está uma lista, da mais alta para a mais baixa prioridade:

1. **Parênteses `()`**: Expressões dentro de parênteses têm a maior prioridade. Qualquer operação dentro de parênteses é avaliada primeiro.

2. **Exponenciação `**`**: A exponenciação tem a segunda maior prioridade. Por exemplo, `2 ** 3` é avaliado antes de outras operações.

3. **Negativo unário `-` e positivo unário `+`**: O sinal negativo unário e positivo unário têm a terceira maior prioridade.

4. **Multiplicação `*`, Divisão `/`, Divisão Inteira `//`, Módulo `%`**: Essas operações têm a mesma prioridade e são avaliadas da esquerda para a direita.

5. **Adição `+` e Subtração `-`**: Adição e subtração têm a menor prioridade e também são avaliadas da esquerda para a direita.

A utilização de parênteses pode ser usada para alterar a ordem de avaliação padrão e forçar uma determinada parte da expressão a ser avaliada primeiro.

## Operadores de comparação
Os operadores de comparação em Python são usados para comparar dois valores e produzir um resultado booleano (True ou False). Aqui estão alguns exemplos dos operadores de comparação com explicação. 

- `valor1 = 10`
- `valor2 = 5`

**Operador de Igualdade (`==`):**
- `resultado_igual = valor1 == valor2  # False, pois 10 não é igual a 5`

**Operador de Diferença (`!=`):**
- `resultado_diferente = valor1 != valor2  # True, pois 10 é diferente de 5`

**Operador de Maior que (`>`):**
- `resultado_maior = valor1 > valor2  # True, pois 10 é maior que 5`

**Operador de Menor que (`<`):**
- `resultado_menor = valor1 < valor2  # False, pois 10 não é menor que 5`

**Operador de Maior ou Igual a (`>=`):**
- `resultado_maior_igual = valor1 >= valor2  # True, pois 10 é maior ou igual a 5`

**Operador de Menor ou Igual a (`<=`):**
- `resultado_menor_igual = valor1 <= valor2  # False, pois 10 não é menor ou igual a 5`


## Operadores Lógicos

Esses operadores lógicos são úteis em situações onde você precisa tomar decisões com base em múltiplas condições. Eles ajudam a construir uma lógica mais complexa em seus programas, permitindo que você modele diferentes cenários de forma clara e eficiente. Retornando sempre um valor booleano (bool).

**Operador Lógico AND (`and`):**
- `tem_sol = True`
- `folga = True`
- `vamos_ao_parque = tem_sol and folga  # True, porque temos tempo ensolarado e estamos de folga`

**Operador Lógico OR (`or`):**
- `frio = True`
- `chocolate_quente = True`
- `queremos_bebida_quente = frio or chocolate_quente  # True, porque está frio lá fora OU temos chocolate quente em casa`

**Operador Lógico NOT (`not`):**
- `esta_chovendo = True`
- `nao_esta_chovendo = not esta_chovendo  # False, porque estamos invertendo a condição de "está chovendo"`

## Prática dos assuntos abordados.


**Exercícios sobre Variáveis e Tipos de Dados:**

1. Crie uma variável chamada `nome` e atribua a ela o seu próprio nome. Em seguida, imprima a mensagem "Olá, [nome]!".

2. Declare uma variável chamada `numero` e atribua a ela um número inteiro. Em seguida, imprima o dobro desse número.

3. Crie uma variável chamada `preco` e atribua a ela um valor decimal representando o preço de um produto. Imprima o preço com um desconto de 10%.

4. Declare uma variável chamada `booleano` e atribua a ela um valor booleano (True ou False). Em seguida, imprima o valor oposto usando o operador lógico NOT.

**Exercícios sobre Input e Casting:**

5. Peça ao usuário para digitar um número. Armazene o valor na variável `entrada` e imprima o quadrado desse número.

6. Solicite ao usuário que insira sua idade como uma string. Converta a string para um número inteiro e imprima a idade.

**Exercícios sobre Operadores Aritméticos:**

7. Declare duas variáveis, `lado1` e `lado2`, representando os lados de um retângulo. Calcule e imprima a área do retângulo.

8. Peça ao usuário para digitar um número decimal. Arredonde esse número para cima e para baixo e imprima os resultados.

**Exercícios sobre Operadores de Comparação:**

10. Declare duas variáveis, `temperatura_atual` e `limite_frio`, representando a temperatura atual e o limite para estar frio. Verifique se está frio (abaixo do limite) e imprima o resultado como true ou false.

11. Peça ao usuário para inserir dois números. Compare os números e imprima uma mensagem indicando qual é o maior.

**Exercícios sobre Operadores Lógicos:**

12. Crie variáveis `tem_sol` e `tem_calor`, representando se está ensolarado e se está calor. Use operadores lógicos para determinar se é um bom dia para ir à praia.

13. Declare uma variável `idade` e verifique se a pessoa é elegível para votar (idade maior ou igual a 18) e se é um número par. Imprima o resultado.

Esses exercícios ajudarão a praticar conceitos básicos de Python, desde variáveis e tipos de dados até operadores e lógica condicional.

## Python: Saída de Dados

### 1. Função `print()`

A função `print` é usada para exibir informações na tela. É uma maneira simples de interagir com o usuário ou visualizar resultados de código. Você pode passar strings, variáveis ou expressões como argumentos para a função `print`.

Exemplo:
```python
print("Olá, Mundo!")
```
Neste exemplo, a função `print` exibe a mensagem "Olá, Mundo!" na tela.

### 2. Parâmetro `.format`

O método `.format` é utilizado para formatar strings de uma maneira mais dinâmica, permitindo a inserção de valores em posições específicas na string.

Exemplo:
```python
nome = "Alice"
idade = 25
print("Olá, meu nome é {} e tenho {} anos.".format(nome, idade))
```
Neste exemplo, `{}` são espaços reservados que serão preenchidos pelos valores de `nome` e `idade` na ordem em que são fornecidos para o método `.format`.

### 3. F-strings (Formated String Literals)

As f-strings são uma maneira mais recente e concisa de formatar strings no Python. Elas começam com o prefixo `f` antes da string e permitem a incorporação direta de variáveis ou expressões dentro da string.

Exemplo:
```python
nome = "Bob"
idade = 30
print(f"Olá, meu nome é {nome} e tenho {idade} anos.")
```
As variáveis dentro das chaves `{}` são substituídas pelos valores correspondentes.

### 4. Saída de Dados Amigável

#### Arredondamento de Números
O exemplo abaixo demonstra como arredondar números para um número específico de casas decimais usando a f-string:

```python
pi = 3.14159
print(f"O valor de pi é aproximadamente {pi:.2f}")
```
Neste caso, `:.2f` significa que o número será formatado como um float com duas casas decimais.

#### Caracteres de Escape
Os caracteres de escape são usados para representar sequências especiais, como quebras de linha. Por exemplo:

```python
print("Quebra de linha:\nSegunda linha.")
```
O `\n` representa uma quebra de linha.

#### Atalhos Úteis
O atalho `\t` é utilizado para inserir uma tabulação:

```python
print("Item\tQuantidade\tPreço")
print("Laptop\t2\t\t$1000")
```
A `\t` cria um espaço equivalente a uma tabulação, útil para organizar colunas.

Neste exemplo, as aspas duplas dentro da string são escapadas usando a barra invertida `\`. Isso permite que elas sejam tratadas como parte da string, em vez de indicar o fim da string. O mesmo princípio se aplica a outros caracteres especiais que podem interferir na formatação da string.

```python
mensagem = "Eu sou uma string com aspas \"duplas\" dentro."
print(mensagem)
```

Esses conceitos são fundamentais para a produção de saídas de dados legíveis e informativas em Python. À medida que você avança na programação, essas técnicas se tornam ferramentas poderosas para comunicar informações de maneira eficaz.

## Python: Desvios Condicionais


### Por que Desvios Condicionais?

Vamos imaginar um programa como um semáforo de trânsito. Em alguns momentos, ele exibe a luz verde, indicando que é seguro avançar. Em outras situações, mostra a luz vermelha, sinalizando a necessidade de parar. Os desvios condicionais em programação são como as regras para o semáforo: "Se a luz estiver verde, avance; senão, espere."

### Estrutura Básica:

Blocos em Python são marcados pelo uso do caractere `:`. Eles indicam o início de um bloco de código associado a uma estrutura, como `if` ou `else`.

A indentação (espaço antes das linhas de código) é crucial. Ela define o escopo do bloco. Tudo que está indentado sob um `if` pertence a ele. A indentação é como o Python entende o que está dentro ou fora do bloco.

```python
if condição:
    # o espaço inicial desta linha é a indentação.
    # faça algo se a condição for verdadeira.
else:
    # faça algo se a condição for falsa
```

### Exemplo no Mundo Real:

Vamos usar um exemplo cotidiano: decidir se você deve levar um guarda-chuva ao sair. A condição seria "se estiver chovendo". Vamos traduzir isso para Python:

```python
clima = input("Está chovendo hoje? (sim/não): ")

if clima.lower() == "sim":
    print("Leve um guarda-chuva!")
else:
    print("Você pode sair sem guarda-chuva.")
```

Neste exemplo:
- `clima.lower()` converte a entrada do usuário para minúsculas, garantindo que "SIM" ou "sim" sejam tratados da mesma forma.

### Dinâmica:

Agora, imagine que a condição seja mais complexa. Digamos que você também quer levar o guarda-chuva se houver previsão de chuva. Isso nos leva aos operadores lógicos (`and`, `or`, `not`).

```python
clima = input("Está chovendo hoje? (sim/não): ")
previsao_chuva = input("Há previsão de chuva? (sim/não): ")

if clima.lower() == "sim" or previsao_chuva.lower() == "sim":
    print("Leve um guarda-chuva!")
else:
    print("Você pode sair sem guarda-chuva.")
```

### Poder na Simplicidade:

Desvios condicionais tornam o código flexível. Imagine um jogo onde o jogador só pode avançar se tiver uma chave. Sem desvios condicionais, o jogo seria estático. Com eles, você pode criar experiências dinâmicas.

### Dica Útil:

Use desvios condicionais para lidar com diferentes cenários. Eles tornam seu código mais inteligente, eficiente e fácil de entender.

### Explorando o elif:

Agora, vamos adicionar mais complexidade usando `elif` (abreviação de "else if"). Ele permite testar várias condições em sequência. 

 
- *if = se*
- *elif = se não se* 
- *else= se não*

```python
hora = int(input("Que horas são? "))

if hora < 12:
    print("Bom dia!")
elif 12 <= hora < 18:
    print("Boa tarde!")
else:
    print("Boa noite!")
```

Neste exemplo, o programa saúda o usuário com base na hora do dia.

### Utilizando Múltiplos elif:

Vamos criar um programa que avalia a nota de um aluno:

```python
nota = float(input("Digite a nota do aluno: "))

if nota >= 9:
    print("Nota A")
elif 7 <= nota < 9:
    print("Nota B")
elif 5 <= nota < 7:
    print("Nota C")
elif 3 <= nota < 5:
    print("Nota D")
else:
    print("Nota F")
```

Aqui, cada `elif` testa uma faixa diferente de notas. Aonde a condição for verdadeira, ela será executada e será encerrado o programa.
