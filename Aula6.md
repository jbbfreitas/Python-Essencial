# Aula 6

## Tipos de dados no Python

### 1-Variáveis
As variáveis no Python são criadas quando se atribui um valor a essas variáveis. Assim como em outras linguagens, como o java por exemplo, existe um coletor de lixo `garbage collector` que atua quando não existe mais nenhuma referência àquela variável.

Vamos dizer a mesma coisa com um exemplo:

```python
a=20
b=a
c=b
```
O que ocorre aqui é que as 3 variáveis: `a`, `b` e `c` apontam (são referências) para o mesmo endereço de memória onde está armazenado o valor `20`.

Somente quando as 3 variáveis não apontarem mais para esse endereço é que o coletor de lixo vair liberar o endereço (limpar).

Existem algumas regras para o nome de variáveis. Vamos mostra-las:

1. Os nomes das variáveis devem começar com uma letra. Não podem começar por caracteres especiais, tais como `á`, `ç`.
2. Podem iniciar com um `underline` (_).
3. Após o primeiro caracter, pode ser seguido por números ou  `underline` (_).

Exemplos de variáveis válidas:

```python
nome123 = 'João'
_salario = 12.45
data_nascimento='12/12/1970'
```

Exemplos de variáveis *inválidas*:

```python
época = "1900" #começa com é
exceção = "Valor inválido" #contém caractere especial `ç`
2semestre=range[6,13] #começa com número
```

Além das regras, existem as boas práticas:

1. Nomes de variáveis devem começar com letras minúsculas
2. Nomes compostos devem ser separados com o caráctere `_`
3. Evitar o uso do `Camel Case` que é a prática de escrever palavras compostas ou frases de modo que cada palavra ou abreviatura no meio da frase comece com uma letra maiúscula.
4. Para mais detalhes, consulte o [Guia de codificação para Python](https://www.python.org/dev/peps/pep-0008/#function-and-variable-names)

### 3-Tipos primitivos (simples)

Existem vários tipos simples de dados pré-definidos no Python, tais como:
- Números (inteiros, reais, complexos, ... ).
Exemplo:

```python
contador =10 # Tipo inteiro
salario = 5482.34 #Tipo real
x= 10+3j #Número complexo. O `j` é a parte imaginária do número complexo
```

- Texto.
```python
nome ='Carlos R Cadete' # Tipo texto
endereco ="Rua Domingos Ferreira" # Tipo texto
salario = 5482.34 #Tipo real
diametro_da_terrra = 12.742e3 #Real em notação científica
print 'O diâmetro da terrra é de {} Km'.format(diametro_da_terrra)
x= 10+3j #Número complexo. O `j` é a parte imaginária do número complexo
print x
```


- Booleanos.
```python
v1 = True
v2=bool(False) # atribui False
v3=bool(None)) # atribui False
v4=bool(1)) # atribui True
```

### 4-Tipos coleções 

Os principais são:
- **Lista** é uma coleção que é ordenada e mutável. Permite membros duplicados.

```python
nomes = ['Mara', 'José', 'Camilo']
dias_da_semana = [1,2,3,4,5,6,7]
temperaturas = [32,27,-4,32,17, 27,-4]
```

- **Tupla** é uma coleção que é ordenada e imutável. Permite membros duplicados.
```python
frutas = ("apple", "banana", "cherry") #OK
frutas = ("grape", "banana") #OK
frutas = frutas + ("avocado", "guava") #OK
frutas[0] = "orange" # Tentativa de alterar `grape` por `orange`. Erro aqui, as tuplas são imutáveis
print frutas
```

- **Conjunto** é uma coleção não ordenada e não indexada. Nenhum membro duplicado.
```python
palpite_1 = [1,10,20,45,55,60]
palpite_2 = [1,17,25,45,61,60]
conjunto = set(palpite_1+palpite_2)
print conjunto
```
- **Dicionário** é uma coleção desordenada, mutável e indexada. Nenhum membro duplicado.
```python
identificacao_empregado = {"Nome": "Caio", "Sobrenome": "Santos", "Data_Nasc": '10/01/1983'}
dados_salariais = {"Salario":4576.17, "Comissao": "17%" }
identificacao_empregado.update(dados_salariais)
print identificacao_empregado
print identificacao_empregado["Nome"]
```
Lembra-se que na Aula 5 eu falei sobre dicionários? Agora você já sabe o que é e para que serve.
Por hoje é só. Na [Aula 7](Aula7.md) você vai aprender um pouco mais sobre os tipos texto do Python. Até!