# Aula 9

# Dicionários

Um dicionário é uma lista contendo um conjunto de chaves e valores, isto é, uma chave (identificador) única é associada a um ou mais valores. As chaves devem ser do tipo imutável (podendo ser uma String, Inteiro ou uma Tupla).

Os valores dos dicionários são mutáveis, tais como as listas.

O dicionário do Python não fornece garantia de que as chaves estarão ordenadas.

Exemplo:
```python

dict1 = {1:"Domingo", 2:"Segunda-Feira", 
         3:"Terça-Feira",4:"Quarta-Feira", 
         5:"Quinta-Feira", 6:"Sexta-Feira", 
         7:"Sábado"}


print dict1[2] # Irá imprimir "Segunda-Feira"
```

## Um dicionário pode conter outro dicionário

Sim, pode-se usar um valor que também é um dicionário.

Exemplo:
```python

despesas = {'Energia': 100.45, 'Agua': 54.33, 'Cartao': {'Visa': 500.33, 'Master': 125.66, 'American': 0}}

print "As despesas com cartão Master foi {}".format(despesas['Cartao']['Master'])
```

## Adicionando elementos a um dicionário

A adição de elementos a um dicionário pode ser feita de várias maneiras:
- Um valor por vez,  por exemplo: dict [Chave] = "Valor". 
- Atualizar um valor em um Dicionário usando o método `update()`.


::: :pushpin: Importante :::

> Ao adicionar um valor ao dicionário, com uma chave já existente, o valor será atualizado, caso contrário, uma nova entrada `chave-valor` será adicionada ao Dicionário.

```python
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
