# Aula 13

## Pacotes

De uma forma bem simples, um pacote é uma coleção de módulos.
Quando os módulos tornam-se muito grandes o ideal é subdividi-lo em vários módulos e depois agrupar os módulos em um determinado pacote. O ideal é planejar o pacote para conter módulos que tratam de assuntos similares.

Os pacotes servem também para evitar a chamada colisão de nomes, isto é, quando você tem dois módulos com o mesmo nome mas que, na verdade, executam de forma diferente. Então o ideal é invocar um módulo na forma de `pacote.modulo` ou `pacote.modulo.funcao`. 

Enquanto os módulos são estruturados em arquivos, conforme visto na aula 12, os pacotes são estruturados em pastas. Todos os pacotes devem, obrigatoriamente, conter um arquivo denominado `__init__.py`. Esses arquivos são necessários para informar o interprestador que uma deeterminada pasta é um pacote de módulos. Em alguns casos, os arquivos `__init.py__` são simplesmente arquivos vazios, em outros, porém, esses arquivos contém um variável denominada `__all__` que é uma lista contendo os módulos daquele pacote.


Para você entender melhor o conceito de pacotes, vamos ver tudo isso na prática:

Crie uma estrutura de diretórios conforme a Figura 1.

<p align="center">
  <img src="imagens/ArvorePacotes.png" alt="Árvore de pacotes para o exemplo">
</p>
<p align="center">
   <strong>Figura 1-Árvore de Pacotes do Exemplo</strong> 
</p>

Na verdade todos os arquivos estão vazios, com excessão do `aritmetica.py`, pois este é apenas um exemplo para você entender melhor o conceito por detrás dos pacotes python.

No arquivo `aritmetica.py` digite:

```python
# _*_ coding: utf-8 _*_

def soma(n1,n2):
    return n1+n2

def divisao(n1,n2):
    return n1/n2    

```
### Existem 3 formas de acessar 

```python
#Forma 1- usar o from com o name space completo e em seguida import *
#Mais simples mas deve ser evitada pois pode causar colisão de nomes
from pacote_utilitario.matematica.aritmetica import * 
print soma(10,20)
```

```python
#Forma 2- usar o import * e invocar o metodo usando o name space completo
#Muito trabalhosa
from pacote_utilitario import *
print matematica.aritmetica.soma(10,20)
```

```python
#Forma 3- usar o name space completo e dar um apelido
#Um pouco mais trabalhosa mas preferível pois documenta melhor e evita colisão de nomes
import  pacote_utilitario.matematica.aritmetica as arit
print arit.soma(10,20)
print arit.divisao(5,10.)
```

::: :pushpin: Importante :::

>Prefira sempre a forma 3 para  acesso a funcoes de seus módulos por questões de clareza e legibilidade do seu código 

### Para que serve o comando dir()

Quando usamos pacotes pode ser necessário saber quais os subpacotes, módulos e funções estão disponíveis. Para isso deve-se criar no arquivo `__init__.py` de cada pacote ou módulo, uma variável denominada `__all__` que é uma lista de todos os subpacotes ou módulos que pertencem àquele pacote.

Essa variável é usada pelo comando dir() para mostrar o diretório de subpacotes e módulos de um determinado pacote. É responsabilidade do desenvolvedor atualizar essa variável sempre que fizer alterações nos subpacotes ou módulos. 

```python
#Exemplo da variável __all__ no arquivo __init__.py do pacote_utilitario
__all__ = ['contabil', 'estatistica','financeira','matematica']

```

```python
#Exemplo da variável __all__ no arquivo __init__.py do subpacote matematica
__all__ = ['algebra', 'aritmetica','diferencial','integral']

````


::: :pushpin: Importante :::

As alterações realizadas nos subpacotes ou módulos só ficam visiveis após compilação. Para ter acesso às alterações em pacotes e módulos é necessário recompilar, criando um novo arquivo com extensão `pyc`.

Este é o fim deste curso de Python-Essencial. Para voltar ao início [Clique Aqui](README.md). Até o próximo curso!

