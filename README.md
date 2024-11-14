# RESOLUÇÃO EXERCÍCIO 03

1. Crie uma função que recebe como parâmetro um número e retorna true se o número for par e false se for ímpar.
   
``` typescript
function par(numero: number): boolean {
    return numero % 2 === 0;
}

const resultado: boolean = par(4)
console.log(`O número é par:`, resultado)
```

2. Crie uma função que receba como parâmetros um nome e um pronome de tratamento opcional. Caso esse último não seja fornecido, deve ser considerado o valor “Sr”. Ao final, imprima uma saudação semelhante a “Sra. Sávia”.

``` typescript
function saudacao(nome: string, tratamento: string = "Sr") {
    console.log(`Bem vindo(a) ${tratamento}. ${nome}`);
}

saudacao("Arabela", "Sra");
saudacao("Márcio");
saudacao("Catarina", "Sra");
```

3. Crie uma função que retorne os números de um array passados por parâmetro separados por traço (-) no formato string. Para isso, use o método forEach dos arrays.

``` typescript
function formatarNumero(lista: number[]): string {
    let resultado: string[] = [];

    lista.forEach((numero) => {
        resultado.push(numero.toString());
    });
    return resultado.join("-");
}

const numeros = [3, 6, 9, 12, 15, 18]
console.log(formatarNumero(numeros));
```

4. Dada a função soma abaixo, tente executar os scripts das alternativas e exiba os eventuais resultados: 
``` typescript
function soma(x: number, y?: any): number { 
return x + y 
}
```
a. console.log(soma(1, 2)); 

R= 3


b. console.log(soma(1, "2")); 

R= 12

c. console.log(soma(1));

R= Nan

5. Crie uma função exibir receba como parâmetro um “rest parameter” representando strings. A função deve exibir no log cada um dos elementos do “rest parameter”. Chame a função usando diferentes quantidade de parâmetros conforme abaixo:

exibir(“a”, “b”); 

exibir(“a”, “b”, “c”); 

exibir(“a”, “b”, “c”, “d”);

``` typescript
function exibir(...elemento: string[]): any {
    elemento.forEach(elemento => console.log(elemento));
}

exibir('a', 'b');
exibir('a', 'b', 'c');
exibir('a', 'b', 'c', 'd');
```

6. Converta em arrow function a seguinte função: 
``` typescript
function ola(): void { 
console.log("Olá"); 
}
```
R= 
``` typescript
const ola = (): void => {
    console.log("Olá");
}

ola();
```

7. Dado método filter dos arrays, crie uma implementação usando arrow function que filtre todos os elementos pares do array abaixo:

const array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15];

R= 

``` typescript
const array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15];
const num_pares = array.filter (array => array % 2 === 0);

console.log(num_pares);
```
8. Crie um exemplo usando a função map para dobrar os elementos de um array e reduce para totalizar a soma dos elementos do array.
``` typescript
const numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const dobrar = numeros.map (num => num * 2);
console.log(dobrar);

const somar = dobrar.reduce ((soma, valor) => soma + valor, 0);
console.log(somar);
```
