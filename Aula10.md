# Aula 10

## Funções

### Dividir para conquistar! 
Esse conceito foi utilizado pelo governante romano César (divide et impera). Em TI usamos essa regra para 'quebrar' um problema maior em pedaços menores e, resolvendo as partes,   juntá-las formando o todo novamente.

Esse conceito também encontra amparo na proposição do cientista canadense Craig Larman   que no seu livro  "Utilizando UML e Padrões" elenca 9 padrões que contribuem para a melhoria da qualidade de software, denominando-os de padrões GRASP. Um desses padrões  é o "Especialista na informação" (information expert). O padrão Especialista é usado  para atribuir responsabilidades ao especialista da informação. Isso significa que: é preciso delegar (atribuir responsabilidade) mas não a qualquer um e sim a um especialista. 

Dito isto nós podemos dizer que as funções são blocos de código especialistas em realizar determinadas operações (funções) para as quais devemos delegar responsabilidades com o objetivo de dividir para conquistar.

As funções são identificados por um nome, podem receber parâmetros pré-determinados e podem ou não retornar um valor.

No Python, as funções: 
- Podem retornar objetos, um ou mais valores, ou simplesmente, não retornar nada.
- Aceitam parâmetros opcionais (defaults). Se não for passado, o parâmetro será
igual ao valor default, definido na função.
- Aceitam que os parâmetros sejam passados com nome. Neste caso,a ordem em que
os parâmetros foram passados não importa.
- Tem escopo local, ou seja não afetam definições de
escopo global.
- São recursivas, ou seja, uma função pode invocar ela mesma

### Uma função bem simples.

```python
# Exemplo 39 - Função para somar dois números 
def calcula_soma(n1,n2):
    soma = n1+n2
    return soma

num1=10
num2=20
print "A soma de {} com {} ".format(num1,num2) + "é igual a " + str(calcula_soma(num1,num2))

```
### Um parâmetro que é uma lista.

```python
# Exemplo 40 - Função para somar números de uma lista
def somalista(numeros):
    soma = 0
    for i in numeros:
        soma = soma + i
    return soma

print(somalista([1,3,5,7,9]))
```

### Função com parâmetros opcionais.

```python
# Exemplo 41 - Função com parâmetros opcionais
def raiz(n, ind = 2):
    ind2 = 1 / float(ind)
    return n ** ind2
    
print raiz(16)  #raiz quadrada de 16
print raiz(8,3) #raiz cúbica de 8
```

::: :pushpin: Importante :::

> Obs 1: No exemplo 41 pode-se observar que o padrão é a raiz quadrada. Por isso, quando invocamos raiz(16), o resultado dá 4.0

> Obs 2: No exemplo 41 foi usado `float(ind)`. A operação 1/ind resultaria em um arredondamento e, consequentemente, erro no cálculo.

> Obs 3: Os argumentos com padrão devem vir por último, depois dos argumentos sem
padrão.

> Obs 4: O valor do padrão para um parâmetro é calculado quando a função é definida.

> Obs 5: Os argumentos passados sem identificador são recebidos pela função na forma de
uma lista e associados aos parâmetros na ordem em que são declarados.

> Obs 6: Os argumentos passados com identificador são recebidos pela função na forma de
um dicionário.

> Obs 7: Os parâmetros passados com identificador na chamada da função devem vir no fim da lista de parâmetros.

### Função com parâmetros opcionais, usando valores padrão nulo.

```python
## Exemplo 42 - Função com parâmetros opcionais
def dividir_texto(seq, inicio=None, fim=None, inc=None):
    """Implementação da dividao usando python"""
    return seq[inicio:fim:inc]

# Usando a funcão built in split
frase = 'um tigre, dois tigres, tres tigres, quatro tigres'.split()
print frase

# Usando a função criada
print dividir_texto(frase)
print dividir_texto(frase,inc=2)
print dividir_texto(frase,inicio=3,fim=5)
```

### Função com número de parâmetros variáveis.

```python
# Exemplo 43 - Função com número de parâmetros opcionais 
def args_variaveis(*lista1, **dic2):
    print 'lista1 pode ter números de parâmetros variáveis', lista1
    print 'dic2 é um dicionário', dic2

args_variaveis('um', 'dois', x=1, y=2, z=3)
args_variaveis('um', 'dois', 'tres', nome='Joao', endereco='Rua das Flores', complemenmto='Apto 1010')
```

::: :pushpin: Importante :::

>  *lista será associado a um conjunto variáveis de valores

>  **dic2 é um dicionário com número variável de parâmetros

### Função com retorno múltiplo de valores. 

```python
# Exemplo 44 - Função com retorno múltiplo de valores 
def retorno_multiplo(num):
    d = 2*num
    t = 3*num
    return d, t

dobro,triplo = retorno_multiplo(10)
print "O dobro é {}".format(dobro)
print "O triplo é {}".format(triplo)

```

Por intermédio desses exemplos você pode constatar o quanto a linguagem Python é poderosa e 
sofisticada.

Por hoje é só. Na [Aula 11](Aula11.md) você vai resolver um conjunto de exercícios usando o Python. Até mais!

