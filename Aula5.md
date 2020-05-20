# Aula 5

## Laços


Como em qualquer linguagem de programação o Python possui diversas estruturas de repetição que podem ser utilizadas sempre que um conjunto (bloco) de instruções precisar ser executado uma ou mais vezes. Essas estruturas de repetição são denominadas `laços` ou `loop`. 

Cada vez que as instruções do bloco é executada diz-se que foi realizado um ciclo ou iteração. Cada iteração  de um `loop` é executada até que uma determinada condição seja atingida. 

É possível inserir um laço dentro de outro laço. Isso é o que se denomina de laços ninho de laços ou laços aninhados.

Vou mostrar duas estruturas de repetição do Python: `while` e `for`

### 1. while

A estrutrua `while` (enquanto em inglês) é utilizada para repetir um bloco de instruções **enquanto** um condição for válida.

Dessa forma a sintaxe do `while` é a seguinte:

```python
while <condição>:
    instrução 1
    instrução 2
    ...
    instrução n

```
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
