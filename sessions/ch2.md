# Capítulo 2

## Construindo algoritmos com Python

<p align="justify">
Antes de efetivamente construir nossos algoritmos é
importante sabermos como elaborar um algoritmo. Ascencio e Campos (2010, p. 3) definem um método para construção de algoritmos, sendo estruturado a partir de alguns elementos básicos, dentre eles:
</p>

1. Compreender o problema a ser resolvido;
2. Definir os dados de entrada que deverão ser fornecidos;
3. Definir o processamento, quais operações deverão ser executadas sobre os dados;
4. Definir a saída final, exibindo o resultado obtido através do processamento dos dados;
5. Construir o algoritmo;
6. Testar o algoritmo através de simulações;

<p align="justify">
Vamos realizar cada uma destas etapas e comparar o
último exemplo de algoritmo fornecido (soma de dois
números) em Pseudocódigo e Python para ter uma boa visão de como seria um algoritmo implementado em Python 3:
</p>

1. **Problema a ser resolvido**: Somar dois números;

2. **Dados de entrada**: numero1 e numero2;

3. **Processamento**: Somar o numero1 com o numero2;

4. **Saída**: Exibir o resultado da soma;

5. **Construção do algoritmo**:


| Pseudocódigo | Python |
| ------------ | ------ |
| ALGORITMO: soma | |
| VAR num1,num2,soma:inteiro | |
| INICIO | |
| LEIA(num1) | num1 = input("Insira o primeiro numero ") | 
| LEIA(num2) | num2 = input("Insira o segundo numero ")|
|soma ← num1 + num2 | soma = int(num1) + int(num2)|
| ESCREVA(soma) | print("Resultado: ", soma)|
| FIM. | |


<p align="justify">
Perceba de acordo com a tabela acima que algumas declarações feitas em pseudocódigo não são necessárias em Python.
</p>

<p align="justify">
Para testar o algoritmo abra seu IDLE e selecione na
parte superior a opção <i>File</i> então <i>New File</i>, uma nova janela se abrirá para que você possa escrever o algoritmo, escreva o algoritmo Python apresentado (recomenda-se fortemente que você <b>escreva</b> os comandos ao invés de copiar e colar) então selecione a opção <i>Run</i> e então <i>Run Module</i> na caixa de ferramentas na parte superior da tela, ao executar o algoritmo no IDLE será solicitado que você salve seu programa, então selecione um diretório de sua preferência e salve o arquivo com a extensão .py (uma sugestão é que salve este primeiro algoritmo como soma.py). Após salvar o arquivo, o Python irá executar seu algoritmo e se tudo ocorrer bem sua saída deve ser
parecida com a da Figura 7:
</p>

<p align="center">
Figura 7 – Saída do algoritmo soma.py
</p>

<p align="center">
<img src="resources/img/fig7.png">
</p>

<p align="center">
Fonte: O autor.
</p>

<p align="justify">
Agora vamos entender os comandos utilizados nesse
algoritmo Python, primeiro criamos uma variável num1 (vamos ver mais sobre variáveis adiante) e atribuímos a ela o valor de entrada recebido em input(). O comando input() em Python 3 permite que o usuário entre com um valor que será tratado como string (veremos mais sobre tipos de dados adiante), este comando também permite que um texto seja passado como argumento e exibido na tela, neste caso passamos o texto “Insira o primeiro numero ” como argumento. Quando o interpretador Python ler esta instrução ele vai primeiro exibir o texto ao usuário e ficará aguardando uma entrada, logo que o usuário do sistema fornecer um valor de entrada e confirmar, o interpretador executará a próxima instrução do algoritmo, que será, neste caso, a atribuição de mais um valor de entrada para a variável num2, da mesma forma como fizemos na primeira instrução.
</p>

<p align="justify">
A terceira instrução do algoritmo soma.py irá realizar a operação de processamento que soma num1 e num2 e armazena seu resultado em uma variável chamada soma, para isto utilizamos um método chamado int() que irá dizer ao interpretador Python que durante este processamento as variáveis num1 e num2 devem ser tratadas como números inteiros<sup><small>1</small></sup>.
</p>

<p align="justify">
Por fim a instrução print() diz ao Python para escrever na tela, este é um comando de saída de dados, e exibirá na tela os argumentos que forem fornecido à instrução print(). Neste caso fornecemos um argumento em forma de texto dizendo “O resultado da soma e ” e adicionamos uma vírgula (,) para separar o próximo argumento que foi a variável soma, desta forma o comando de saída exibirá o texto fornecido e o valor guardado na variável soma.
</p>

<hr>
<p align="justify">
<sup><small>1</small></sup> : 
<small>Uma observação importante é que, em Python 3 o comando input( ) vai receber sempre os
dados em formato de cadeia de caracteres (string), sendo tratada como um texto, por este
motivo a necessidade de converter para números os valores isneridos através da instrucão
int( ), em Python 2 o comando input( ) receberia apenas valores numéricos e caso o
usuário entrasse com uma letra ou simbolo o Python retornaria um erro. Em python 2 há
um comando específico para receber entradas de texto chamado raw_input( ). Não se
preocupe com isso por enquanto, mais para frente quando você estiver mais familiarizado
com os tipos de dados isto se tornará mais simples de compreender.</small>
</p>

<hr>

<br />


## Variáveis e tipos de dados


<p align="justify">
Variáveis em Algoritmos e Lógica de Programação são
valores que podem sofrer alterações no decorrer do algoritmo. Ascencio e Campos (2010, p. 7) afirma que “Um algoritmo e, posteriormente, um programa, recebem dados, que precisam ser armazenados no computador para serem posteriormente utilizados no processamento. Esse armazenamento é feito na
memória”, logo, sempre que declaramos uma variável em
nosso algoritmo o computador irá separar um espaço na
memória para que um dado possa ser armazenado ali. Segundo Ascencio e Campos(Op. Cit) uma variável “possui nome e tipo, e seu conteúdo pode variar ao longo do tempo, durante a execução de um programa. Embora uma variável possa assumir diferentes valores, ela só pode armazenar um valor a cada instante”.
</p>

<p align="justify">
Agora vamos fazer uma pequena abstração, imagine um
garoto chamado Pedrinho. Pedrinho possui uma variável
chamada idade que neste exato momento possui o valor 7, representando que Pedrinho tem 7 anos. No seu próximo aniversário Pedrinho completará mais um ano de vida então o valor da sua variável idade será incrementado em um, passando agora a representar o valor 8. Esta pequena analogia demonstra a mutabilidade dos valores guardados em uma variável, que recebe este nome justamente por seus valores variarem ao longo de um algoritmo.
</p>

<p align="justify">
As variáveis sempre guardam valores de um respectivo
tipo de dado, que de acordo com Ascencio e Campos (2010, p.8) os mais comuns são numéricos, lógicos e literais.
</p>


*Numéricos*


<p align="justify">
Os dados do tipo numérico são divididos em duas
categorias: Inteiros e Reais. “Os números inteiros podem ser positivos ou negativos e não possuem parte
fracionária”(ASCENCIO; CAMPOS, 2010), como exemplo de
números inteiros temos:
</p>

<p align="center">
12, -7, 154, 0, -98
</p>

<p align="justify">
Os números Reais são aqueles que possuem uma parte
fracionária e podem ser positivos ou negativos, como por exemplo:
</p>

<p align="center">
3.14, 2.9876, -1.98,  0.765
</p>

<p align="justify">
Uma observação importante deixada por Ascencio e
Campos (2010) é que “os números reais seguem a notação da língua inglesa, ou seja, a parte decimal é separada da parte inteira por um . (ponto) e não por uma , (vírgula)” é importante compreender isso desde o início pois poderá evitar complicações futuras quando implementar seu algoritmo.
</p>

<br />


*Lógicos*


<p align="justify">
Os valores lógicos, também chamados de booleanos
(ASCENCIO; CAMPOS, 2010), somente podem assumir dois
valores: verdadeiro ou falso. Estes são utilizados muitas vezes em comparações lógicas e verificações condicionais (veremos mais sobre isto nos próximos capítulos).
</p>


<br />


*Literais*


<p align="jutify">
Os dados do tipo literal são formados por sequências de caracteres (letras maiúsculas, minúsculas e símbolos) ou por um único caractere(ASCENCIO; CAMPOS, 2010). Este tipo de dado é popularmente chamado de string, sendo representado pelo texto envolto por “aspas”, como no exemplo a seguir:
</p>

<p align="center"> “aluno” </p>
<p align="center"> “Carro”</p>
<p align="center"> “Minha casa é azul”</p>
<p align="center"> “fulano@email.com”</p>
<p align="center"> “12 x 10 =”</p>
<p align="center"> “F$0c!3^y</p>

<p align="justify">
Perceba que mesmo os numerais que estiverem entre
aspas serão identificados como dados literais, e Puga e Rissetti (2010, p. 37) afirmam que “Os números armazenados em uma variável cujo tipo de dado é literal não poderão ser utilizadas
para cálculo”, somente sendo possível realizar operações matemáticas com as variáveis do tipo numérico, desta forma é importante conhecer os tipos de dados que estamos trabalhando.
</p>

><small>Definir o tipo de dado mais adequado para ser armazenado em uma variável é uma questão de grande importância para garantir a resolução do problema. Ao desenvolver um algoritmo, é necessário que se tenha conhecimento prévio do tipo de informação (dado) que será utilizado para resolver o problema proposto. Daí, escolhe-se o tipo adequado para a variável que representa esse valor. (PUGA; RISSETTI, 2010, p. 36)</small>

<p align="justify">
As variáveis também possuem identificadores, que nada
mais são do que o seu próprio nome. Sempre que definimos
uma variável a declaramos com um nome, este nome chama-se
identificador, praticamente todos os comandos possuem
identificadores, o print( ) é um identificador para uma rotina
de exibição de dados por exemplo.
</p>

<p align="justify">
É importante saber que existem algumas regras para
formação dos identificadores, segundo Ascencio e
Campos(2010, p. 9), sendo elas:
</p>

+ Somente podem ser utilizadas letras maiúsculas,
minúsculas, números e o caracter sublinhado ( _ ) no
nome das variáveis;

+ O caractere inicial deve obrigatoriamente ser uma letraou o caractere sublinhado, não se deve começar o nome da variável por números;

+ Não são permitidos espaços em branco nem caracteres especiais (!@#$%^&*+-<>=...) com exceção do
sublinhado ( _ );

+ Não podemos utilizar palavras reservadas, estas são
nomes iguais a outros identificadores como comandos
da linguagem de programação que você estiver
utilizando, nomes de variáveis já declaradas no escopo, etc.

<p align="center">
Tabela 3 – Identificadores válidos e inválidos
</p>


| FORMA VALIDA | Razão | FORMA INVÁLIDA | Razão |
| ------------ | ----- | -------------- | ----- |
| Joao12 | Começa com letras | 8C | Não pode começar com números|
| cpf | Contém somente letras | nome usuario | Não pode conter espaços em branco|
| _nome | Pode começar com *underscore* (_)| True | Não pode conter nomes de palavras reservadas da linguagem (True é uma palavra reservada para um tipo de dado booleano) |
| registro_usuario | Liga duas palavras através de um *underscore* | id-paciente | Não pode conter careacteres especiais (- é um caractere que representa a subtração) |
| NOTA | Caixa alta é permitido | bot@ao | Não é permitido o uso de caracteres especiais (exceto o underscore) |


<p align="center">Fonte: O autor.</p>

<br />


## Variáveis em Python


<p align="justify">
As variáveis em Python são bem flexíveis, se adaptando
ao tipo de dado e alocando espaço dinamicamente na memória. Para atribuir um valor à uma variável utilizamos o operador de atribuição, representado pelo careactere <b>=</b>
</p>


<pre>
    nome = "Edgar Morin"
    idade = 97
    peso = 67.24
</pre>


<p align="justify">
Diferentemente do pseudocódigo e de algumas
linguagens de programação não precisamos declarar o tipo de variável para que o Python a reconheça. Vamos a um exemplo, abra seu IDLE e crie um novo arquivo (<i>File</i> então <i>New File</i>), insira o pequeno trecho a seguir:
</p>


<pre>
    mensagem = "Ola Mundo"
    print(mensagem)
</pre>


Salve seu arquivo e execute em <i>run module</i>. Sua saída deve ser parecida com esta:

<p align="center">
<img src="resources/img/fig_exemplo1.png">
</p>

<p align="justify">
Tome cuidado ao escrever o identificador da variável,
pois o Python diferencia letras maiúsculas e minúsculas, assim a variável <b>Carro</b> é diferente de <b>carro</b>. Da mesma forma, caso o identificador esteja escrito incorretamente, nosso interpretador
retornará um erro. Tente reescrever o programa anterior omitindo uma letra da variável mensagem na instrução print( ), desta forma:
</p>


<pre>
    mensagem = "Ola Mundo"
    print(mesagem)
</pre>


<p align="justify">
Perceba que criamos uma variável chamada mensagem,
mas passamos para a instrução print() um identificador chamado <b>mesagem</b>. O interpretador Python irá retornar um erro parecido com este:
</p>

<p align="center">
<img src="resources/img/fig_exemplo2.png">
</p>

<p align="justify">
Não se preocupe com os erros, eles irão aparecer muitas vezes nas suas simulações de algoritmo. O Python é muito eficiente ao informar para o programador onde está o erro e que tipo de erro foi encontrado. Veja, na primeira linha temos
um <i>Traceback</i>, que segundo Matthes(2016, p. 52) “um traceback é um registro do ponto em que o interpretador se deparou com problemas quando tentou executar seu código”. 
</p>

<p align="justify">
Na próxima linha, o interpretador indica qual foi o arquivo e a linha do arquivo em que o programa parou. Neste caso vemos que o arquivo <b>exemplo1.py</b> possui um erro na linha 2. 
</p>

<p align="justify">
A terceira linha tenta nos mostrar aproximadamente a instrução onde o Python encontrou o erro, que foi na instrução <i>print(mesage)</i>.
</p>

<p align="justify">
Por fim, na quarta linha da mensagem de erro temos o tipo de erro encontrado, que neste caso é um <i>NameError</i> que é um erro comum gerado quando tentamos operar um identificador não existente. Como não declaramos nenhuma variável chamada <b>mesagem</b> o interpretador retornou um erro avisando <strike>(em trocadilhos)</strike> <i>“Olha Sr. Programador, o sr. me pediu para escrever o conteúdo identificado por 'mesagem' mas eu não encontrei nada na memória com esse identificador, tem certeza que é isso mesmo?”</i>. Se o Python pudesse falar ele
diria algo como isto, mas as informações que ele mostra já são suficientes pra nos informar onde foi que erramos<sup><small>2</small></sup>.
</p>

<hr>
<sup><small>2</small></sup> : 
<small>No Python você verá que os erros são chamados de exceptions, a maioria deles estão listados na
<a href="https://docs.python.org/2/library/exceptions.html">documentação oficial do Python</a></small>
<hr>

<p align="justify">
Ao declarar uma variável em Python, também devemos respeitar as palavras reservadas da linguagem, ou seja os identificadores já existentes. Segundo a documentação do Python temos dispostos alguns exemplos de palavras reservadas (<i>keywords</i>):
</p>

<p align="center">
Figura 8 – Palavras reservadas em Python:
</p>

<p align="center">
<img src="resources/img/fig8.png">
</p>

<p align="center">
Fonte: https://docs.python.org/3.5/reference/lexical_analysis.html#identifiers
</p>

<br />

Vamos exercitar mais um pouco e criar uma variável
para cada tipo de dado que acabamos de conhecer:

<pre>
    texto = "mensagem com texto"
    numero_inteiro = 9
    fracionario = 1.29
    dado_logico = True

    print(texto, numero_inteiro, fracionario, dado_logico)
</pre>

<p align="justify">
Os dados do tipo literal em Python podem ser
declarados entre 'aspas simples' ou “aspas duplas”, desde que se abra e feche as mesmas aspas, não sendo possível abrir um aspa simples e fechar com uma dupla ('exemplo”) e nem ao contrário (“exemplo'), mas pode-se abrir uma aspa simples dentro de uma aspa dupla e vice-versa (“Assim 'por exemplo'”, ou ainda, 'Assim “por exemplo”'). “Python chama qualquer número com um ponto decimal de número de ponto flutuante (float). Esse termo é usado na maioria das linguagens de programação e refere-se ao fato de um ponto decimal poder aparecer em qualquer posição de um número” (MATTHES, 2016, p. 63), ressalta-se aqui a importância de declarar os números reais (<i>float</i>) utilizando-se o ponto ( . ) para representar a parte fracionária e não a virgula ( , ) do contrário o Python irá
retornar um erro.
</p>

<p align="justify">
Os dados lógicos ou booleanos devem ser declarados
com a primeira letra maiúscula (<b>True</b> ou <b>False</b>), se você inserir o valor true, ou inserir o valor false, o Python não irá reconhecer e irá enviar um traceback indicando um <i>NameError</i> como vimos anteriormente, sua desculpa é que nenhum identificador com o nome 'true' ou 'false' foi definido, isto porque assim como muitas outras linguagens, o Python é Case Sensitive, o que significa que ele diferencia letras
maiúsculas e minúsculas, logo, True e true são duas coisas completamente distintas para nosso interpretador, sempre que escrevermos um algoritmo devemos ser muito claros e específicos.
</p>

<p align="justify">
Podemos passar as variáveis separadas por vírgula para
a instrução print( ) como no exemplo anterior, ou podemos fazer uma instrução para cada variável:
</p>

<pre>
    print(texto)
    print(numero_inteiro)
    print(fracionario)
    print(dado_logico)
</pre>

<p align="justify">
Há outras formas de imprimir na tela pulando linhas, e formas mais eficientes de se trabalhar com os dados de forma que o desempenho do algoritmo seja superior, porém em nível de aprendizado estas instruções demonstram muito bem o comportamento do interpretador Python.
</p>

<p align="justify">
Vimos no inicio deste capítulo que uma variável
somente pode guardar um valor por vez, isso quer dizer que se eu declarar uma variável chamada surpresa e atribuir diferentes valores para ela, cada vez que um novo valor for atribuído, o
anterior será esquecido, veja:
</p>

<pre>
    surpresa = 9
    surpresa = 16.78
    surpresa = 'doce de goiaba'
    surpresa = "CWB City Rocks"

    print(surpresa)
</pre>

<p align="justify">
Atribuímos inicialmente o o valor inteiro 9 para a
variável surpresa, então logo em seguida atribuímos o valor real 16.78, então a próxima instrução diz ao Python para atribuir uma string à mesma variável, e em seguida pede para atribuir outra string. No final dizemos ao Python para escrever
o valor da variável surpresa.
</p>

<p align="center">
<img src="resources/img/fig_exemplo3.png">
</p>

<p align="justify">
O valor exibido na tela foi o último valor a ser atribuído à variável, todos os outros valores foram desconsiderados, isso porque uma variável somente pode guardar um valor de cada
vez. Esta sequência de instruções também demonstra como o Python consegue atribuir diferentes tipos de dados em uma mesma variável, o que não aconteceria em muitas outras linguagens de programação.
</p>

<p align="justify">
Lembra-se do algoritmo soma.py que construímos no
início do capítulo? Neste algoritmo o a instrução input( ) irá esperar o usuário entrar com um tipo de dado, porém independente do tipo de dado fornecido, o Python irá armazenar a entrada como uma string (dado do tipo literal), então para realizar a soma tivemos que fazer uma conversão utilizando uma instrução int( ). Quando passamos um tipo de dado para a instrução int( ) o Python tentará realizar uma conversão do tipo de dado fornecido para um tipo inteiro. Vamos ver um exemplo:
</p>

<pre>
    numero = '12'
    print(numero)
    numero = int(numero)
    print(numero)
</pre>

<p align="justify">
Primeiro declaramos uma variável chamada numero e
pedimos para mostrá-la na tela, então realizamos a conversão para inteiro e pedimos para mostrar na tela. Na saída não conseguimos identificar a diferença, observe o resultado:
</p>

<p align="center">
<img src="resources/img/fig_exemplo4.png">
</p>

<p align="justify">
Mas se tentarmos realizar uma operação matemática,
como a soma, em variáveis do tipo literal o que acontece é um evento chamado concatenação, e não a adição em si, veja o exemplo:
</p>

<pre>
    numero = '12'
    numero2 = '3'
    print(numero + numero2)

    numero = int(numero)
    numero2 = int(numero2)
    print(numero + numero2)
</pre>

<p align="justify">
Primeiro declaramos duas strings e tentamos exibir a
soma de ambas, depois convertemos as strings para inteiro e exibimos a soma das variáveis:
</p>

<p align="center">
<img src="resources/img/fig_exemplo5.png">
</p>

<p align="justify">
Observe os resultados, na primeira linha obtivemos o
resultado da concatenação, que nada mais é do que juntar a segunda string ao final da primeira, resultando não na soma, mas na junção das duas variáveis literais em um único texto. Ja no segundo resultado pudemos obter o resultado da operação de adição, pois a instrução int() converteu os dados literais para numéricos e o Python compreendeu que deveria realizar uma operação aritmética com estes dados.
</p>

<p align="justify">
Mas o que aconteceria se você tentasse converter uma
letra para número?
</p>

<pre>
    fruta = "banana"
    banana = int(fruta)
    print(fruta)
</pre>

<p align="justify">
Ao criarmos uma variável literal com caracteres não
numéricos e forçarmos uma conversão, o Python logo retornará um erro, pois não é possível converter letras para números, o mesmo aconteceria se tentássemos converter um dado do tipo
real ou lógico.
</p>

<p align="center">
<img src="resources/img/fig_exemplo6.png">
</p>

<p align="justify">
O erro retornado é um ValueError, dizendo que
os valores expressados na tentativa de execução não são válidos, por isto devemos tomar muito cuidado ao trabalhar com os tipos de dados para não levantar erros inesperados.
</p>

<p align="justify">
Caso você tenha dúvida quanto ao tipo de dado que
você está lidando, o Python tem a instrução type( ). Quando você passar uma variável para a instrução type(variavel) ele ira informar o tipo de dado dessa variável, como no exemplo a seguir:
</p>

<pre>
    fruta = "banana"
    numero = 78
    God = False
    PI = 3.1415

    print(type(fruta))
    print(type(numero))
    print(type(God))
    print(type(PI))
</pre>

Saida:

<p align="center">
<img src="resources/img/fig_exemplo7.png">
</p>

<p align="justify">
Vemos que que cada tipo de dado pertence a uma classe
que representa um tipo de dado específico: Literal (str), Inteiro (int), Lógico (bool) e Real (float).<sup><small>3</small></sup>
</p>

<hr>
<sup><small>3</small></sup> : 
<small>O Python também tem o tipos de dados complex, mas não será abordado
nesta obra, você pode conferir o modelo de dados do Python <a href="https://docs.python.org/3/reference/datamodel.html#">aqui.</a></small>
<hr>

<br />


## Constantes


<p align="justify">
Da mesma forma que possuímos valores variáveis,
também temos valores constantes, ou seja, que não se
modificam ao longo do seu algoritmo. No Python, por questões de boas práticas, sempre definimos uma constante com todas as letras do identificador em CAIXA ALTA, ou seja, letras maiúsculas, dessa forma:
</p>

<pre>
    PI = 3.1215
    ALTURA = 600
    LARGURA = 600
</pre>

<p align="justify">
Porém escrever uma variável em caixa alta não a torna realmente uma "constante", o que quer dizer que ainda se pode modificar o valor desta variável atribuindo outro valor à mesma. Escrever com letras maiúsculas é apenas uma boa prática para facilitar a legibilidade do código e distinção das variáveis pelo programador. Em Python é muito comum declarar valores constantes em formas de tuplas, que nada mais são que listas imutáveis, o que torna a alteração do valor contido na variável impossível de ser realizado.
</p>

Declarando uma tupla:

<pre>
    QUANTIDADE = (100)
</pre>

Para acessar o valor da tupla:

<pre>
    qt = QUANTIDADE[0]
    print(qt)
</pre>

Não se preocupe quanto a isto neste momento, veremos mais sobre tuplas em seções futuras deste livro.


## Expressões


<p align="justify">
Quando estivermos elaborando nossos algoritmos,
muitas vezes teremos que utilizar expressões aritméticas para
processar os dados, as expressões são formadas por operadores
aritméticos e possuem, assim como na matemática, uma
prioridade de execução, denominada precedência. Segue um
quadro com os operadores em Python:
</p>

<p align="center">
Tabela 4 – Operadores aritméticos mais comuns em Python e sua
precedência
</p>


| OPERADOR | OPERAÇÃO | PRECEDÊNCIA | DESCRIÇÃO |
| :------: | :------: | :---------: | --------- |
| + | Adição | 0 | Realiza a soma dos operandos. Ex: a + b |
| - | Subtração | 0 | Realiza a subtração dos operandos. Ex: total - desconto |
| / | Divisão | 1 | Realiza a divisão dos operandos. Ex: 12 / 2 |
| // | Divisão inteira | 1 | Retorna a parte inteira da divisão. Ex: 3 // 2 (resulta em 1) |
| * | Multiplicação | 1 | Multiplica os operandos. Ex: 2 * 5 |
| ** | Exponenciação | 2 | Eleva o operando a esquerda pelo operando a direita. Ex: 5**2 (cinco ao quadrado) |
| % | Módulo | 2 | Obtém o resto da divisão dos operandos. Ex: 7%2 (Resulta em 1) |


<p align="justify">
As operações com menor precedência são executadas
por último, neste caso ao observar a expressão 2 + 3 * 5, assim como na matemática, a primeira operação a ser realizada é a multiplicação (3 * 5), somente então a adição será realizada (2 + 15). Estas precedências podem ser alteradas fazendo uso do
parêntese ( ), dando precedência para a expressão que estiver dentro do parêntese, desta forma:
</p>

<pre>
    a = 2 + 3 * 5
    b = (2 + 3) * 5

    print("O valor de a: ", a)
    print("O valor de b: ", b)
</pre>

Saída:

<p align="center">
<img src="resources/img/fig_exemplo8.png">
</p>

Nós também temos os operadores relacionais, que
permitem realizar comparações entre valores:

<p align="center">
Tabela 5 – Operadores relacionais em Python
</p>


| OPERADOR | COMPARAÇÃO | DESCRIÇÃO |
| :------: | :--------: | --------- |
| == | Igualdade | Dois sinais de = compara se dois valores são idênticos. Ex: a == b | 
| != | Diferença | Compara se dois valores são diferentes. Ex: a != b |
| > | Maior | Compara se o primeiro valor é maior que segundo. Ex: a > b |
| < | Menor | Compara se o primeiro valor é menor que o segundo. Ex: a < b |
| >= | Maior igual | Compara se o primeiro valor é maior ou igual ao segundo valor. Ex: a >= b |
| <= | Menor igual | Compara se o primeiro valor é menor ou igual ao segundo. Ex: a <= b |


<p align="center">Fonte: O autor.</p>

As expressões relacionais sempre retornarão um valor
lógico (**True** ou **False**), veja no exemplo a seguir:

<pre>
    a = 2
    b = 3

    print(a == b)
    print(a != b)
    print(a > b)
    print(a < b)
    print(a >= a)
    print(a <= b)
</pre>

Saída:

<p align="center">
<img src="resources/img/fig_exemplo9.png">
</p>

<p align="justify">
Existem mais operadores que não cobriremos aqui, mas
você pode conferir a lista completa na documentação do Python.<small><sup>4</sup></small>
</p>

<hr>
<small><sup>4</sup></small> : <small>
Disponível <a href="https://docs.python.org/3.5/reference/lexical_analysis.html#operators"> aqui </a>.
</small>
<hr>

<p align="justify">
Uma aplicação interessante em Python é a multiplicação de strings, veja:
</p>

<pre>
    chaves = "pi"
    print(chaves * 10)
</pre>

Saída:

<p align="center">
<img src="resources/img/fig_exemplo10.png">
</p>

<p align="justify">
Temos também os operadores lógicos que podem ser
utilizados juntamente com os relacionais fazendo comparações, a seguir os operadores lógicos:
</p>

<p align="center">
Tabela 6 – Operadores lógicos em Python
</p>


| OPERADOR | OPERAÇÃO | PRECEDÊNCIA | DESCRIÇÃO |
| :------: | :------: | :---------: | --------- |
| or | Disjunção | 1 | A disjunção entre duas operações resultara verdadeiro se um dos valores for verdadeiro |
| and | Conjunção | 2 | A conjunção resultará em verdadeiro se, e somente se, todos os valores examinados forem verdadeiros |
| not | Negação | 3 | A negação inverte o valor lógico da variável examinada. Se o valor for verdadeiro ele se tornará falso, e vice-versa. |


<p align="center">Fonte: O autor </p>

Vamos examinar estas operações com o Python:

<pre>
    a = 2
    b = 3
    c = 4

    print(a > b or a > c)
    print(a < b and a < c)
    print(not a == b)
</pre>

Saída:

<p align="center">
<img src="resources/img/fig_exemplo11.png">
</p>

<p align="justify">
Veja que definimos as variáveis a = 2, b = 3 e c =4.
Então fizemos um pergunta ao Python como que “Python, a é maior que b OU a é maior que c?” então na primeira linha da saída temos a resposta False, pois a não é nem maior que b e nem maior que c, a na disjunção somente obtemos uma saída verdadeira se pelo menos uma expressão resultar em verdadeiro, como nossas duas expressões resultaram falso, a disjunção resultou falso.
</p>

<p align="justify">
Então perguntamos ao Python: “a é menor que b E a é
menor que c?”, o Python responde: True, pois na conjunção obtemos resultado verdadeiro se todas as expressões resultarem verdadeiro, como 2 é menor que 3 e também é menor que 4, nossa avaliação lógica retornou verdadeiro.
</p>

<p align="justify">
Por fim perguntamos ao Python se a e b são idênticos e informar o valor lógico inverso (como assim? você pergunta), temos que 2 não é igual a 5, então o resultado da avaliação seria Falso, mas como dissemos ao Python para nos informar o inverso ele respondeu Verdadeiro (True). Um detalhe interessante é que sempre que uma variável estiver inicializada com o valor 0 ela retornará Falso.
</p>


## Funções Intrínsecas


<p align="justify">
Funções intrínsecas são funções (instruções) prédefinidas
em uma linguagem de programação. Estas funções
auxiliam o programador para não ter que reinventar a roda em
seus algoritmos. Por exemplo, a instrução print( ) é uma
função pré-definida (built-in function de acordo com BARRY,
2015) da linguagem que permite exibir uma mensagem na tela.
No site oficial do Python encontramos uma tabela com as
funções intrínsecas existentes no Python 3:
</p>

<p align="center">
Tabela 7 – Funções intrínsecas no Python 3
</p>

<p align="center">
<img src="resources/img/tabela7.png">
</p>

<p align="center">
Fonte: https://docs.python.org/3/library/functions.html
</p>

<p align="justify">
Você não precisa decorar todas estas funções, mas a
medida que for construindo seus algoritmos vai utilizar
algumas delas, existem outras funções que não estão presentes
nesta lista mas você poderá conhece-las na documentação do
Python, outras apresentaremos no decorrer deste livro. A
descrição destas pode ser encontrada na documentação do
Python. Algumas destas você já utilizou aqui em alguns
exemplos, como por exemplo print( ), int( ), input( ) e type( ).
Lembra-se do int( ) para converter números em dados literais
para números inteiros? Também temos as funções str( ) e
float( ) para converter dados em literais e números reais
respectivamente.
</p>

<pre>
    a = 2
    print(str(a))
    print(float(a))
</pre>

Saída:
<pre>
    2
    2.0
</pre>


## Entrada de dados


<p align="justify">
Como vimos, o Python possui uma função interna
chamada input( ) que recebe uma entrada do usuário. Nesta
instrução podemos fornecer uma string para ajudar o usuário a
saber que tipo de dado ele deve fornecer, como no exemplo a
seguir:
</p>

<pre>
    nome = input("Insira seu nome ")
    print("Ola ", nome, " como esta hoje?")
</pre>

Saída:

<p align="center">
<img src="resources/img/fig_exemplo12.png">
</p>

<p align="justify">
Como vimos, a instrução input( ) recebe uma string por
padrão, e caso precisemos que a entrada seja de outro tipo de
dado temos que fazer a conversão com int( ) ou float( ), desta
forma:
</p>

<pre>
    nome = input("Insira seu nome ")
    idade = int(input("Insira sua idade "))
    altura = float(input("Insira sua altura "))
    print("Seu nome e ", nome)
    print("Voce tem ", idade, " anos de idade")
    print("Voce mede ", altura, " de altura")
</pre>

<p align="justify">
Perceba que ao obter a idade, primeira declaramos a
variável então atribuímos a ela a instrução int( ) pois ela deve
ser um número inteiro, e dentro da instrução int( ) inserimos o
input( ). Lembra quando dissemos que tudo que estiver dentro
do parêntese acontece antes? É exatamente isto, primeiro
ocorre a chamada da função input( ) que irá fazer uma
solicitação de entrada ao usuário. Quando ele realizar esta
entrada o valor fornecido será processado pela função int( ),
convertendo o valor para um dado do tipo inteiro, que então será armazenado na variável idade. O mesmo acontece com a
altura, primeiro um valor é solicitado, então convertido para o
tipo de dados float e então atribuído à variável altura. Quando
acessarmos estas variáveis elas já estarão com o tipo de dado
que convertemos. A saída para o algoritmo acima seria parecida
com esta:
</p>

<p align="center">
<img src="resources/img/fig_exemplo13.png">
</p>


## Exercícios elaborados


Primeiramente será mostrado alguns problemas e suas
soluções em Python, vamos explicar a elaboração dos
exercícios e alguns exercícios para que você leitor resolva
sozinho utilizando os conhecimentos aprendidos até aqui.

1. Formular um algoritmo que leia e apresente os dados de
uma pessoa: nome, idade, endereço, telefone de contato
e mostre as informações obtidas na tela.
Problema a ser resolvido: Obter informações de uma
pessoa e exibir as informações na tela;

**Dados de entrada**: nome, idade, endereco, telefone;

**Processamento**: Não há processamento, apenas entrada e saída de informações;

**Saída**: Exibir os dados da pessoa;

<p align="center">
Figura 9 – Fluxograma Atividade 1
</p>

<p align="center">
<img src="resources/img/fig9.png">
</p>

<p align="center">Fonte: O autor.</p>

<pre>
    nome = input("Insira seu nome ")
    idade = int(input("Insira sua idade "))
    endereco = input("Insira seu endereco ")
    telefone = input("Insira seu telefone ")

    print("Nome: ", nome)
    print("Idade: ", idade)
    print("Endereço ", endereco)
    print("Telefone para contato: ", telefone)
</pre>

<p align="justify">
Primeiramente declaramos a variável nome e atribuímos
a ela uma string informada pelo usuário, em seguida a variável idade irá receber um valor de entrada do usuário que será
convertido em um inteiro. Então atribuímos um valor de
entrada para a variável endereco e mais uma para a variável
telefone. Como não temos processamento as próximas
instruções são comandos de saída, exibindo as informações
obtidas correspondentes aos dados da pessoa.
</p>

<p align="center">
<img src="resources/img/exercicio1.png">
</p>

<p align="justify">
<b>Observações</b>: É muito comum obtermos o valor de um
telefone como string, pois o usuário pode entrar com caracteres
especiais como parêntese ( ) e o traço -. Também recomenda-se
que nas variáveis que possuem acento ou cedilha este caractere
seja substituído ou omitido como no caso de endereço
(declaramos como endereco). Salienta-se ainda o cuidado ao
declarar instruções dentro de instruções como no caso de
int(input( )) onde abrimos dois parênteses então precisamos
fechar dois parênteses, do contrário você receberá um erro.
</p>

<br />

2) Sua professora de matemática pediu que você
calculasse a área e o perímetro de um quadrado e lhe
passou as fórmulas para o cálculo da área sendo A = L x
L (o tamanho do lado do quadrado vezes ele mesmo) e
o perímetro deve ser obtido através da soma dos quatro
lados do quadrado. Vamos escrever um algoritmo que
faça seu dever de casa:

**Problema a ser resolvido**: Calcular a área e o
perímetro de um quadrado;

**Dados de entrada**: area, perimetro, lado

**Processamento**: calcular a área (A = lado x lado ou lado**2) e calcular o perímetro (b x 4 ou b + b + b + b);

**Saída**: Exibir o resultado do cálculo;

<p align="center">
Figura10 – Fluxograma Atividade 2
</p>

<p align="center">
<img src="resources/img/fig10.png">

<p align="center">Fonte: O autor.</p>

<pre>
    lado = float(input("Insira o tamanho dos lados do quadrado: "))
    area = lado * lado
    perimetro = lado * 4
    print("A area do quadrado e de: ", area)
    print("O perimetro do quadrado e de: ", perimetro)
</pre>

<p align="justify">
Primeiro precisamos do valor correspondente ao
tamanho dos lados do quadrado então declaramos a variável
lado e atribuímos a ela o valor que for inserido pelo usuário
convertido em um número real, em seguida fazemos o
processamento, multiplicando o lado por ele mesmo e
atribuindo o resultado à variável area, a variável perímetro
recebe o valor de lado multiplicado por 4. Em seguida temos as
saídas exibindo os resultados.
</p>

<p align="center">
<img src="resources/img/exercicio2.png">
</p>

<p align="justify">
Observação: Como o valor de area deveria ser lado ao
quadrado poderia-se ter utilizado lado**2 que funcionaria da
mesma forma, o operador ** eleva o valor da esquerda à potência do valor da direita, tente fazer isto no seu IDLE.
</p>

<br />

3) Sua professora gostou tanto do seu algoritmo
computacional que lhe pediu para elaborar outro
algoritmo, dessa vez um que realize o cálculo da área
de um triângulo, sabendo que a área do triângulo é igual
o quociente da base vezes a altura por 2, vamos elaborar este algoritmo:

**Problema a ser resolvido**: Calcular a área de um
triângulo;

**Dados de entrada**: base, altura;

**Processamento**: calcular a área A = (base x altura) / 2;

**Saída**: Exibir o resultado do cálculo;

<p align="center">
Figura 11 – Fluxograma atividade 3
</b>

<p align="center">
<img src="resources/img/fig11.png">
</p>

<p align="center">Fonte: O autor.</p>

<pre>
    base = float(input("Insira o valor da base do triangulo: "))
    altura = float(input("Insira o valor da altura do triangulo: "))
    print("A area do triangulo e: ", (base * altura) / 2)
</pre>

<p align="justify">
Primeiro vamos receber a entrada necessária.
Declaramos uma variável base e atribuímos a ela o valor
inserido pelo usuário convertido em número real, depois
fazemos o mesmo com a variável altura. Desta vez inserimos o
processamento diretamente no comando de saída através de
uma expressão, assim economizamos uma variável fazendo
com que o algoritmo tenha um melhor desempenho. Em um
pequeno programa como este pode não fazer nenhuma
diferença, mas a medida que for construindo algoritmos mais
complexos o número de linhas e comandos pode impactar no desempenho do seu programa.
</p>

<p align="center">
<img src="resources/img/exercicio3.png">
</p>

<p align="justify">
Observação: Se você andou brincando com o Python pode já
ter percebido que em alguns cálculos com números reais o
Python pode retornar um valor com várias casas decimais, isso
é normal não se assuste, veremos como lidar com isso no
decorrer do livro. Caso você ainda não tenha visto isso tente
calcular 2.90 x 1.43.
</p>


*Exercícios propostos*


1) Elabore um algoritmo em Python que leia, calcule e
escreva a média aritmética entre quatro números;

2) Elabore um algoritmo em Python que receba um número inteiro e escreva na tela o número fornecido, o antecessor desse número e o sucessor desse número;

3) Elabore um algoritmo em Python que:

+ Primeiro exiba uma mensagem de boas vindas;

+ Pergunte o nome do usuário;

+ Exiba uma mensagem dizendo uma mensagem de olá,
seguida pelo nome do usuário, seguida por outra mensagem fazendo um elogio.

4) Elabore um algoritmo em Python que calcule a área e o perímetro de um círculo, sabendo que A = π.r² e P=2π.r.

<hr>

* [< Voltar ao Capítulo 1](ch1.md)
* [> Continuar para o Capítulo 3](ch3.md)