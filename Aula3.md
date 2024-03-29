# Aula 3

## Sintaxe do Python

Nos próximos itens vamos mostrar os fundamentos da linguagem Python. Assim como o futebol tem seus fundamentos: cabecear, matar no peito, chute de 3 dedos etc, a linguagem Python, como qualquer outra linguagem de programação, tem sua própria maneira (sintaxe) de escrever as instruções fundamentais, ou simplesmente, os fundamentos.

Então vamos lá.

1. Continuação de linhas

Uma boa prática de programação é escrever as linhas do seu programa com a largura máxima de 80 colunas. Isso melhora a legibilidade do seu código e evita que o leitor tenha que ficar rolando a tela para direita e para a esquerda o tempo todo. 

Para evitar linhas muito longas o ideal é quebrá-las em 2 ou 3 linhas. Entretanto, quando vc quebra uma linha você tem que informar ao Python que a próxima linha é uma continuação da linha atual. Como fazer isso? 

Bem, para informar isso você deve usar o caractere de barra invertida `\` ao final da linha ou parênteses `(`, colchetes `[`, vírgulas `,` quando separando parâmetros e também as chaves `{`, em expressões que utilizam tais caracteres.

- Exemplo 1 - Continuação usando barra invertida:

```python 
#Exemplo-1
a="Python é uma linguagem interpretada e "\
  "muito poderosa!"
   
print a    

```

```
Python é uma linguagem interpretada e muito poderosa!
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
Ficou claro? 
Resumindo: 
 - Via de regra utilize o caractere `\` para indicar que uma linha continua na linha seguinte.
 - Se ao final da linha houver uma caractere `[`, `(`, `,` ou  `{`, não precisa usar o `\`.

2. Comentários

Em toda linguagem de programação os comentários servem para documentar o que está sendo realizado. Lembre-se: você não escreve um programa para você ler nem muito menos para a máquina (senão melhor seria usar o assembler), mas sim, para que outros possam ler.

Pensando nisso, você deve documentar o que está escrevendo, explicando em uma linguagem simples e concisa as instruções que não são tão intuitivas em uma primeira leitura.

Há duas formas de fazer comentário em Python

- Comentário de linha usando `#`

- Comentário de múltiplas linhas Usando `'''`   `'''`

- Exemplo 3 - Comentário de uma única linha

```python 
#Exemplo-3 - Comentário de uma única linha
#As instruções a seguir fazem uma iteração (caminhamento) em uma lista
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
#Exemplo-4 - Comentário de múltiplas linhas
'''
Este é um comentário de múltiplas linhas
Serve para documentar a rotina
Estas linhas serão ignoradas pelo interpretador, ou seja, não são interpretadas pela máquina
'''

```

3. Comentários Funcionais

Comentários funcionais geralmente são usados para 2 coisas:
-  1-alterar a codificação do arquivo fonte do programa acrescentando um comentário
com o texto “#-*- coding: <encoding> -*#-” no inicio do arquivo, onde <encoding> é a codificação do arquivo (geralmente latin1 ou utf-8). Alterar a codificação é necessário para suportar caracteres que não fazem parte da língua inglesa, no código fonte do programa.
- 2-definir o interpretador que será utilizado para executar o programa em sistemas UNIX, através de um comentário começando com “#!” no inicio do arquivo, que indica o caminho para o interpretador (geralmente a linha de comentário será algo como “#!/usr/bin/env python”).

Exemplo de comentários funcionais:

```python
#Exemplo-5 - Comentários funcionais

#!/usr/bin/env python 
# -*- coding: latin1 -*-
# Uma chamada de função (quebrada por vírgula)
c = range(1, 
          11)
print c
```

4. Blocos de código

Como o nome já diz um "bloco de código" é um conjunto de instruções escritas em Python que devem operar em conjunto, ou seja, um instrução em um bloco não está sozinha, mas agrupada com outras instruções. O Python tem vários tipos de bloco. Nós vamos falar deles nas próximas aulas. O importante aqui é que você entenda como instruir o Python que você está escrevendo um bloco de instruções e isso é feito com o uso do caractere `:`.
Importante dizer que dentro de um bloco é possível criar outros blocos (ou sub-blocos). O nome técnico para isso é "ninho" de blocos, ou seja, um bloco está "aninhado" dentro de outro bloco.

<p align="center">
  <img src="imagens/Bloco_Codigo.png" alt="Blocos de Código">
</p>
<p align="center">
   <strong>Figura 1-Blocos de Código Aninhados</strong> 
</p>

Conforme você pode observar na Figura 1, o sinal de `:` determina o ínicio de um bloco. As instruções que estão dentro de um bloco devem, obrigatoriamente, estar recuadas (usando-se a tecla `tab`, não use a barra de espaços).
Para aninhar um bloco dentro de outro bloco, basta fazer novo recuo. 

Vamos mostrar isso com um exemplo.

```python
#Exemplo-6 - Blocos de código
# Para i na lista 30, 60, 90, 120, 171:
for i in [30, 60, 90, 120, 172]:
# Se o resto dividindo por 3 for igual a zero:
    if i % 3 == 0: # Este bloco está aninhado ao bloco for...
        print i, '/ 3 =', i / 3
    else:
        print i,'Não é divisível por 3'
```
::: :pushpin: Resumo :::

Nesta aula nós vimos 4 importantes fundamentos da linguagem Python:
- Como fazer continuação de linhas 
- Como fazer comentários nos códigos
- O que são comentários funcionais e qual a sua sintaxe
- O que são e como fazer para criar blocos de código

Por hoje é só. 

Até a [Próxima Aula](Aula4.md)