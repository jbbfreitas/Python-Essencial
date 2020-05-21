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
x= 10+3j #Número complexo. O `j` é a parte imaginária do número complexo
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
- **Tupla** é uma coleção que é ordenada e imutável. Permite membros duplicados.
- **Conjunto** é uma coleção não ordenada e não indexada. Nenhum membro duplicado.
- **Dicionário** é uma coleção desordenada, mutável e indexada. Nenhum membro duplicado.


Os tipos no Python podem ser:
▪ Mutáveis: permitem que os conteúdos das variáveis sejam alterados.
▪ Imutáveis: não permitem que os conteúdos das variáveis sejam alterados.
Em Python, os nomes de variáveis são referências, que podem ser alteradas em tempos de execução.