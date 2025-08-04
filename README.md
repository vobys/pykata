# Instruções

* Abaixo estão listados quatro exercícios.
* Você deve utilizar a linguagem `Java` e criar um projeto **MAVEN** contendo um utilitário para cada exercício resolvido.
* Você pode fazer testes unitários (ou não).
* Você pode utilizar a IDE de sua preferência (ou não).
* Empacote o código contendo a solução dos exercícios em um arquivo `zip` ou `tar.gz` (lembre-se de não compactar o que está compilado, pasta `target`, arquivos `.class` e etc).
* Envie a solução compactada por e-mail em anexo ou envie um link do dropbox, drive ou etc.


## Exercício 1

Escreva a função:

```java
// Utilitário TripleTroubleUtil
static int tripleDouble(long num1, long num2)
```

que recebe dois números `num1` e `num2`e retorne `1` se existir uma sequência de três dígitos iguais em qualquer posição no `num1` e também  uma sequência de dois desses mesmos dígitos no `num2` em qualquer posição. Caso contrário a função deverá retornar `0`.

Por exemplo:
```java
tripleDouble(451999277, 41177722899) == 1 // num1 tem uma sequencia de três 9s (999)
                                          // num2 tem uma sequencia de dois 9s (99)

tripleDouble(1222345, 12345) == 0 // num1 tem uma sequencia de três 2s (222) porém num2 tem apenas um único dígito 2

tripleDouble(12345, 12345) == 0

tripleDouble(666789, 12345667) == 1
```

## Exercício 2

Escreva a função:

```java
// Utilitário FindOutlierUtil
static int find(int[] integers)
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
// Utilitário FactorialUtil
static int zeros(int n)
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

Escreva a função:

```java
// Utilitário WorkingDaysUtil
static long count(final LocalDate start, final LocalDate end)
```

que recebe duas datas, sendo uma inicial e outra final posterior a primeira. As duas juntas representam o período de execução de um projeto.
O retorno da função deve ser a quantidade de dias úteis disponíveis para a execução do projeto, mas respeitando as seguintes regras:
- Dias úteis são os dias de segunda-feira a sexta-feira.
- Dias não-úteis são o sábaso e o domingo. Não haverá feriados.
- Ignore os dias informados nas datas. Apenas serão usados no cálculo o mês e ano informados.
- O projeto iniciará sempre na primeira segunda-feira do mês inicial.
- E deve ser finalizado na última sexta-feira do mês final.
- Assim, se a data inicial e final forem no mesmo mês, então o projeto será executado ao longo daquele mês.


Por exemplo:

**Sem exemplos desta vez.**
