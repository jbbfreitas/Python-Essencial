# Aula 12

## Módulos

### Por que usar módulos?

A modularização de uma aplicação é algo extremamente importante. Ela deve ser feita por duas razões:

- Para escrever módulos e reutilizar o código escrito em outras aplicações;
- Queremos que o código de nossa aplicação esteja organizado de modo a facilitar o controle e o entendimento do todo. Os módulos "ocultam" certos detalhes que não precisam ser entendidos para a compreensão do todo, criando,  para usar o linguajar o  'paradigma orientado a objetos', uma espécie de 'abstração'.

### O que são os módulos em Python?
Módulos são arquivos de código Python cuja interface é conhecida e que podem ser importados por outros módulos. Podem conter qualquer estrutura do Python e são executados quando importados. Eles são compilados quando importados pela primeira vez e armazenados em arquivo (com extensão “.pyc” ou “.pyo”), possuem namespace próprio são objetos no padrão 'Singleton', isto é, só é carregada uma instância em memória, que fica disponível de forma global para o programa.

Quando um programador importar um módulo, ele saberá (ou tem meios de saber) quais funções e classes o módulo possui. Ele também saberá como usá-las, isto é, conhecendo seus nomes, parâmetros, que excessões pretende tratar, dentre outras características.

### Como os módulos são carregados?

Os módulos são localizados pelo interpretador através da lista de pastas PYTHONPATH (sys.path), que normalmente inclui a pasta corrente em primeiro lugar. O módulo principal de um programa tem a variável __name__ igual à “__main__”. PYTHONPATH é uma variável ambiental, assim como CLASSPATH do java.

Os módulos são carregados através da instrução import. Desta forma, ao usar alguma estrutura do módulo, é necessário identificar o módulo. Isto é chamado de importação absoluta.

Por exemplo:

```python
import os 
...
print os.name
```
Também possível importar módulos de forma relativa:

Por exemplo:

```python
from os import name 
...
print name
```

O caractere “*” pode ser usado para importar tudo que está definido no módulo:

```python
from os import * 

print name
```
::: :pushpin: Importante :::

>Por evitar problemas como a ofuscação de variáveis, **a importação absoluta é uma prática melhor de programação do que a importação relativa**.

### Criando um primeiro Módulo

- Em um editor de textos qualquer, por exemplo o VSCode, crie um arquivo com o seguinte conteúdo, grave-o com o nome de Meu_Modulo.py :

```python
# -*- coding: latin1 -*-
"""
Meu_Modulo => rotinas utilitárias para aritmética 
"""

def somar(a,b):
    return a+b

def subtrair(a,b):
    return a-b

def multiplicar(a,b):
    return float(a)*float(b)

def dividir(a,b):
    return float(a)/float(b)
```

No JupyterNotebook crie a célula abaixo e execute-a:

```python
from Meu_Modulo import *

print somar(10,20)
print subtrair(10,20)
print dividir(10,20)
print multiplicar(10,20)
```

### Módulos da biblioteca padrão
É comum dizer que o Python vem com “baterias inclusas”, em referência a vasta biblioteca de módulos e pacotes que é distribuída com o interpretador.

Alguns módulos importantes da biblioteca padrão:
- Sistema: os, glob, shutils, subprocess.
- Threads: threading.
- Persistência: pickle, cPickle.
- XML: xml.dom, xml.sax, elementTree (a partir da versão 2.5).
- Configuração: ConfigParser, optparse.
- Tempo: time, datetime.
- Outros: sys, logging, traceback, types, timeit.




