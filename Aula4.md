# Aula 4

Na aula 3 nós dissemos que o Python tem vários tipos de blocos e que o caractere `:` indica que estamos criando um bloco.

Nós iremos agora mostrar como fazer para alterar o fluxo normal de execução das instruções. 

## Controle do Fluxo

O fluxo normal de uma rotina escrita em qualquer linguagem de programação é `top-down`, ou seja, é uma sequencia de linhas de código que são executadas de cima (`top`) para baixo (`down`). Ocorre, entretanto, que em diversas ocasiões pode ser necessário alterar esse fluxo normal, por exemplo, executar uma determinada linha apenas se uma determinada condição for verdadeira. É para isso que existem os chamados `controles de fluxo`. 

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

> Observe  que Python é uma linguagem `case sensitive`, ou seja, diferencia caracteres maiúsculos de minúsculos. Assim, por exemplo, se você der um nome para uma variável de `Temperatura` ela será diferente da variável `temperatura`. Faço questão de frisar isso aqui por que as instruções são grafadas em mínúsculo (`if`, `elif`, `else`), isto é, se você usar `IF` o Python vai informar que há um erro na sua sintaxe.

Que tal você experimentar esse trecho de código do Exemplo 7? Faça isso em uma nova célula do Jupyter. Não há nenhum problema se você não entender a sintaxe completa. O objetivo aqui é você entender o bloco de código `if`.

2. `SE` `inline`

Em algumas situações, como por exemplo no uso de `lambda` (que será visto mais adiante), é desejável que a instrução `if else` esteja escrita em uma única linha (**inline**).    

```python
clima = 'muito quente' if temperatura > 35 else 'suportável'
```
Veja que legal! No exemplo acima o `if` não é um bloco, por isso não usa o `:`, por estar escrito em uma só linha. Esse comando é chamado de  ` if in line` (if em uma só linha).

3. Operadores lógicos

Os operadores lógicos são usados para  construir condições mais complexas para fazer o controle do fluxo.

Explicando melhor: suponha que você queira mostrar uma mensagem de boas vindas que depende de duas informações: o e-mail e a senha. Neste caso você terá que verifica se a senha está correta `e` se o e-mail está correto. Esse `e`em Python é o que se chama de conector `and`. Então voc6e escreveria algo mais ou menos assim:

```python
if e-mail=='o email' and senha=='a senha': 
    print 'Seja bem-vindo ao nosso site'
else
    print 'O e-mail ou a senha informados esstão incorretos'
```        

Os operadores lógicos em Python são os seguintes: `and`, `or`, `not`, `is` e `in`.

-  `and` : avalia duas expressões e retorna verdadeiro <b>se e somente se</b> ambas são forem verdadeiras.

- `or` : avalia duas expressões e retorna verdadeiro se uma ou ambas as expressões forem
verdadeiras.

- `not` : nega uma expressão, ou seja, se ela for verdadeira, passa a ser falsa e vice-versa.

- `is` : usado para verificar se um objeto é uma instância de uma classe.

- `in` : usado para verificar se um elemento está contido em uma lista

```python
#Exemplo 8- Operadores lógicos

estado_civil = ['Solteiro', 'Casado', 'Viúvo','Separado','Amasiado']
es = raw_input('Favor informar o estado civil:')
if not(es in estado_civil): 
    print 'Estado civil inválido!'
else: 
    print 'Obrigado pela sua informação'    

```

Na 3a linha da listagem acima, temos dois operadores `not` e `in`. Essa linha quer 
dizer o seguinte:

Se o estado civil informado não estiver contido na lista `estado_civil` então escreva `Estado civil inválido`. Se tiver contido, então escreva `Obrigado pela sua informação`.

::: :pushpin: Resumo :::

> Nesta aula você aprendeu como alterar (controlar) o fluxo normal `top-down` usando as seguintes instruções:
1. `if`....`elif`....`else`
2. `if` `inline`
3. Os operadores: `and`, `or`, `not`, `is` e `in`

#### Desafio 1 :innocent:
Escreva em Python um trecho de programa usando os operadores `if` e `and`

#### Desafio 2 :innocent:
Escreva em Python um trecho de programa usando os operadores `if`, `not` e `or`

Por hoje é só. Na [Aula 5](Aula5.md) você vai aprender usar laços. Até.








