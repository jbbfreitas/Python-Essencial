# Aula 9

# Dicionários

Um dicionário é uma lista contendo um conjunto de chaves e valores, isto é, uma chave (identificador) única é associada a um ou mais valores. As chaves devem ser do tipo imutável (podendo ser uma String, Inteiro ou uma Tupla).

Os valores dos dicionários são mutáveis, tais como as listas.

O dicionário do Python não fornece garantia de que as chaves estarão ordenadas.

Exemplo:
```python

dict1 = {1:"Domingo", 2:"Segunda-Feira", 3:"Terça-Feira",
4:"Quarta-Feira", 5:"Quinta-Feira", 6:"Sexta-Feira", 7:"Sábado"}


print dict1[2] # Irá imprimir "Segunda-Feira"
```

## Um dicionário pode conter outro dicionário

Sim, pode-se usar um valor que também é um dicionário.

Exemplo:
```python

despesas = {'Energia': 100.45, 'Agua': 54.33, 'Cartao': {'Visa': 500.33, 'Master': 125.66, 'American': 0}}

print "As despesas com cartão Master foi {}".format(despesas['Cartao']['Master'])
```

