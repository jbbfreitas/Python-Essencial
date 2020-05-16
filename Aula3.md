# Aula 3

## Sintaxe do Python

1. Continuação de linhas

As linhas em  Python  podem continuar nas linhas seguintes, pelo uso do caractere de barra invertida (\) ao final da linha ou parênteses, colchetes ou chaves, em expressões que utilizam tais caracteres.

- Exemplo 1 - Continuação usando barra invertida:

```python 
#Exemplo-1
a="Python é uma linguagem interpretada e "\
  "muito poderosa"
   
print a    

```

```
Python é uma linguagem interpretada e muito poderosa
```





- Exemplo 2 - Continuação usando colchete e parênteses:

```python 
#Exemplo-2
a = [1,2,3,4]+[
    10,20,30]

b= (3+2)*(
    8+2)
print "A variável 'a' é o resultado da soma de duas listas e vale {}".format(a)
print "A variável 'b' é o resultado de uma expressão e vale {}".format(b)
```

```
A variável 'a' é o resultado da soma de duas listas e vale [1, 2, 3, 4, 10, 20, 30]
A variável 'b' é o resultado de uma expressão e vale 50
```


2. Comentários

Em toda linguagem de programação os comentários servem para documentar o que está sendo realizado.
Há duas formas de fazer comentário em Python

- Comentário de linha usando `#`

- Comentário de múltiplas linhas Usando `'''`   `'''`

- Exemplo 3 - Comentário de uma única linha

```python 
#Exemplo-3
#Vamos fazer uma iteração em uma lista
lista = [1,2,3,4,5] #Uma lista de números inteiros
for x in lista:
    print x
```

```
1
2
3
4
5
```

```python
#Exemplo-4
'''
Este é um comentário de múltiplas linhas
Serve para documentar a rotina
Estas linhas serão ignoradas pelo interpretador
'''

```



    



O caractere # marca o inicio de comentário. Qualquer texto depois do # será ignorado até o fim da linha , com exceção dos comentários funcionais.
Comentários funcionais geralmente são usados para:
▪ alterar a codificação do arquivo fonte do programa acrescentando um comentário
com o texto “#-*- coding: <encoding> -*#-” no inicio do arquivo, aonde <encoding> é a codificação do arquivo (geralmente latin1 ou utf-8). Alterar a codificação é necessário para suportar caracteres que não fazem parte da linguagem inglesa, no código fonte do programa.
▪ definir o interpretador que será utilizado para rodar o programa em sistemas UNIX, através de um comentário começando com “#!” no inicio do arquivo, que indica o caminho para o interpretador (geralmente a linha de comentário será algo como “#!/usr/bin/env python”).
Exemplo de comentários funcionais:
