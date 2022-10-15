
# Rescript - Características

### Algumas características

1. Criado com a linguagem OCaml. Que é funcional e OO. 
Com foco em "Segurança, legibilidade, expressividade e desempenho"

2. Cada arquivo do projeto é um "módulo". Sem a confusão de import e export.
```js
// Arquivo: "math.re"
module Operations = {
  module Basic = {
   let add = (a, b) => a + b;
  }
}
```
Como usar um módulo? 
Basta usar o nome do arquivo
```js
// Arquivo: "file.re"
Math.Operations.Basic.add(1, 2)
```
3. Tipagem estática e por inferência do compilador. 
Mais seguro e melhor do que precisar tipar tudo como TypeScript.

4. Compila muitas vezes mais rápido que TypeScript.

5. Sem const, sem var. Só existe let imutável. 
```js
let hello = "hello"
```
6. Sem undefined. Sem null.

7. Sem "return" no final da função. 

8. Sem "function name(arg)". Apenas:
```ocaml
let make = (a, b) => a + b  
```
9. JSX nativo no compilador. Não precisa plugin/Babel.
```ocaml
<Comp message />
```
10. Loop "for" simplificado.
```ocaml
for x in 1 to 3 { Js.log(x) }
```
11. Criar novo tipos sem burocracia. 
```ocaml
type coord3d = (float, float, float)
type coordinates = {x: float, y: float}
```
12. Tuplas. 
```ocaml
let ageAndName: (int, string) = (24, "ReScript")
```
13. Expressões regulares. 
```ocaml
let r = %re("/b/g")
```
14. Currying. 
```ocaml
external a: x => y => z = "fn"
external b: (x => y) => z = "fn"
a == b
```
15. Pattern Matching
```ocaml
let animal = Human(string) | Cat | Dog | Fish
```
16. Pipe
```cs
// Confuso
validateAge(getAge(parseData(person)));

// Semântico
person
  ->parseData
  ->getAge
  ->validateAge
```
Etc, etc, etc

### Referências
https://rescript-lang.org/
