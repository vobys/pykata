# Instruções

* Abaixo estão listados quatro exercícios. Escolha pelo menos 2 desses exercícios para serem resolvidos.
* Você pode utilizar a linguagem `Java` ou `Python`, a que se sentir mais confortável.
* Você pode fazer testes unitários (ou não).
* Você pode utilizar a IDE de sua preferência (ou não).
* Empacote o código contendo a solução dos exercícios em um arquivo `zip` ou `tar.gz` (lembre-se de não compactar o que está compilado, pasta `target`, arquivos `.class`, `.exe` e etc).
* Envie a solução compactada por e-mail em anexo ou envie um link do dropbox, drive ou etc.


## Exercício 1

Escreva a função:

```java
int TriploEDobro(long num1, long num2)
```

que recebe dois números `num1` e `num2`e retorne `1` se existir uma sequência de três dígitos iguais em qualquer posição no `num1` e também  uma sequência de dois desses mesmos dígitos no `num2` em qualquer posição. Caso contrário a função deverá retornar `0`.

Por exemplo:
```java
TriploEDobro(451999277, 41177722899) == 1 // num1 tem uma sequencia de três 9s (999)
                                          // num2 tem uma sequencia de dois 9s (99)

TriploEDobro(1222345, 12345) == 0 // num1 tem uma sequencia de três 2s (222) porém num2 tem apenas um único dígito 2

TriploEDobro(12345, 12345) == 0

TriploEDobro(666789, 12345667) == 1
```

## Exercício 2

Escreva a função:

```java
int intruso(int[] nums)
```

que recebe um array (que terá um tamanho mínimo de 3, mas pode ser bem maior) contendo números inteiros. O array será composto por interamente por números pares ou inteiramente por números impares, exceto por um único elemento. Escreva um método que receberá esse array e retorne apenas esse elemento fora do padrão.

Por exemplo:

```[2, 4, 0, 100, 4, 11, 2602, 36]```

Deve retornar: 11 (o único elemento ímpar)

```[160, 3, 1719, 19, 11, 13, -21]```

Deve retornar: 160 (o único elemento par)

## Exercício 3

Escreva a função:

```java
int zeros(int num)
```

que recebe um número inteiro e calcula a quantidade de zeros a direita no resultado do fatorial do número. Tente elaborar uma solução que rode no menor tempo possível.

```N! = 1 * 2 * 3 * ... * N```

Cuidado, 1000! tem 2568 digitos...

Por exemplo:

```java
zeros(6) = 1
// 6! = 1 * 2 * 3 * 4 * 5 * 6 = 720 --> 1 zero à direita
```

```java
zeros(12) = 2
// 12! = 479001600 --> 2 zeros a direita
```

Dica: Não é necessário calcular o fatorial, pense em uma forma diferente de calcular o número de zeros a direita do resultado.

## Exercício 4

Você foi designado para uma força-tarefa com o objetivo de desenvolver uma nova geração de unidades de disco rígido. Um dos principais componentes nos quais você trabalhará é responsável por armazenar os dados na unidade.

Precisamos de uma função que possa determinar se um dado arquivo pode ser armazenado em um bloco do disco. Para que isso seja possível deve haver pelo menos um número de setores livres e contíguos em um determinado bloco igual ao tamanho do arquivo.

Você receberá como parâmetro um `Set<Integer> occupiedSectors` em que cada elemento é um setor entre 1 e `blockSize` que representam os setores já ocupados naquele bloco. Outros setores estão livres para escrita caso contrário.

Retorne um _booleano_ informando se é possível armazenar o arquivo no bloco especificado.

Embora seja uma fase inicial de desenvolvimento experimental, lembre-se de que é indesejável ter o desempenho do disco degradado pela execução muito lenta do método `isWritable`.

Escreva a função:

```java
boolean isWritable(int blockSize, int fileSize, Set<Integer> occupiedSectors)
```

Restrições:

* `blockSize` estará entre 1 e 1.000.000, inclusive.
* `fileSize` estará entre 1 e `blockSize`, inclusive.
* `occupiedSectors` estará entre 1 e 100.000 elementos, inclusive.
* Cada elemento de `occupiedSectors` estará entre 1 e `blockSize`, inclusive.
* Elementos de `occupiedSectors` serão distintos.
* Tempo de execução esperada abaixo de 10 segundos.

Por exemplo:

* `isWritable(1, 1, [])` deverá retornar `true` já que existe exatamente 1 setor livre, o suficiente para armazenar o arquivo de tamanho 1.
* `isWritable(1, 1, [1])` deverá retornar `false` já que não há espaço suficiente no bloco.
* `isWritable(4, 2, [1, 4])` deverá retornar `true` já que o arquivo de tamanho 2 pode ser armazenado nos setores 2 e 3.
