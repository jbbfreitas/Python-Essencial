# Aula 7

## Entendendo um pouco mais o tipo Texto

Os textos no Python são tratados como `string`.

Uma `string` é qualquer sequência de caracteres. Um caractere é a menor unidade de todo o texto. Os caracateres são classificados em 3 grupos: numérico, letras do alfabeto e caracteres especiais.
As `strings` no Python são imutáveis, isto é, após criada,  não é possível adicionar, remover ou mesmo modificar algum dos seus caracteres. Para realizar essas operações, o Python precisa criar um nova `string`.

### 1. Exemplo de strings:

```python
#Exemplo 22-Strings
animal = 'Camelo'
print 'O ' + animal + ' pode ficar até 8 dias sem beber água!' # Concatenação
print 'A variável "%s" tem %d caracteres' % (animal, len(animal)) # Interpolação
for um_char in animal: print um_char # String tratada como seqüência
if animal.startswith('C'): print animal.upper() # Strings são objetos
print 3 * animal  # Pode isso ? Pode!

```

Símbolos usados na interpolação:
- %s: string.
- %d: inteiro.
- %f: real.

```python
#Exemplo 23-formatando com %
print("%s %s" %('Olá','Mundo'))

#Exemplo 24-formatando com % 
name = 'Mundo'
program ='Python'
print('Olá %s! Este é o %s.'%(name,program))

#Exemplo 25-str.format
name = 'Mundo' 
program ='Python'
print('Olá {}! Este é o {}.'.format(name, program))


#Exemplo 26-format com substituição de variáveis
name = 'Mundo' 
program ='Python'
print('Olá {nome}! Este é o {linguagem}.'.format(linguagem=program,nome=name))


#Exemplo 27-Novidade no Python 3.6  - Interpolação usando o f
name = 'World'
program = 'Python'
print(f'Hello {name}! This is {program}')

```

::: :pushpin: Importante :::

- O uso do % é uma forma antiga de fazer  interpolação e seu uso é desaconselhado pois a legibilidade do código fica compremetida.
- No método str.format() nós passamos o objeto string para a função format para a interpolação da string
- A interpolação via substituição de variáveis é muito poderosa e favorece a legibilidade do código.

### 2. Dividindo strings:


<p align="center">
  <img src="imagens/Substrings.png" alt="Dividindo string em pedaços">
</p>
<p align="center">
   <strong>Figura 1-Dividindo string em pedaços</strong> 
</p>
