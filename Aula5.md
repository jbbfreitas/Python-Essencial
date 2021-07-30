# Aula 5

## Laços ou Loop

Na lição 4 nós aprendemos as estrutura que podem alterar o fluxo normal de execução de um programa que é `top-down`. Na lição 3, nós aprendemos sobre os blocos de código e dissemos que, nas próximas lições, iríamos falar um pouco mais sobre os vários tipos de blocos de código.

Nesta lição iremos falar sobre um tipo de bloco denominado laço ou loop.
Você já viu uma apresentação de acrobacia áerea? Pois é, nesse tipo de apresentação, geralmente os aviões fazem um "loop". Em acrobacia aérea, um loop nada mais é do que voar descrevendo um círculo vertical, ou seja, parte-se de um ponto A (o ponto mais alto), passa-se por um ponto B (o ponto mais baixo) e retorna-se ao ponto inicial (ponto A). Veja a Figura 1.

<p align="center">
  <img src="imagens/Loop.png" alt="Imagem de um looping aéreo">
</p>
<p align="center">
   <strong>Figura 1-Um loop aéreo</strong> 
</p>


Como em qualquer linguagem de programação o Python possui diversas estruturas de repetição que podem ser utilizadas sempre que um conjunto (bloco) de instruções precisar ser executado uma ou mais vezes. Essas estruturas de repetição são denominadas `laços` ou `loop`. 

Cada vez que as instruções do bloco são executadas diz-se que foi realizado um ciclo ou iteração. Cada iteração  de um `loop` é executada até que uma determinada condição seja atingida. 

É possível inserir um laço dentro de outro laço. Isso é o que se denomina de ninho de laços ou laços aninhados.

Vou mostrar duas estruturas de repetição do Python: `while` e `for`

### 1. while

A estrutrua `while` (enquanto em inglês) é utilizada para repetir um bloco de instruções **enquanto** um condição for válida.

Dessa forma a sintaxe do `while` é a seguinte:

```python
while <condição>:
    instrução 1
    break
    continue
    instrução 2
    ...
    instrução n
else:
    instrução n+1
```
A clausula `break` interrompe o laço e a `continue` ignora as instruções que estão abaixo e volta ao `while` passando para a próxima iteração. O código dentro do `else` é executado ao final do laço, a menos que o laço tenha sido interrompido por um `break`.

Vou mostrar 3 exemplos:


```python 
#Exemplo 9 - A taboada do 10
x=1
while x<=10:
    print '10 x', x, '=', 10*x 
    x=x+1
```

```python
#Exemplo 10-Bichinhos do pet center
pets = ['cão','gato', 'periquito', 'hamster']
i=0
while i < len(pets): 
    print(pets[i]) 
    i += 1 
```

```python
#Exemplo 11-Iteração com palavras
while True:
    valor_informado = raw_input("Digite alguma palavra: ")
    if valor_informado.lower() == "fim":
        print("Você optou por Sair!")
        break
    if len(valor_informado) <= 2:
        print("Número mínimo de letras é 3")
        continue
    print("Para sair digite \"fim\"") 
```
### 2. for

O `for` é usado quando se quer iterar sobre um bloco de código um determinado número de vezes.
Isso significa que diferentemente do `while` o número de iterações é conhecida `a priori`.

Vou mostrar mais 3 exemplos:

```python
#Exemplo 12 - Mostrando números de 1 a 9
for i in range(1,10):
    print i
```

```python
# -*- coding: latin-1 -*-
#Exemplo 13 - Iterando em uma frase
frase = u"O Python é cool"
for letra in frase:
    print letra
```

```python
# -*- coding: utf-8 -*-
#Exemplo 14 - Iterando em um dicionário
gatinhos = {'Português': "Boa Noite", "Inglês": "Good Night", "Francês": "Bonne Nuit", "Alemão": "Gute Nacht"}
for chave, valor in gatinhos.items():
    print '{}->{}'.format(chave,valor)

```
Não se preocupe se você não entendeu o que vem a ser um dicionário ou a letra 'u' antes da frase (exemplo 13), ou até mesmo a função range(). Isso foi proposital, para aguçar a sua curiosidade. 

::: :pushpin: Resumo :::
Nesta aula você aprendeu sobre o uso dos laços `while`e `for`.

#### Desafio 1 :innocent:
Pesquise na internet sobre a letra `u` como usada na frase  `frase = u"O Python é cool"`

#### Desafio 2 :innocent:
Pesquise na internet sobre a função range() como usada em `for i in range(1,10):`

#### Desafio 3 :innocent:
Pesquise na internet sobre a performance(velocidade de execução) do `while` e do `for`

#### Desafio 4 :innocent:
Execute os exemplos de 9 a 14, mostrados nesta aula,  no Jupyter.

#### Desafio 5 :innocent:
Altere o exemplo 14 para incluir também o cumprimento em espanhol.

Por hoje é só. 

Na [Aula 6](Aula6.md) você vai aprender sobre os tipos de dados no Python. Até!
