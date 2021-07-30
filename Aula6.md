# Aula 6

## Tipos de dados no Python

### 1-Variáveis
Variáveis são nomes que criamos para armazenar, temporariamente, algum valor.
Exemplo: `salario`, `nome_fantasia`, `total_da_compra` etc.

Tecnicamente falando, as variáveis são os endereços da memória do computador aos quais atribui-se um determinado nome.

As variáveis no Python são criadas no momento em que recebem algum valor. Assim como em outras linguagens, como o java por exemplo, existe um coletor de lixo `garbage collector` que atua, destruindo as variáveis, sempre que não existe mais nenhuma referência àquela variável, ou seja, quando a variável deixa de representar um endereço de memória.

Vamos dizer a mesma coisa com um exemplo:

```python
a=20
b=a
c=b
```
O que ocorre aqui é que as 3 variáveis: `a`, `b` e `c` apontam (são referências) para o mesmo endereço de memória onde está armazenado o valor `20`.

Somente quando as 3 variáveis não apontarem mais para esse endereço é que o coletor de lixo vair liberar o endereço (limpar).

Existem algumas regras para o nome de variáveis. Vou mostrá-las:

1. Os nomes das variáveis devem começar com uma letra. Não podem começar por caracteres especiais, tais como `á`, `ç` nem com números.
2. Podem iniciar com um `underline` (_).
3. Após o primeiro caracter, pode ser seguido por números ou  `underline` (_).

Exemplos de variáveis válidas:

```python
#Exemplo 15-Váriáveis válidas
nome123 = 'João'
_salario = 12.45
data_nascimento='12/12/1970'
```

Exemplos de variáveis *inválidas*:

```python
#Exemplo 15-Váriáveis inválidas
época = "1900" #começa com é
exceção = "Valor inválido" #contém caractere especial `ç`
2semestre=range[6,13] #começa com número
```

Além das regras acima, existem as boas práticas:

1. Nomes de variáveis devem começar com letras minúsculas
2. Nomes compostos devem ser separados com o caráctere `_`
3. Evitar o uso do `Camel Case` que é a prática de escrever palavras compostas ou frases de modo que cada palavra ou abreviatura no meio da frase comece com uma letra maiúscula. Exemplo: `estadoCivil`.
4. Para mais detalhes, consulte o [Guia de codificação para Python](https://www.python.org/dev/peps/pep-0008/#function-and-variable-names)

### 2-Tipos primitivos (simples)

Existem vários tipos simples de dados pré-definidos no Python, tais como:
- Números (inteiros, reais, complexos, ... ).
Exemplo:

```python
#Exemplo 16-Váriáveis numéricas
contador =10 # Tipo inteiro
salario = 5482.34 #Tipo real
x= 10+3j #Número complexo. O `j` é a parte imaginária do número complexo
diametro_da_terrra = 12.742e3 #Real em notação científica
print 'O diâmetro da terrra é de {} Km'.format(diametro_da_terrra)
```

- Texto.
```python
#Exemplo 17-Váriáveis textos
nome ='Carlos R Cadete' # Tipo texto
endereco ="Rua Domingos Ferreira" # Tipo texto
var22 = u'Eqüidade' # Tipo texto unicode
```


- Booleanos. São variáveis que armazenam `True`(verdadeiro) ou `False`(falso)
```python
#Exemplo 17-Váriáveis booleanas
v1 = True
v2=bool(False) # atribui False
v3=bool(None)) # atribui False
v4=bool(1)) # atribui True
```
::: :pushpin: Importante :::
Os valores booleanos são grafados em a inicial maiúscula.

### 3-Tipos coleções 

Coleção são tipos complexos que armazenam não apenas um valor, mas um conjunto de valores. As principais coleções no Python são:

- **Lista** é uma coleção que é ordenada e mutável. Permite membros duplicados.

```python
#Exemplo 18-Listas
nomes = ['Mara', 'José', 'Camilo']
dias_da_semana = [1,2,3,4,5,6,7]
temperaturas = [32,27,-4,32,17, 27,-4]
```

- **Tupla** é uma coleção que é ordenada e imutável. Permite membros duplicados.
```python
#Exemplo 19-Tuplas
frutas = ("apple", "banana", "cherry") #OK
frutas = ("grape", "banana") #OK
frutas = frutas + ("avocado", "guava") #OK
frutas[0] = "orange" # Tentativa de alterar `grape` por `orange`. Erro aqui, as tuplas são imutáveis
print frutas
```

- **Conjunto** é uma coleção não ordenada e não indexada. Nenhum membro pode ser duplicado.
```python
#Exemplo 20-Conjuntos
palpite_1 = [1,10,20,45,55,60]
palpite_2 = [1,17,25,45,61,60]
conjunto = set(palpite_1+palpite_2)
print conjunto
```
- **Dicionário** é uma coleção desordenada, mutável e indexada. Nenhum membro pode ser duplicado.
```python
#Exemplo 21-Dicionário
identificacao_empregado = {"Nome": "Caio", "Sobrenome": "Santos", "Data_Nasc": '10/01/1983'}
dados_salariais = {"Salario":4576.17, "Comissao": "17%" }
identificacao_empregado.update(dados_salariais)
print identificacao_empregado
print identificacao_empregado["Nome"]
```
Lembra-se que na Aula 5 eu falei sobre dicionários e letra 'u' antes do texto? Agora você já sabe o que é e para que serve.


::: :pushpin: Resumo :::
Nesta aula você aprendeu:
- O que é uma variável e em que momento ela é criada
- Para que serve o coletor de lixo e quando ele atua
- Principais regras e boas práticas para nomes de variáveis
- Os tipo primitos do Python
- Os tipos de coleções e exemplos de uso: Lista, Tupla, Conjunto e Dicionário


#### Desafio 1 :innocent:

Agora que você já conhece o tipo `coleção` e a estrutura de laço `for`, escreva um programa para percorrer uma lista de nomes, mostrando todos os seus valores.

Por hoje é só. Na [Aula 7](Aula7.md) você vai aprender um pouco mais sobre os tipos texto do Python. Até!