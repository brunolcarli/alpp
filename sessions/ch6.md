# Capítulo 6

<p align="justify">

</p>

## Sub-rotinas e programação com arquivos

<p align="justify">
Vamos conhecer neste capítulo os conceitos de sub- rotinas que nada mais são do que partes do nosso algoritmo que podem ser reaproveitadas sem termos que reescreve-las diversas vezes sempre que necessário, facilitando a depuração, manutenção e aumentando a legibilidade do nosso código. Para entender estes conceitos também será necessário compreender o escopo das variáveis, como variáveis globais e locais, tema que também será abordado neste capítulo.
</p>

<p align="justify">
Outro ponto a ser estudado neste capítulo será a manipulação de arquivos com Python, abordando elementos de inserção, leitura e remoção de dados oriundos de um arquivo guardado no disco rígido do seu computador, permitindo assim que os dados que trabalhamos fiquem armazenados de forma permanente.
</p>

## Sub-rotinas

<p align="justify">
Uma sub-rotina é uma parte do algoritmo que pode ser utilizada diversas vezes sem que tenhamos que reescrever o código cada vez que seja necessário executar uma determinada tarefa. Ascencio e Campos (2010, p. 230) define as sub-rotinas como “blocos de instruções que realizam tarefas específicas”. Leal (2016a, p. 166) comenta que as sub-rotinas são responsáveis por diminuir a complexidade de determinados problemas, desta forma reduzimos um grande problema em pequenas partes, ou subproblemas, facilitando sua resolução. Desta forma utiliza-se as sub-rotinas para executar os subproblemas tratando cada parte complexa individualmente.
</p>

><small>Uma sub-rotina é carregada apenas uma vez e pode ser executada quantas vezes for necessário, podendo ser utilizada para economizar espaço e tempo de programação. Em cada sub- rotina, além de ter acesso às variáveis do programa que o chamou (variáveis globais), pode ter suas próprias variáveis (variáveis locais), que existem apenas durante sua chamada. (LEAL, 2016a)
</small>


<p align="justify">
Na literatura encontramos as sub-rotinas em duas formas: Procedimentos e Funções, vamos analisar ambas as formas destacando suas características e como utilizá-las em Python.
</p>

## Procedimentos

<p align="justify">
Um procedimento é uma sub-rotina que contém um bloco de instruções a serem executadas a qualquer momento
desejado. Assim como as variáveis, os procedimentos devem possuir um identificador para ser usado na hora de sua chamada. Ao ser chamado durante a execução de um algoritmo, o procedimento executa seus comandos e retorna para o fluxo normal do algoritmo logo após sua chamada, dando continuidade ao programa em execução. O procedimento caracteriza-se por não retornar nenhum valor após sua execução, ele simplesmente executa suas instruções e segue para o próximo comando do algoritmo após ter sido chamado. A sintaxe para declarar um procedimento em Python é a seguinte:
</p>

```python
def identificador( ):
    # bloco de instruções
```

<p align="justify">
A palavra-chave def é utilizada para definir o procedimento, no identificador atribuímos um nome para o procedimento, seguindo as regras para nomenclatura de identificadores já abordado no início deste livro, em seguida abrimos e fechamos parênteses para caracterizar o procedimento e finalizamos com dois pontos (:). Após os dois pontos serão declaradas as instruções do procedimento, estas deverão ser indentadas para que o Python reconheça que as instruções pertencem ao bloco do procedimento. Veja um exemplo em Python para um procedimento que exibe a mensagem “Ola mundo”:
</p>

```python
def olamundo(): # definimos um procedimento
    print("Ola mundo") # instrução do procedimento

olamundo() # chamada do procedimento
```

<p align="justify">
Definimos um procedimento chamado olamundo( ), no seu bloco de comandos temos a instrução print( ). O procedimento executa a instrução print( ) declarada em seu bloco de comandos quando houver a chamada para sua execução. Para chamar um procedimento basta escrevermos seu nome no programa, como no exemplo anterior. Ao chamarmos o procedimento olamundo( ) obtemos a execução dos seus comandos internos, neste caso uma mensagem:
</p>

```
Ola mundo
>>>
```

<p align="justify">
É possível no momento da definição do nosso procedimento, especificar parâmetros para execução do procedimento, estes parâmetros são fornecidos dentro dos parênteses em sua definição, e devem obrigatoriamente ser utilizados no bloco de comandos. Ao chamar o procedimento fornecemos um argumento para o procedimento, os argumentos serão substituídos pelos parâmetros listados na definição e as instruções utilizarão os argumentos na execução do procedimento.
</p>

```python
def cumprimento(nome):
	print("Ola %s, prazer em conhecê-lo" % nome)

cumprimento("Bruno")
```

<p align="justify">
Veja que ao definirmos o procedimento, dentro dos parênteses declaramos um parâmetro chamado nome, este parâmetro está sendo utilizado na mensagem dentro do procedimento. Quando chamamos o procedimento fornecemos um argumento que substituirá o parâmetro nome para ser utilizado na mensagem.
</p>

```
Ola Bruno, prazer em conhecê-lo
>>>
```

<p align="center"><img src="resources/img/box6.png"></p>

<p align="justify">
De acordo com Matthes (2016, p. 187),
parâmetro é um valor que deve ser fornecido para a sub-rotina na hora de sua definição, já o argumento é um valor passado para a chamada da sub-rotina durante a execução do algoritmo. Neste caso, nome é o parâmetro, pois foi declarado no procedimento durante sua definição, e a string 'Bruno' é um argumento que foi passado para o procedimento durante sua chamada na execução do algoritmo.
</p>

<p align="justify">
Leal(2016a) coloca uma distinção entre parâmetros que apresenta os mesmos conceitos acima, como sendo os parâmetros formais aqueles declarados juntamente à sub-rotina e os parâmetros reais aqueles que substituem os parâmetros formais ao chamar a sub-rotina no programa principal (os argumentos). Na literatura estes conceitos caracterizam a distinção entre parâmetro e argumento, ou parâmetro formal e parâmetro real. Vamos exemplificar com mais um procedimento que realiza a soma ou a subtração de dois números:
</p>

```python
def soma(a, b):
	print("O resultado da soma é ", a+b)

def subt(a, b):
	print("O resultado da subtração é ", a-b)

num1 = int(input("Insira o primeiro número: "))
num2 = int(input("Insira o segundo número: "))

print("Qual operação deseja realizar?")
print("[1] Soma\n[2] Subtração")
escolha = int(input())

if escolha == 1:
	soma(num1, num2)

elif escolha == 2:
	subt(num1, num2)

else:
	print("Escolha inválida")

```

<p align="justify">
Definimos inicialmente os procedimentos do algoritmo, ambos recebem dois parâmetros a e b, e quando chamados exibem uma mensagem informando o resultado da operação entre os parâmetros. As primeiras instruções do algoritmo solicitam dois números ao usuário, então pedimos para que faça uma escolha entre soma e subtração, e caso a escolha seja correspondente a soma então chamamos o procedimento de soma e fornecemos os números de entrada como argumentos, ou se a escolha corresponder à subtração então chamamos o procedimento de subtração fornecendo as entradas como argumentos.
</p>

```
Insira o primeiro número: 5
Insira o segundo número: 3
Qual operação deseja realizar?
[1] Soma
[2] Subtração
1
O resultado da soma é  8
>>>
Insira o primeiro número: 5
Insira o segundo número: 3
Qual operação deseja realizar?
[1] Soma
[2] Subtração
2
O resultado da subtração é  2
>>>
```

<p align="justify">
Você já conheceu aqui algumas formas interessantes de se construir algoritmos, implemente este último exemplo adicionando dois novos procedimentos para divisão e multiplicação. Implemente também um laço que pergunta ao usuário se gostaria de realizar outra operação ao final do algoritmo. Implemente também um laço que verifica se a entrada do usuário é válida (um valor numérico) e caso seja inválido fique repetindo a solicitação até que um valor válido seja inserido.
</p>

## ~~Funções~~

## ~~Parâmetros~~

## ~~Escopo das variáveis~~

## ~~Recursividade~~

## ~~Arquivos~~

## ~~Bibliotecas e módulos~~
