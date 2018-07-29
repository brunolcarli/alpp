# Capítulo 5

## Estruturas de dados

<p align="justify">
As estruturas de dados em lógica de programação são
responsáveis por permitir que agrupemos diversos tipos de dados em uma única variável, em outras linguagens é comum que estas estruturas sejam divididas em homogêneas e heterogêneas, pois há estruturas específicas para agrupar um
único tipo de dado (como uma lista enorme de números inteiros), porém no Python é possível misturar diferentes tipos em uma única lista, desta forma pode-se dizer que as estruturas
de dados em Python são praticamente todas heterogêneas, mas nada lhe impede de criar listas somente de inteiros ou somente
de literais.
</p>

<p align="justify">
Até agora estávamos armazenando os valores em
variáveis separadas, mas existem momentos em que
precisamos armazenar muitos dados, o que nos exigiria a declaração de inúmeras variáveis. “Suponha, por exemplo, o caso de um treino de classificação de uma corrida de Fórmula 1, em que é necessário verificar os tempos obtidos por todos os pilotos para avaliar qual será o primeiro no grid de largada. Para fazer essa ordenação, é necessário armazenar o tempo de todos os pilotos e, depois, realizar a ordenação desses tempos.”(PUGA; RISSETTI, 2010 p. 83), já pensou quantas variáveis precisaríamos criar? Uma para cada piloto, mais uma para cada tempo, isso exigiria muito consumo de memória do computador, e seria desnecessário já que possuímos as estruturas de dados para agrupar todos estes valores. Vamos conhecer as estruturas de dados em Python.
</p>

## Estruturas de dados unidimensionais

<p align="justify">
Em lógica de programação, as estruturas
unidimensionais são popularmente conhecidas como vetores, vetor é uma estrutura de dados unidimensional (ASCENCIO; CAMPOS, 2010), unidimensional porque ela possui apenas uma dimensão linear onde os dados serão listado um após o outro em sequência.
</p>
<p align="justify">
Em Python estas estruturas são denominadas listas, e assim como uma lista comum os itens serão incluídos e identificados por um índice que corresponde à sua localização na lista.
</p>

<quote><small><p align="justify">
Uma lista é uma coleção de itens em uma ordem em particular. Podemos criar uma lista que inclua as letras do alfabeto, os dígitos de 0 a 9 ou os nomes de todas as pessoas de sua família. Você pode colocar qualquer informação que quiser em uma lista, e os itens de sua lista não precisam estar relacionados de nenhum modo em particular. (MATTHES, 2016 p. 70)
</p></small></quote>

<p align="justify">
Vamos exemplificar isto com uma situação bem
comum. Suponha que sua mãe pediu para que você fosse ao mercado e comprasse bananas, queijo, trigo e uma lata de azeite. Logo você pega um pedaço de papel e anota:
</p>

1 – Banana;

2 – Queijo;

3 – Trigo;

4 – Azeite;

Vamos fazer a mesma lista em Python agora:

```python
# criamos nossa lista
lista = ['banana', 'queijo', 'trigo', 'azeite']

# exibe o conteúdo da lista
print(lista)
```

Saída:

```
['banana', 'queijo', 'trigo', 'azeite']
>>>
```

A sintaxe para criar uma lista em Python é:

`identificador = [conteúdo]`

<p align="justify">
Em Python as listas são definidas por um par de [ ], e os itens que estiverem dentro dos colchetes pertencem a lista, mais de um item deve ser separado por vírgula. Veja no exemplo anterior que guardamos quatro valores literais dentro
de uma única variável e quando chamamos esta variável na instrução print( ) o Python nos diz todos os valores que existem nessa variável. Nós podemos verificar quantos itens existem em uma lista com a instrução len( ).
</p>

```python
# criamos nossa lista
lista = ['banana', 'queijo', 'trigo', 'azeite']

# exibe o número de itens na lista
print(len(lista))
```

Saída:

```
4
>>>
```

<p align="justify">
Desta forma ao trabalharmos com listas muito extensas em que precisamos verificar a quantidade de itens nesta lista basta passarmos a lista como parâmetro para a instrução len( ).
</p>

<p align="justify">
Agora vamos supor que antes de você sair para o
mercado sua mãe lhe diz que esqueceu de dizer que é pra você trazer cenouras também, então você precisa adicionar mais um item em sua lista, para fazer isto no Python basta utilizar o comando .append( ) com o nome do item a ser adicionado entre os parênteses, desta forma:
</p>

```python
# lista inicial
lista = ['banana', 'queijo', 'trigo', 'azeite']

# verifique o tamanho da lista
print(len(lista))
# verifique os itens da lista
print(lista)

# adicione a cenoura no fim da lista
lista.append("cenoura")

# verifique novamente o tamanho da lista
print(len(lista))

# verifique novamente os itens da lista
print(lista)
```
<p align="justify">
Utilizamos as instruções len( ) para verificar que a lista aumentou de tamanho, escrevemos antes e depois de adicionar o item para verificar que as alterações foram feitas com sucesso. Agora você já pode ir ao mercado comprar as coisas para sua mãe.
</p>

```
4
['banana', 'queijo', 'trigo', 'azeite']
5
['banana', 'queijo', 'trigo', 'azeite', 'cenoura']
>>>
```

<p align="justify">
Ao chegar no mercado você colocou em sua cestinha a
banana e o azeite, e resolveu riscar da sua lista os itens que você já pegou para não acabar se perdendo. Para remover um item conhecido de sua lista basta escrever o item a ser removido como parâmetro na instrução .remove( ), desta forma:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# removemos a banana
lista.remove('banana')
# removemos o azeite
lista.remove('azeite')

# verificamos quais itens ainda estão na lista
print(lista)
```
Saída:

```
['queijo', 'trigo', 'cenoura']
>>>
```

<p align="justify">
No começo deste capítulo foi dito que as estruturas de dados em Python são heterogêneas, o que significa que podemos misturar tipos de dados em uma única lista. Nos exemplos anteriores fizemos uma lista de literais, mas é possível inserir dados de tipos distintos em uma mesma lista Python. Veja neste exemplo:
</p>

```python
# criamos um vetor vazio
meus_dados = []

# solicitamos que o usuário insira o nome
nome = input("Insira seu nome: ")

# inserimos o nome no vetor
meus_dados.append(nome)

# solicitamos a idade
idade = int(input("Insira sua idade: "))

# inserimos a idade no vetor
meus_dados.append(idade)

# solicitamos a altura
altura = float(input("Insira sua altura: "))

# inserimos a altura no vetor
meus_dados.append(altura)

# exibimos o conteúdo do vetor
print(meus_dados)
```

<p align="justify">
Primeiro criamos uma lista vazia com o identificador meus_dados, para criar uma lista vazia basta atribuir os colchetes vazios [], então fazemos as solicitações de entrada de três tipos de dados diferentes um literal (nome) um inteiro (idade) e um real (altura), adicionando cada um deles em nossa lista, no final do algoritmo escrevemos o conteúdo da lista.
</p>

```
Insira seu nome: Bruno
Insira sua idade: 27
Insira sua altura: 1.63
['Bruno', 27, 1.63]
>>>
```

<p align="justify">
Veja como as listas em Python suportam diferentes tipos de dados, por este motivo são caracterizadas como heterogêneas, diferentemente dos vetores em algumas linguagens de programação como C por exemplo, que somente aceitam dados de um único tipo. Dissemos também no início deste capítulo que os itens da lista são identificados por um índice, assim podemos pedir para o Python um determinado elemento da lista pelo índice. Se você se lembrar bem, o Python começa a contar do zero, isso também se aplica as listas, logo o primeiro índice da lista é 0, e todos os elementos na sequência seguem a numeração do índice. A nossa lista de compras dos primeiros exemplos possui no índice 0 o item “banana”, no índice 1 o item “queijo”, no índice 2 o item “trigo” e assim por diante. Para que o Python identifique o item pelo índice basta escrever o nome da lista seguido pelo índice entre colchetes, desta forma:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# exibe o item com indice 0
print(lista[0])

# exibe o item com indice 4
print(lista[4])
```

Saída:

```
banana
cenoura
>>>
```

<p align="justify">
Perceba que apesar de nossa lista possuir 5 elementos, o último elemento da lista é representado pelo índice 4, é bem comum o Python retornar um erro ao passarmos um índice inexistente para ele, necessitando um pouco de cuidado ao solicitar os elementos pelo índice. No exemplo anterior pedimos que o Python escrevesse o item da posição 0 e da posição 4, e caso não existisse uma posição 4, o Python retornaria um erro:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# exibe o item com indice 0
print(lista[0])

lista.remove("cenoura")

# exibe o item com indice 4
print(lista[4])
```

Saída:

```
banana
Traceback (most recent call last):
  File "x.py", line 10, in <module>
    print(lista[4])
IndexError: list index out of range
>>>
```

<p align="justify">
Neste exemplo, ao pedirmos que o Python escreva a
posição 0 ocorre tudo bem, ele escreve “banana”, mas quando o algoritmo chegar a instrução que solicita ao Python para escrever a posição 4 ele retornará um Traceback do tipo IndexError, pois antes desta instrução havíamos removido o
item da posição 4, e como não haviam mais itens na sequência, a posição do índice 4 ficou inexistente. Ao tentar analisar isto o Python tenta nos dizer “ei programador esse índice não existe”.
</p>
<p align="justify">
Quando você não tiver certeza de quantos elementos
possui a lista, mas mesmo assim quiser verificar o último elemento da lista, basta utilizar [-1] como índice, e o Python irá buscar o último item da lista, independente de quantos elementos ela possua:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# exibe o item com indice 4
print(lista[0])

lista.remove("cenoura")

# exibe o último item da lista
print(lista[-1])
```

Saída:

```
azeite
>>>
```


<p align="justify">
Através dos índices também é possível alterar o
conteúdo da lista fazendo uma nova atribuição ao índice, isto irá sobrescrever o elemento armazenado naquela posição, veja:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

lista[0] = "sorvete"
lista[1] = "chocolate"
lista[2] = "pizza"
lista[3] = "coxinha"
lista[4] = "pão de queijo"

print(lista)
```

Saída:

```
['sorvete', 'chocolate', 'pizza', 'coxinha', 'pão de queijo']
>>>
```

<p align="justify">
Modificamos todas as posições da lista e atribuímos
novos valores a cada posição do índice, essa lista parece ter ficado bem mais gostosa, mas infelizmente não é o que sua mãe pediu pra você comprar.
</p>
<p align="justify">
Uma das formas mais comum de se trabalhar com listas é iterar através do laço <b>for</b>, assim podemos analisar item por item da lista, veja:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# para cada item na lista
for item in lista:
    # exiba o item da lista na tela
    print(item)
```

Saída:

```
banana
queijo
trigo
azeite
cenoura
>>>
```

<p align="justify">
Com o loop percorremos cada um dos elementos e
vamos escrevendo-o na tela. O for é o mais comum de se utilizar porém é perfeitamente possível fazer o mesmo com o loop while, você saberá quando utilizar um ou outro no decorrer de seus algoritmos. Da mesma forma que podemos percorrer a lista com um laço, também é possível verificar se um determinado item existe na lista com uma estrutura condicional, como no exemplo a seguir:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# se houver queijo na lista
if "queijo" in lista:
    # diga que há queijo na lista
    print("Queijo está na lista!")
```

Saída:

```
Queijo está na lista!
>>>
```

<p align="justify">
Viu como é fácil trabalhar com listas em Python?
Vamos ver mais uma função bacana para se utilizar nas listas, o método sort( ). Com este comando podemos ordenar nossa lista de forma organizada, no exemplo a seguir vamos organizar a nossa lista de compras em ordem alfabética:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# organiza a lista em ordem alfabética
lista.sort()

# escreve a lista
print(lista)
```

Saída:

```
['azeite', 'banana', 'cenoura', 'queijo', 'trigo']
>>>
```

<p align="justify">
É possível fazer o inverso e organizar os itens da lista de trás para frente com o método .reverse( ), assim a lista será invertida ao contrário, como neste exemplo:
</p>

```python
lista = ['banana', 'queijo', 'trigo', 'azeite', 'cenoura']

# inverte a lista ao contrário
lista.reverse()

# exibe a lista
print(lista)
```

Saída:

```
['cenoura', 'azeite', 'trigo', 'queijo', 'banana']
>>>
```

<p align="justify">
Tanto o método sort( ) como o reverse( ) também
funcionam com listas numéricas, se o conteúdo da sua lista for composto de diversos números aleatórios desordenados, basta chamar o método sort( ) para organiza-los de forma crescente, e caso queira ordena-los em forma decrescente basta chamar o método sort( ) depois o método reverse( ). Tente fazer isto!
</p>
<p align="justify">
Existe uma outra forma de criar uma lista, através da instrução <b>list( )</b> passando como parâmetro a instrução <b>range( )</b> contendo o tamanho desejado para sua lista, desta forma:
</p>

```python
# cria uma lista com 10 elementos
minha_lista = list(range(10))

# exibe o conteúdo da lista
print(minha_lista)
```

<p align="justify">
A instrução list() combinada com a instrução range( ) criam uma lista de números inteiros automaticamente, lembrando que o Python começa a contar do zero, sabendo que nosso range é 10 a lista deverá conter uma sequência de 0 a 9:
</p>

```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>>
```

<p align="justify">
Uma outra forma peculiar, e bem eficiente de se criar uma lista é utilizando um loop for dentro da lista. Isso em Python é chamado <i>list comprehension</i>, muito em breve você estará familiarizado com estes conceitos "pythonicos", veja um exemplo:
</p>


```python
# cria uma lista com 10 elementos
minha_lista = [numeros for numeros in range(10)]

# exibe o conteúdo da lista
print(minha_lista)
```

O resultado seria o mesmo que o anterior:

```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>>
```

<p align="justify">
Você se recorda do algoritmo de soma? Bom o Python
tem uma função embutida chamada sum( ), que faz exatamente a mesma coisa, soma os números entre parênteses, mas uma característica interessante desta instrução é que ela pode receber uma lista de números e retorna como resultado a soma total de todos os números da lista, veja:
</p>

```python
# lista de números
lista = [2, 3, 5]

# passamos a lista para a instrução sum()
total = sum(lista)

print(total)
```

Saída:

```
10
>>>
```

## Estruturas de dados multidimensionais