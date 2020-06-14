# Aula 10

## Funções

### Dividir para conquistar! 
Esse conceito foi utilizado pelo governante romano César (divide et impera). Em TI usamos essa regra para 'quebrar' um problema maior em pedaços menores e, resolvendo as partes,   juntá-las formando o todo novamente.

Esse conceito também encontra amparo na proposição do cientista canadense Craig Larman   que no seu livro  "Utilizando UML e Padrões" elenca 9 padrões que contribuem para a melhoria da qualidade de software, denominando-os de padrões GRASP. Um desses padrões  é o "Especialista na informação" (information expert). O padrão Especialista é usado  para atribuir responsabilidades ao especialista da informação. Isso significa que: é preciso delegar (atribuir responsabilidade) mas não a qualquer um e sim a um especialista. 

Dito isto nós podemos dizer que as funções são blocos de código especialistas em realizar determinadas operações (funções) para as quais devemos delegar responsabilidades com o objetivo de dividir para conquistar.

As funções são identificados por um nome, podem receber parâmetros pré-determinados e podem ou não retornar um valor.

No Python, as funções: 
- Podem retornar objetos, um ou mais valores, ou simplesmente, não retornar nada.
- Aceitam parâmetros opcionais (defaults). Se não for passado, o parâmetro será
igual ao valor default, definido na função.
- Aceitam que os parâmetros sejam passados com nome. Neste caso,a ordem em que
os parâmetros foram passados não importa.
- Tem escopo local, ou seja não afetam definições de
escopo global.
- São recursivas, ou seja, uma função pode invocar ela mesma



