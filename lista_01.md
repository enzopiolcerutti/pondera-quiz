# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
**a) A saída será undefined seguido de erro**

**resposta: letra a, pois a variável x, declarada com var, é elevada ao topo do escopo, mas não é inicializada, já y é declarada com let, não é elevada, causando erro se acessada antes da inicialização.**

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log


**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

**a) Substituir if (a || b === 0) por if (a === 0 || b === 0)**

**resposta: letra a, pois a condição if (a || b === 0) está verificando se a é verdadeiro ou se b é igual a 0, 
e o correto é verificar se a é igual a 0 ou se b é igual a 0.**

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

**b) O código imprime 200.**

**resposta: letra b, pois ao não possuir break na case 'eletrônico', faz com que a execução do código continue retornando para a case 'vestuário'.**

c) O código imprime 50.

d) O código gera um erro.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

**d) 24**

**resposta: letra d, pois o código está multiplicando cada elemento do array por 2.**
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

**c) ["banana", "abacaxi", "manga", "laranja"]**

**resposta: letra c, pois o método splice remove 2 elementos a partir do índice 1 e adiciona "abacaxi" e "manga" no lugar dos elementos removidos.**

d) ["banana", "maçã", "uva", "abacaxi", "manga"]
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

**b)As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.**

**resposta: letra b, pois a segunda frase apenas explica como ela é implementada no código e não do porque dela funcionar.**

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

**a) I e II são verdadeiras.**

**resposta: letra a, pois a classe funcionario herda de pessoa e pode acessar os atributos nome e idade diretamente,
 e o método apresentar() da classe funcionario sobrepõe o método apresentar() da classe pessoa, mas chama o método da classe pai usando super.**

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

**b) A asserção é verdadeira e a razão é falsa.**

**resposta: letra b, pois em javascript não é possível sobrecarregar métodos em uma classe.**

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
``` 
``` javascript
// código corrigido:
function somaArray(numeros) {
    let soma = 0; // a variável soma deve ser inicializada antes do loop
    for (let i = 0; i < numeros.length; i++) { // o erro estava em numeros.size, que não existe, o correto é numeros.length
        soma += numeros[i]; // a variável soma deve ser incrementada com o valor do elemento do array multiplicado por 2
    }
    return soma * 2; // a soma final deve ser multiplicada por 2
}
console.log(somaArray([1, 2, 3, 4])); // 2x(1+2+3+4) = 20
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

``` javascript
// resposta da questão 10: 
class Produto { // classe produto com atributos nome e preco
    constructor(nome, preco) { 
        this.nome = nome; 
        this.preco = preco;
    }
    calcularDesconto() { // método calcularDesconto que aplica um desconto fixo de 10% no preço do produto
        return this.preco * 0.1; // retorna o valor do desconto
    }
}

class Livro extends Produto { // classe livro que herda de Produto
    constructor(nome, preco) {
        super(nome, preco); // chama o construtor da classe pai
    }
    calcularDesconto() { // método calcularDesconto que aplica um desconto de 20% no preço dos livros
        return this.preco * 0.2; // retorna o valor do desconto
    }
} 

let produto = new Produto('computador', 1500); // valor genérico para o produto
let livro = new Livro('o pequeno principe', 50); // valor genérico para o livro

console.log('Preço do produto: ' + produto.preco); // imprime o preço do produto
console.log('Preço do livro: ' + livro.preco); // imprime o preço do livro
console.log(`Desconto no produto: ${produto.calcularDesconto()}`); // imprime o desconto no produto
console.log(`Desconto no livro: ${livro.calcularDesconto()}`); // imprime o desconto no livro

/* comentários finais sobre a questão 10: 

- como funciona a herança nesse contexto: a classe livro herda os atributos e métodos da classe Produto, podendo acessá-los e modificá-los conforme necessário. */
```











