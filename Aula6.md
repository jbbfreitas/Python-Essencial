# Aula 6

## Tipos de dados no Python


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
época = "1900'
exceção = "Valor inválido"
2semestre=range[6,13]
```






```

  (sem acentuação) ou sublinhado (_) e seguido por letras (sem acentuação), dígitos ou sublinhados (_), sendo que maiúsculas e minúsculas são consideradas diferentes.
Existem vários tipos simples de dados pré-definidos no Python, tais como:
▪ Números (inteiros, reais, complexos, ... ).
▪ Texto.
▪ Booleanos.
Além disso, existem tipos que funcionam como coleções. Os principais são:
▪ Lista.
▪ Tupla.
▪ Dicionário.
Os tipos no Python podem ser:
▪ Mutáveis: permitem que os conteúdos das variáveis sejam alterados.
▪ Imutáveis: não permitem que os conteúdos das variáveis sejam alterados.
Em Python, os nomes de variáveis são referências, que podem ser alteradas em tempos de execução.