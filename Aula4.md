# Aula 4

Na aula 3 nós dissemos que o Python tem vários tipos de blocos e que o caractere `:` indica que estamos criando um bloco.

Nós iremos agora detalhar os vários tipos de blocos, explicando para que serve cada um deles. 

## Controle do Fluxo

O fluxo normal de uma rotina escrita em qualquer linguagem de programação é `top-down`, ou seja, é uma sequencia de linhas de código que são executadas de cima (`top`) para baixo (`down`). Ocorre, entretanto, que em diversas ocasiões pode ser necessário alterar esse fluxo normal. É para isso que existem os chamados `controles de fluxo`. 

Vajamos os principais controles de fluxos existentes na linguagem.

1. `SE`....`SENÃO SE`....`SENÃO`

Em python esse controle é escrito da seguinte forma:

```python
#Exemplo 7- Controle do fluxo (if)

temperatura = int(raw_input('Entre com a temperaturaeratura (exemplo 27): '))
if temperatura < 0:
    print 'Nossa! Está fazendo {} graus. Está muito frio ...'.format(temperatura)
elif 0 <= temperatura <= 15: 
    print 'Está fazendo {} graus. Está frio ...'.format(temperatura)
elif 16 <= temperatura <= 25: 
    print 'Está fazendo {} graus. Está bem agradável a temperatura ...'.format(temperatura)
elif 26 <= temperatura <= 35: 
    print '{} graus de temperatura pede um chopp!'.format(temperatura)
else:
    print '{} graus, é muito quente! Um banho de agua gelaaaaada'
```
> Observe que a instrução `senão se` é `elif` e NÃO `elseif`. Observe ainda que o sinal `:`, assim como mostrado na [Aula 3](Aula3.md), define o início de um bloco de código e que, após esse sinal, as instruções devem estar recuadas por um `tab`.

> A última instrução é um `SENÃO` que em python é o `else`.

> A última observação é que Python é uma linguagem `case sensitive`, ou seja, diferencia caracteres maiúsculos de minúsculos. Assim, por exemplo, a variável `Temperatura` é diferente da variável `temperatura`. Fiz questão de frisar isso aqui por que a instruções são grafadas em mínúsculo (`if`, `elif`, `else`).

Que tal você experimentar esse trecho de código do Exemplo 7? Faça isso em uma nova célula do Jupyter.

2. `SE` `inline`

Em algumas situações, como por exemplo no uso de `lambda` (que será visto mais adiante), é desejável que a instrução `if else` seja escrita em uma única linha (**inline**).    

```python
clima = 'muito quente' if temperatura > 35 else 'suportável'
```

3. Operadores lógicos

Os operadores lógicos são usados para  construir condições mais complexas para fazer o controle do fluxo.

Os operadores lógicos em Python são os seguintes: `and`, `or`, `not`, `is` e `in`.

-  `and` : avalia duas expressões e retorna verdadeiro se e somente se ambas são
verdadeiras.

- `or` : avalia duas expressões e retorna verdadeiro se uma ou ambas as expressões são
verdadeiras.

- `not` : nega uma expressão, ou seja, se ela for verdadeira, passa a ser falsa e vice-versa.

- `is` : usado para verificar se um objeto é uma instância de uma classe.

- `in` : usado para verificar se um elemento está contido em uma lista

```python
#Exemplo 8- Operadores lógicos

estado_civil = ['Solteiro', 'Casado', 'Viúvo','Separado','Amasiado']
es = raw_input('Favor informar o estado civil:')
if not(es in estado_civil): print 'Estado civil inválido!'
else: print 'Obrigado'    

```

Por hoje é só. Na [Aula 5](Aula5.md) você vai aprender usar laços. Até.








