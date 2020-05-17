# Aula 4

## Controle do Fluxo

O fluxo normal de uma rotina escrita em qualquer linguagem de programação é `top-down`, ou seja, é uma sequencia de linhas de código escritos em determinadas linguagem que são executadas de cima para baixo (top-down). Ocorre, entretanto, que em diversas ocasiões é necessário alterar esse fluxo normal. É para isso que existem os chamados `controles de fluxo`. 

Vajamos os principais controles de fluxos existentes na linguagem.

1. `Se`....`senão`....`senão se`

Em python esse controle é escrito da seguinte forma:

```python
#Exemplo 7- Controle do fluxo (if)

temperatura = int(raw_input('Entre com a temperaturaeratura (exemplo 27): '))
if temperatura < 0:
    print 'Nossa! Está fazendo {} graus. Está muito frio ...'.format(temperatura)
elif 0 <= temperatura <= 15: 
    print 'Está fazendo {} graus. Está frio ...'.format(temperatura)
elif 16 <= temperatura <= 25: 
    print 'Está fazendo {} graus. Está bem boa a temperaturaeratura ...'.format(temperatura)
elif 26 <= temperatura <= 35: 
    print '{} graus de temperaturaeratura pede um chopp!'.format(temperatura)
else:
    print '{} graus, é muito quente! Um banho de agua gelaaaaada'
```
> Observe que a instrução `senão se` é `elif` e NÃO `elseif`. Observe ainda que o sinal `:`, assim como mostrado na [Aula 3](Aula3.md), define o início de um bloco de código e que, após esse sinal, as instruções devem estar recuadas por um `tab`.

> A última instrução um `SENÃO` que em python é o `else`.







