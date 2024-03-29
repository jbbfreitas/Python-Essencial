# Aula 8

## Um pouco mais sobre coleções

Nesta aula vamos aprender um pouco mais sobre coleções: como são criadas, fatiadas, alteradas, adicionar ou remover elementos.

O Python tem diversos tipos de coleções e um dos mais simples e versateis é a Lista. Você irá usar listas o tempo todo em Python.

### 1- Como as listas são criadas?

Em Python é muito fácil criar uma lista, bastando para isso colocar todos os seus elementos dentro de colchetes `[]` separados por vírgula.

Os itens de uma lista podem ser de quaisquer tipo (`integer`, `float`, `string`). Pode, inclusive, ser uma outra lista, ou seja, uma lista dentro de uma lista.

As listas são mutáveis, isto quer dizer que você pode alterar, a qualquer tempo, um ou mais elementos de uma lista.

Vamos ver alguns exemplos de como criar e modificar uma lista.

```python
# Aula 8 - Listas
# Exemplo 28- Listas

linguagens = ['Java', 'Python', 'C', 'R', 'Java Script']# Uma nova lista: Linguagens de programação
for prog in linguagens: print prog # Varrendo a lista inteira
linguagens[-1] = 'TypeScript' # Trocando o último elemento
linguagens.append('C#') # Incluindo uma nova linguagem
linguagens.remove('C') # Removendo uma linguagem da lista
linguagens.sort() # Ordenando a lista
linguagens.reverse() # Invertendo a lista
for i, prog in enumerate(linguagens): print i + 1, '=>', prog # Imprimindo com numeração
print linguagens[1:] # Imprime do segundo item em diante
```
Veja como fica saída:
```
Java
Python
C
R
Java Script
1 => TypeScript
2 => R
3 => Python
4 => Java
5 => C#
['R', 'Python', 'Java', 'C#']
```

::: :pushpin: Importante :::

> A função enumerate() retorna uma tupla de dois elementos a cada iteração: um número
seqüencial e um item da seqüência correspondente. (`i` e `prog`) no nosso caso. Tupla nada mais é do que uma lista, entretanto, diferentemente das listas, as tuplas são imutáveis. 

> Então a instrução `for i, prog in enumerate(linguagens)` tem uma dupla função: contar elementos e obter os elementos.

> As funções de ordenação (sort) e de inversão (reverse) são realizadas na própria lista, sendo assim, não geram novas listas. Observe que a lista `liguagens` foi alterada com o uso dessas duas funções.

### 2- Como funcionam os índices?

A linguagem Python é denominada `zero indexed`, ou seja, seus índices são baseadas em zero. Isso significa que o primeiro elemento de uma lista é o zero, e o último é o número de elementos menos 1. Lembra-se da aula 7 quando falamos das strings?

Se uma lista contiver uma outra lista, o acesso a um de seus elementos é duplamente indexado.
Assim : elemento[i,j]: onde `i` é a posição da sublista na lista principal e `j` é a posição do elemento dentro da sublista.

Veja e pratique os exemplos abaixo.

```python
# Exemplo 29 -Indice das listas

minha_lista = ['c', 'o', 'n', 's', 't','r','u','i','r']

# Imprime: c
print(minha_lista[0])

# Imprime: n
print(minha_lista[2])

# Imprime: t
print(minha_lista[4])

# Lista dentro de lista
outra_lista = ["Alegria", [2, 0, 2, 1]]

# Índice de uma Lista dentro de outra.
# Imprime a letra 'l'
print(outra_lista[0][3])

# Imprime o número 5
print(outra_lista[1][2])


#print(minha_lista[4.0]) Essa instrução dariaErro! Não pode usar float como índice, apenas inteiros


```

### 3- O que são índices negativos ?

Python permite índices negativos para as suas coleções. O índice -1 refere-se ao último item, -2 ao penúltimo e assim por diante.

```python
# Exemplo 30 -Indices Negativos

# Indices negativos em uma lista
minha_lista = ['c', 'o', 'n', 's', 't','r','u','i','r']
print(minha_lista[-1])
print(minha_lista[-5])
```

### 4- Como fatiar as listas?
Para fatiar, ou seja, extrair pedaços de uma lista, usa-se o `:`.

```python
# Exemplo 31 -Fatiando as listas


minha_lista = ['c', 'o', 'n', 's', 't','r','u','i','r']

# exibir a partir do índice 2 até o 5º elemento 
print(minha_lista[2:5])

# exibir a lista subtraindo os 5 últimos elementos
print(minha_lista[:-5])

# exibir do a partir do índice 5 até o final
print(minha_lista[5:])

# todos os elementos do início ao fim
print(minha_lista[:])
```
Veja como fica a saída

```
['n', 's', 't']
['c', 'o', 'n', 's']
['r', 'u', 'i', 'r']
['c', 'o', 'n', 's', 't', 'r', 'u', 'i', 'r']

```


### 5-Como adicionar ou alterar elementos a uma lista?

Listas são mutáveis, significando que seus elementos podem ser alrterados, diferentemente das strings e das tuplas.

Para alterar uma lista usa-se o operador `=`. É possível alterar um elemento ou uma faixa (subconjunto) de elementos.

```python
# Exemplo 32 -Alterando listas, para corrigie um erro (de pares para impares)
impares = [2, 4, 6, 8]

# alterar o índice 0  
impares[0] = 1            

print(impares)

# alterando a partir do índice 1 até o 4º elemento
impares[1:4] = [3, 5, 7]  

print(impares)                                 
```
Veja como fica a saída
```
[1, 4, 6, 8]
[1, 3, 5, 7]
```


::: :pushpin: Não confunda! :::

> O que vem antes do `:` é o índice (começando em 0). O que vem após o `:` é o número de elementos . Se o número de elementos for negativo, conta-se de marcha ré (do final para o começo).

É possível adicionar um item a uma lista usando o método `append()` ou um conjunto de vários itens usando o método `extend()`.

```python
# Exemplo 33 -Adicionando e estendendo listas 

impares = [1, 3, 5]
impares.append(7)
print(impares)
impares.extend([9, 11, 13])
print(impares)

```
### 6-Os operadores `+` e `*`

As listas em Python ainda podem ser alteradas com o uso dos operadores `+` e `*`. Vejamos o que cada um faz:

O operador `+` serve para concatenar duas listas. Então se tenho `listaA = [1,2]` e `listaB=[3,4]` a operação `listaA + listaB` resulta em [1,2,3,4].

Já o operador `*` serve para repetir elementos em uma lista.

Vamos aos exemplos:

```python
# Exemplo 34 -Uso dos operadores + e * em listas 
listaA = [1, 2]
listaB = [3,4]
print(listaA + listaB+ [5, 6, 7])
listaC= ["do", "ré", "mi","fá"]+ ["fá"] * 2
for e in listaC:
    print e

```
#### Desafio 1 :innocent:
Complete o código python abaixo (segunda linha) para que o resultado seja : `linguagem  Python: poderosa e simples`

```python
lista2 = ['@#&','lin','&*','guagem ',' Python',': ','<<','po','**','derosa',' e simples']
lista3= #Complete aqui usando os conhecimentos aprendidos nesta aula
print ''.join([str(elem) for elem in lista3])
```


Por hoje é só. Na [Aula 9](Aula9.md) você vai aprender um pouco mais sobre os dicionários no Python. Até mais!


