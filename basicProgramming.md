# Programação básica

Bom dia!

Neste capítulo vou apresentar alguns conceitos básicos de programação, para eles, eu recomendo que você use o [codepen](https://codepen.io/pen/), ele é um site que você poder escrever códigos em HTML, CSS e Javascript, e ver o resultado em tempo real.

## Hello World

Uma tradição muito comum de programação é ter com primeiro exercício é escrever `Hello World`. No Javascript isso pode ser feito de duas formas:

```javascript
window.alert("Hello World");
```

ou

```javascript
console.log("Hello World");
```

### Qual é a diferença?

A primeira forma é usar o `alert`, que é uma função que mostra uma mensagem na tela, e a segunda é usar o `console.log`, que mostra a mensagem no console do navegador, que pode ser acessado através do menu `F12` ou `Ctrl + Shift + I`. O console é uma ferramenta muito útil que ainda vamos explorar mais a frente.

### Exercício

1. Escreva um código que mostre a mensagem `Hello World` na tela.
2. Escreva um código que mostre a mensagem `Hello World` no console do navegador.
3. Escreva um código que mostre o seu nome na tela.

## Variáveis

Uma variável é um espaço reservado para armazenar um valor, e é usado para manipular o valor armazenado. No Javascript, variáveis são declaradas usando uma de duas palavras chave, `let` para variáveis que mudam e `const` para variáveis que não mudam (constantes).

```javascript
let myVariable = "Hello World";
const myConstant = "Hello World";
```

Variáveis são uma parte essencial de programação, e são necessárias para realizar operações mais complexas. Elas

### Tipos de dados simples

Em programação e em JavaScript, variáveis podem armazenar valores de diferentes tipos de dados. Os tipos de dados mais básicos são:

- String
  - Um conjunto de caracteres entre aspas simples ou duplas. Usado para armazenar texto.
- Number
  - Um número inteiro ou decimal. (Em JS números sempre são decimais, isso tem alguns efeitos colaterais interessantes)
- Boolean
  - Um valor de verdadeiro ou falso.
- Null
  - Um valor especial que representa a ausência de valor.
- Undefined
  - Um valor especial que representa um valor que ainda não foi definido.

No Javascript, variáveis podem ser de qualquer tipo de dado, porém isso é considerado uma má prática, já que isso deixa o código mais difícil de ser entendido e mantido.

## Operações básicas

Uma das coisas mais básicas que você pode fazer em qualquer linguagem de programação é realizar diversas operações matemáticas e de manipulação de dados. Elas são:

- Adição
  - `a + b`
- Subtração
  - `a - b`
- Multiplicação
  - `a * b`
- Divisão
  - `a / b`
- Módulo (é o resto de uma divisão)
  - `a % b`

Claro, os operadores seguem a ordem de operações normal, mas podemos usar parêntesis `(` e `)` para mudar essa ordem, assim como na matemática.


Além dos operadores matemáticos básicos, temos operadores lógicos, eles são:

- E (só é verdadeiro se ambos os lados forem verdadeiros)
  - `a && b`
- OU (só é verdadeiro se pelo menos um dos lados for verdadeiro)
  - `a || b`
- NÃO (só é verdadeiro se o lado direito for falso)
  - `!a`
- Igualdade (só é verdadeiro se os valores forem iguais)
  - `a === b`
- Diferença (só é verdadeiro se os valores forem diferentes)
  - `a !== b`
- Menor que (só é verdadeiro se o valor esquerdo for menor que o valor direito)
  - `a < b`
- Maior que (só é verdadeiro se o valor esquerdo for maior que o valor direito)
  - `a > b`
- Menor ou igual a (só é verdadeiro se o valor esquerdo for menor ou igual a o valor direito)
  - `a <= b`
- Maior ou igual a (só é verdadeiro se o valor esquerdo for maior ou igual a o valor direito)
  - `a >= b`

Mas de que servem esses operadores se não podemos guardar eles em variáveis? Para isso, nós usamos o operador `=` para atribuir um valor a uma variável.

```javascript
let a = 5;
let b = 10;

a = a + b; // 15
window.alert(a); // 15
```

### Exercício

1. Escreva um programa que mostre na tela a resposta de `x + y * 2 - 1`, escolha os valores de `x` e `y`.

## Condicionais

Condicionais são uma forma de controlar o fluxo de um programa, e são usadas para verificar se um determinado valor é verdadeiro ou falso, e então executar um código diferente dependendo disso.

```javascript
if (condição) {
  // código a ser executado se a condição for verdadeira
} else {
  // código a ser executado se a condição for falsa
}
```

### Exercício

1. Escreva um programa que receba um número x, e mostre na tela se o número é par ou ímpar.
Ex:
```javascript
let x = 0; // valor a ser testado

if (condicao 1) {
  window.alert("O número é par");
} else if (condicão 2) { // só chega aqui se condição 1 não for verdadeira
} else {
  window.alert("O número é ímpar");
}
```

## Loops

Loops são uma forma de repetir um código até que uma condição seja verdadeira. Eles são essenciais para não termos que repetir o mesmo código várias vezes.

### While

O loop `while` é usado para repetir um código até que uma condição seja verdadeira, e é composto por três partes:

- A declaração `while`
- A expressão de condição
- O bloco de código a ser executado

```javascript
while (condição) {
  // código a ser executado
}
```

Exemplo:

```javascript
let x = 0; // valor inicial

while (x < 10) { // roda até x ser menor ou igual a 10
  x++; // aumenta o valor de x em 1
  window.alert(x);
}
```

### For

O loop `for` é usado para repetir um código uma determinada quantidade de vezes, e é composto por três partes:

- A declaração `for`
- A expressão de condição
- O bloco de código a ser executado

```javascript
for (inicialização; condição; incremento) {
  // código a ser executado
}
```

Exemplo:

```javascript
for (let x = 0; x < 10; x++) { // roda 10 vezes
  window.alert(x);
}
```

### Exercício

1. Escreva um programa que imprima `foo` se o número for divisível por 3, e `bar` se não for, para todos os números de 0 a 100. (recomendo usar o console.log para mostrar o resultado)

2. Atualize o programa anterior para que ele imprima `foo` se o número for divisível por 3 e `bar` se for divisível por 5, e o número em si, se não for divisível por 3 nem por 5.

## Funções

Funções são uma forma de reutilizar código, e são usadas para criar pequenas partes de código que podem ser chamadas várias vezes, e que podem receber parâmetros.

```javascript
function nomeDaFuncao(parâmetro1, parâmetro2) {
  // código a ser executado
}
```

Mas o que são esses parâmetros? São variáveis que recebem um valor quando a função é chamada, e podem ser usadas dentro do código da função. Um exemplo pode ser uma função de soma:

```javascript
function soma(a, b) {
  return a + b;
}
```

A palavra-chave `return` é usada para retornar um valor, quando usamos ela, esse valor é automaticamente passado para a função que chamou a função. E como se chama uma função?

```javascript
let resultado = soma(5, 10);
```

Aqui podemos ver que não precisamos saber o que tem dentro da função `soma`, apenas chamá-la e passamos os parâmetros `5` e `10` para ela, e ela retorna o valor correto, `15`.

### Exercício

1. Escreva uma função que receba um ano e retorna `true` se o ano for um ano bissexto, e `false` caso contrário. ([regras para ano bissexto](https://pt.wikipedia.org/wiki/Ano_bissexto#Calend%C3%A1rio_Gregoriano))

## Estruturas de dados mais complexas

Esses tipos de variáveis que você viu já são muito úteis, mas quando estamos lidando com mais informações, fica muito difícil ter uma variável para cada informação. Por isso, temos estruturas de dados que tem várias informações dentro delas, por exemplo:

### Listas

Listas são estruturas de dados que guardam várias informações em uma ordem específica. No Javascript, elas são representadas por colchetes `[]`.

```javascript
let lista = [1, 2, 3, 4, 5];
```

Eles são muito úteis para guardar grupos de informações, por exemplo:

- Frutas
  - `["Banana", "Maçã", "Laranja", "Limão"]`
- Idades
  - `[18, 21, 50, 13]`
- Nomes
  - `["Bob", "Joe", "Jane", "Alice"]`

#### Operações com listas

- Acessando elementos
  - Para acessar um elemento de uma lista, usamos o índice do elemento, e o índice começa em 0, então o primeiro elemento é o elemento no índice 0.
  ```javascript
  let lista = [1, 2, 3, 4, 5];

  console.log(lista[0]); // 1
  console.log(lista[1]); // 2
  console.log(lista[2]); // 3
  ```
- Adicionando elementos
  - Para adicionar um elemento a uma lista, usamos o método `push`.
  ```javascript
  let lista = [1, 2, 3, 4, 5];

  lista.push(0); // adiciona 6 no final da lista
  console.log(lista); // [1, 2, 3, 4, 5, 0]
  ```
- Removendo elementos
  - Para remover o último elemento de uma lista, usamos o método `pop`.
  ```javascript
  let lista = [1, 2, 3, 4, 5];

  lista.pop(); // remove o último elemento da lista
  console.log(lista); // [1, 2, 3, 4]
  ```
- Ordenando elementos
  - Para ordenar uma lista, usamos o método `sort`.
  ```javascript
  let lista = [5, 3, 1, 4, 2];

  lista.sort(); // ordena a lista
  console.log(lista); // [1, 2, 3, 4, 5]
  ```

### Objetos

Objetos são estruturas de dados que guardam várias informações que cada uma tem um nome, isso é muito útil para guardar informações complexas, como:

- Pessoas
  - `{ nome: "Bob", idade: 21, sexo: "M" }`
- Produtos
  - `{ nome: "Notebook", preco: 1000, cor: "Azul" }`

#### Operações com objetos

- Acessando propriedades
  - Para acessar uma propriedade de um objeto, usamos o nome da propriedade.
  ```javascript
  let pessoa = { nome: "Bob", idade: 21, sexo: "M" };

  console.log(pessoa.nome); // Bob
  console.log(pessoa.idade); // 21
  console.log(pessoa.sexo); // M
  ```
- Alterando propriedades
  - Para alterar uma propriedade de um objeto, usamos o nome da propriedade seguido de `=`.
  ```javascript
  let pessoa = { nome: "Bob", idade: 21, sexo: "M" };

  pessoa.nome = "Joe"; // altera o nome da pessoa
  console.log(pessoa); // { nome: "Joe", idade: 21, sexo: "M" }
  ```

### Exercício

1. Escreva um programa que receba um array de números e mostre na tela a soma dos números.

2. Escreva um programa que receba um array de números e mostre na tela a soma dos números, mas somente para os números que são pares.

3. Escreva um programa que receba os dados a seguir e mostra na tela os nomes das pessoas que são maiores de 18 anos.

```javascript
let dados = [
  { nome: "Bob", idade: 21, sexo: "M" },
  { nome: "Joe", idade: 50, sexo: "M" },
  { nome: "Jane", idade: 18, sexo: "F" },
  { nome: "Alice", idade: 13, sexo: "F" },
];
```

## Conclusão

Esses são as principais partes de programação, ao longo da sua jornada você vai encontrar outros conceitos e técnicas, mas com isso você consegue começar a entender o funcionamento do programa e evoluir nas partes mais legais da programação.
