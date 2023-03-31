# data-structures
Códigos produzidos como monitor da disciplina de Estruturas de Dados e Algoritmos

Conteúdo:


## RECURSIVIDADE

- Lei 1: Um algoritmo recursivo deve ter um caso base (condição de parada).
- Lei 2: Um algoritmo recursivo deve mudar seu estado e se aproximar do previsto para o caso base.

- Recursão direta: a função some a si mesma
- Recursão indireta: chama outra que a chama

- Recursão em cauda: a chamada da recursividade é a última instrução
- Sem cauda: em qualquer lugar que não seja a última posição

Temos objetivos muito maiores por meio da recursão do que simplesmente definir funções em termos de si mesmas. Recursão está relacionada com o poder de computação. Permite definir coisas infinitas de forma finita.

É possível ter:
- Funções e algoritmos recursivos (template geral)
- Caso(s) base(s)  –  situações triviais (terminais)
- Caso indutivo/recursivo  –  dependem da aplicação da mesma função a casos mais simples.
- Tipos de dados recursivos
- Expr = Num |

### TIPOS DE RECURSÃO
- Simples e múltipla: a função é chamada apenas uma vez ou diversas vezes
- Indireta (ou mútua)
- Estrutural: definição feita em termos de si mesma

#### RECURSÃO vs ITERAÇÃO
- poder expressivo: possuem o mesmo poder e um pode ser convertido no outro
- performance: depende do compilador, mas a versão iterativa normalmente é mais eficiente


## ORDENAÇÃO POR COMPARAÇÃO
#### PROPRIEDADES IMPORTANTES:
- Algoritmo estável  –  preserva a ordem de elementos iguais.
- Algoritmo in-place  –  não faz uso de memória extra, o array de entrada é o mesmo de saída, sem utilização de auxiliares

#### BUBBLE SORT
- Varrer a entrada da esquerda para a direita, analisando os elementos adjacentes
- Cada iteração leva o maior elemento para a última posição

#### SELECTION SORT
- Baseado na seleção do maior e seu posicionamento no final ou seleção do menor e seu posicionamento na posição i.
- Primeiro, seleciona; depois, leva para a posição correta.
- Não-estável
- In-place
- Eficiência (pior caso) n²
- Nº de comparações: (n-1) + (n-2) + … + 1 + 0. PA decrescente finita
- Nº de trocas: n

#### INSERTION SORT
- Baseado na ideia de inserir um elemento em uma lista ordenada
- Começa do segundo item, considerando o primeiro como uma sublista ordenada
- Avalia cada item, colocando-o em sua posição ordenada na sublista
- Estável: preserva a ordem dos elementos iguais
- In-place: não utiliza outra estrutura de dados auxiliar
- Faz menos comparações  –  não precisa ir até o final do array
- Faz mais trocas

## ALGORITMOS DE DIVISÃO E CONQUISTA
Baseiam-se na ideia de dividir um problema global em problemas menores para obter ganhos em performance. Na fase da divisão, o problema é dividido em, no mínimo 2; na fase da conquista cada subproblema é separadamente resolvido de forma recursiva; por fim, chega-se na fase de combinação, em que as respostas dos subproblemas são convertidas na resposta global.

#### MERGE SORT
- Vai quebrando a lista em duas, de tamanhos aproximadamente iguais, até chegar numa lista trivial de tamanho 1.
- Feito isso, começa o processo de construir listas ordenadas por meio da união entre listas previamente ordenadas.

#### QUICK SORT
- Particiona o vetor de acordo com a escolha de um pivot
- Ordena recursivamente cada subvetor
