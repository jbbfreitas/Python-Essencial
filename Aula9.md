# Aula 9

# Dicionários

Um dicionário é uma lista contendo um conjunto de chaves e valores, isto é, uma chave (identificador) única é associada a um ou mais valores. As chaves devem ser do tipo imutável (podendo ser uma String, Inteiro ou uma Tupla).

Os dicionários são muito similares à notação [JSON](https://www.w3schools.com/python/python_json.asp), utilizada no protocolo [REST](https://becode.com.br/o-que-e-api-rest-e-restful/) para comunicação cliente-servidor por intermédio do protocolo HTTP.

Os valores dos dicionários são mutáveis, tais como as listas.

O dicionário do Python **não fornece garantia** de que as chaves estarão ordenadas.

Exemplo:
```python
# Exemplo 35 - Dicionário 
# Um dicionário que relacionada os dias da semana ao seu respectivo número
dict1 = {1:"Domingo", 2:"Segunda-Feira", 
         3:"Terça-Feira",4:"Quarta-Feira", 
         5:"Quinta-Feira", 6:"Sexta-Feira", 
         7:"Sábado"}


print dict1[2] # Irá imprimir "Segunda-Feira"
```

## Um dicionário pode conter outro dicionário

Sim, pode-se usar um valor que também é um dicionário. E isso torna os dicionários ainda mais interessantes, já que um valor pode, na verdade, ser também um dicionário.

Observe o exemplo 36. Nesse exemplo a chave 'Cartao' contém não apenas um valor, mas os valores gastos (no mês por exemplo) em 3 bandeiras: Visa, Master e American.

Exemplo:
```python
# Exemplo 36 - Dicionário 
despesas = {'Energia': 100.45, 'Agua': 54.33, 'Cartao': {'Visa': 500.33, 'Master': 125.66, 'American': 0}}

print "As despesas com cartão Master foi {}".format(despesas['Cartao']['Master'])
```

## Adicionando elementos a um dicionário

A adição de elementos a um dicionário pode ser feita de várias maneiras:
- Um valor por vez,  por exemplo: dict [Chave] = "Valor". 
- Atualizar um valor em um Dicionário usando o método `update()`.


::: :pushpin: Importante :::

> Ao adicionar um valor ao dicionário, com uma chave já existente, o valor será atualizado, caso contrário, uma nova entrada `chave-valor` será adicionada ao Dicionário.

### Exemplo:
```python
# Exemplo 37 - Dicionário 
# Criando dicionário vazio
dic1 = {} 
print("Dicionário Vazio: ") 
print(dic1) 

# Adicionando elementos um a um 
dic1[0] = 'Pele'
dic1[2] = 'Rivelino'
dic1[3] = 10
print("\nDicionário após adicionar 3 elementos: ") 
print(dic1) 

# Adicionando um conjunto de valores  
# para uma única chave 
dic1['dic2'] = 2, 3, 4
print("\nDicionário após adicionar um dicionário aninhado: ") 
print(dic1) 

# Atualizando valores de uma chave 
dic1[0] = 'Rei Pele'
dic1[2] = 'Rivelino era um craque'
print("\nFoi atualizada uma chave: ") 
print(dic1) 

# Adicionando um dicionário a um dicionário 
dic1[5] = {'dic2' :{'1' : 'Vida', '2' : 'Mar'}} 
print("\nAdicionando um dicionário: ") 
print(dic1) 
```

## Resultados
```
Dicionário Vazio: 
{}

Dicionário após adicionar 3 elementos: 
{0: 'Pele', 2: 'Rivelino', 3: 10}

Dicionário após adicionar um dicionário aninhado: 
{0: 'Pele', 2: 'Rivelino', 3: 10, 'dic2': (2, 3, 4)}

Foi atualizada uma chave: 
{0: 'Rei Pele', 2: 'Rivelino era um craque', 3: 10, 'dic2': (2, 3, 4)}

Adicionando um dicionário: 
{0: 'Rei Pele', 2: 'Rivelino era um craque', 3: 10, 'dic2': (2, 3, 4), 5: {'dic2': {'1': 'Vida', '2': 'Mar'}}}
```

## Removendo elementos a um dicionário


Em um dicionário, a exclusão de chaves pode ser feita usando a palavra-chave `del`. 
Ao usar o `del`, um valor específico de um dicionário ou até mesmo todo o dicionário podem ser excluídos, bem como um dicionário aninhado.

::: :pushpin: Importante :::
`del` Dict excluirá todo o dicionário e, portanto, imprimi-lo após a exclusão gerará um erro.

### Exemplo:

```python
# Exemplo 38 - Dicionário 
# Criando dicionário vazio
dic1 = {} 
dic1[0] = 'Pele'
dic1[2] = 'Rivelino'
dic1[3] = 10
dic1['dic2'] = 2, 3, 4
dic1[0] = 'Rei Pele'
dic1[2] = 'Rivelino era um craque'
dic1[5] = {'dic2' :{'1' : 'Vida', '2' : 'Mar'}} 
print("\nDicionário logo após ser criado: ") 
print dic1

#Excluindo um elemento
del dic1[2]
print("\nDicionário após excluir o elemento 2: ") 
print dic1

#Excluindo um dicionário aninhado
del dic1[5]
print("\nDicionário após excluir o elemento 5: ") 
print dic1
```
## Resultados
```
Dicionário logo após ser criado: 
{0: 'Rei Pele', 2: 'Rivelino era um craque', 3: 10, 'dic2': (2, 3, 4), 5: {'dic2': {'1': 'Vida', '2': 'Mar'}}}

Dicionário após excluir o elemento 2: 
{0: 'Rei Pele', 3: 10, 'dic2': (2, 3, 4), 5: {'dic2': {'1': 'Vida', '2': 'Mar'}}}

Dicionário após excluir o elemento 5: 
{0: 'Rei Pele', 3: 10, 'dic2': (2, 3, 4)}
```

## Tabela 1 - Dicionários: outros métodos importantes:


| métodos       | Descrição             |
| ------------- |---------------------|
|copy()	    |O método copy () retorna uma cópia superficial do dicionário.|
|clear()	|O método clear () remove todos os itens do dicionário.|
|pop()	    |Remove e retorna um elemento de um dicionário que possui a chave fornecida.|
|popitem()	|Remove o par de valor-chave arbitrário do dicionário|
|get()	    |É um método convencional para acessar um valor para uma chave.|
|str()	    |Produz uma representação de sequência imprimível de um dicionário.|
|update()	|Adiciona pares de valores-chave do dicionário|
|keys()	    |Retorna a lista de chaves do dicionário|
|items()	|Retorna uma lista dos pares de tuplas do dicionário (chave, valor)|
|has_key()	|Retorna `True` se há chave no dicionário dict, `False` caso contrário|
|fromkeys()	|Cria um novo dicionário com chaves de seq e valores definidos como valor.|
|type()	    |Retorna o tipo da variável passada.|
|cmp()	    |Compara elementos de ambos os ditados.|

```python
# Exemplo 38-A - 
# Usando alguns métodos do objeto dicionário 
dic1 = {}
dic1 = {"nome":"Joao Bosco","endereco":{"rua":"Rua Fulano de Tal", "numero":"1717", "complemento":"Apto 01"}}
dic2 = dic1.copy()
# Cria um dicionário denominado endereco
localizacao = {"rua":"Rua Fulano de Tal", "numero":"1717", "complemento":"Apto 01", "bairro":"Copa"}
#Altera o dic2 com o novo endereco
dic2["endereco"] = localizacao
print "1)=====Conteúdo de dic1====="
print dic1
print "2)=====Conteúdo de dic2, copiado de dic1 e com endereço alterado====="
print dic2
print "3)=====Removendo o endereco de dic2, com o método pop()====="
dic2.pop("endereco") 
print "4)=====Conteúdo de dic2, após remover o endereco com o método pop()====="
print dic2
print "5)=====Adicionando o endereco de dic2, com o método update()====="
dic2.update({"endereco":localizacao}) #Adiciona novamente a chave endereço contendo o dicionário endereco
print "6)=====Conteúdo de dic2, após adicionar o endereco com o método uppdate()====="
print dic2
```

## Resultados
>
>1)=====Conteúdo de dic1=====

> {'endereco': {'rua': 'Rua Fulano de Tal', 'complemento': 'Apto 01', 'numero': '1717'}, 'nome': 'Joao Bosco'}

> 2)=====Conteúdo de dic2, copiado de dic1 e com endereço alterado=====

>{'endereco': {'bairro': 'Copa', 'rua': 'Rua Fulano de Tal', 'complemento': 'Apto 01', 'numero': '1717'}, 'nome': 'Joao Bosco'}

>3)=====Removendo o endereco de dic2, com o método pop()=====

>4)=====Conteúdo de dic2, após remover o endereco com o método pop()=====

>{'nome': 'Joao Bosco'}

>5)=====Adicionando o endereco de dic2, com o método update()=====

>6)=====Conteúdo de dic2, após adicionar o endereco com o método uppdate()=====

>{'endereco': {'bairro': 'Copa', 'rua': 'Rua Fulano de Tal', 'complemento': 'Apto 01', 'numero': '1717'}, 'nome': 'Joao Bosco'}

## Fazendo uma iteração em um dicionário

Um recurso importando quando você utiliza os dicionários, é poder exibir um a um os seus elementos, usando a estrutura de loop `for`. Veja o exemplo abaixo.

# Exemplo 38-B - 
# Usando o for para fazer a iteração em um dicionário

Usando-se o método keys() do dicionário, é possível fazer a iteração para exibir, separadamente, as chaves e os valores.

```python
dic1 = {}
dic1 = {"nome":"Joao Bosco","endereco":{"rua":"Rua Fulano de Tal", "numero":"1717", "complemento":"Apto 01"}}
for chave in dic1.keys():
    print "Chave->"+chave
    print "Valores->"+str(dic1[chave])
    print " "
```



::: :pushpin: Importante :::

Os dicionários são essenciais na utilização do Python na Ciência de Dados. 

#### Desafio 1 :innocent:
Tomando como base o Exemplo 38-A, crie um dicionário e experimente outros métodos da Tabela 1.


Por hoje é só. Na [Aula 10](Aula10.md) você vai aprender a criar funções no Python. Até mais!
