# Lógica aplicada com JavaScript - Gama Experience 
______________________________________________________


## JavaScript Avançado
______________________________________________________

* Template string
* Operador ternário
* Arrow functions
* Arrays, Operador spread e métodos de iteração
* Objetos e Destructuring
* SPA, PWA e WebComponenetes
* Projetinho
  
______________________________________________________
## Como rodar javascript fora do navegador
______________________________________________________

* Hello Word no terminal do vs code
* 3 formas de rodar um arquivo .js com node (direto no terminal, 
  run em um arquivo e extensão code runner.)

________________________________________________________

## Ferramenta extra: Readline-sync
# __________________________________________________________

* Readline-sync é um pacote maravilhoso para pegar inputs no terminal, 
  ou seja pegar entradas de dados no sistema. Se você veio de programação 
  front-end isso equivale a pegar o value do input de um usuário num formulário.

* Dentro da pasta de seu projetinho instale digitando o comando no terminal: 
  npm install readline-sync 
___________________________________________________________________________________
# 1. Template String
______________________________________________________________________________________
## Conceito

O ES6 trouxe uma nova forma de unir strings com expressões javascript, o Template 
String ou Template Literals.

Com ele podemos criar cadeias de caracteres, utilizando outra forma de interpolação 
que não seja o sinal de +. Em vez de aspas utilizamos crases e em vez do operador de 
soma interpolamos a expressão javascript utilizando ${}.


"Simara";
"Gama Academy";
let role = "transformadora"

console.log(`Simara é ${role} na Gama Academy`) // Simara é transformadora na Gama Academy.
______________________________________________________________________________________________
# 2. Operador ternário
________________________________________________________________________________________________
## Conceito

Você pode usar o operador ternário do JavaScript para tornar o seu código mais resumido.
Ele é uma alternativa ao if...else, entenda:

let x = 8

em vez de: 

if(x % 2 === 0) {
    return 'Par'
} else {
    retunr 'Impar'
}

use: 
x % 2 === 0 ? 'Par' : 'Impar'

Resumindo: teste ? verdadeiro : falso

O operando teste é uma expressão que é avaliada como um valor booleano true ou false. 
Se a condição for verdadeira, o operador ternário retornará o operando verdadeiro, 
caso contrário, retornará o falso.

Os operandos verdadeiro e falso são expressões de qualquer tipo.

# 3. Arrow functions
__________________________________________________________________________________

## Conceito
O ES6 também trouxe uma forma menos verbosa de escrever funções. São as famosas 
Arrow Functions, por causa da sintaxe que lembra uma flecha: () =>.

Entenda:
em vez de: 
function soma(a,b) {
    return a + b
}

use: 
const soma = (a,b) => a + b

Arrow functions são excelentes para trabalharmos com funções anônimas e callbacks 
(são funções passadas como argumentos dentro de outras funções a fim de serem utilizadas 
em um momento posterior).

# 4. Arrays, Operador spread e métodos de iteração
_________________________________________________________________________________________________
## Conceito

Um array (ou lista) permite armazenar um conjunto de dados e atribuí-los a uma variável, 
sendo esta a estrutura de dados mais simples possível.

## Inicializando Arrays
Para criar um novo Array, podemos atribuir a uma variável uma lista de elementos entre colchetes
e separados por vírgula. Também é possível utilizando a palavra reservada new e instanciando os 
valores que queremos atribuir ou apenas especificando o seu tamanho.

const alunasGama = ['Paula', 'Estela', 'Mariana'];

## Acessando valores

Para acessar o valor de um Array, use a notação de colchetes e informe a posição que deseja acessar,
lembrando que a contagem começa em zero.

const alunasGama = ['Paula', 'Estela', 'Mariana'];

console.log(alunasGama[0]) // Paula
console.log(alunasGama[1]) // Estela
console.log(alunasGama[2]) // Mariana

# Spread Operator

## Conceito

Ele é representado por três pontos. Spread significa espalhar, ou seja, este operador é usado para 
‘espalhar’ os elementos de um array quando interpretado em tempo de execução.

Ou seja, esses 3 pontinhos serve para copiarmos arrays.

let numeros = [0, 1, 2];
let novoNumero = 12;
numberStore = [...numeros, novoNumero];


Você pode também transformar uma string em array utilizando o spread:

var string = "hello";
var array = [...string];
console.log(array); // ['h', 'e',' l',' l', 'o']

## Métodos de iteração  
* filter retorna um novo array com os elementos filtrados.
* find retorna o primeiro elemento que achar igual ao elemento passado por parâmetro.
* map retorna um novo array sem alterar o array original, criando uma cópia com as alterações que desejamos.
* sort ordena o array.
* reduce reduz o array para um único valor mediante a uma operação matemática.
* Existem muitos outros métodos, continue seu aprendizado!

# 5. Objetos e Destructuring
___________________________________________________________________________________________________
## Conceito

Objeto é um tipo de dado que contém uma coleção de propriedades organizadas em pares de chave 
(ou nome) e valor, sendo o valor qualquer tipo de dado (número, texto, função ou até mesmo outro objeto).

## Inicializando objetos
Para criar um novo Objeto, podemos atribuir a uma variável uma lista de elementos entre chaves, 
separados por vírgula e com a notação de chave : valor. Também é possível utilizando a palavra reservada
new ou a partir de uma função.

const pessoa = {
  nome: 'Ariel',
  idade: 25,
  profissao: 'desenvolvedora',
};

## Acessando valores
### Notação de ponto

console.log(pessoa.nome); // Ariel
console.log(pessoa.idade); // 25
console.log(pessoa.profissao); // desenvolvedora

### Notação de colchetes (ou índice)

console.log(pessoa['nome']); // Ariel
console.log(pessoa['idade']); // 25
console.log(pessoa['profissao']); // desenvolvedora

## Atribuição via desestruturação

const pokemon = {
  nome: 'Pikachu',
  tipo: 'elétrico',
  altura: 40.6
}

const { nome, tipo, altura } = pokemon

console.log(nome) // Pikachu
console.log(tipo) // elétrico
console.log(altura) // 40.6

MDN: destructuring assignment

# 6. SPA, PWA e WebComponents
__________________________________________________________________________________________
Agora, vamos falar de SPA, PWA e Webcomponents que são alguns conceitos da programação web atual. 
Dessa vez não colocaremos a mão no código, nessa aula diferente apenas com conceitos, vamos falar 
muito sobre mudar a nossa forma de pensar aplicações web.

## 6.1 SPA

Single page applications são aplicações que concentram seu conteúdo em apenas uma página. O que isso quer dizer? Ela possui o super poder de atualizar apenas uma parte da página para renderizar novos dados, em vez de atualizar a página inteira.

O que usar para construir Single Page Applications? No mercado diversas ferramentas como frameworks e bibliotecas facilitam a criação de SPA. Alguns dos mais conhecidos são: Angular, React e Vue. Eles são baseados em JavaScript e trabalham com o conceito de componentes.

## 6.2 PWA

Progressive Web Apps são aplicações híbridas entre web e mobile. Ou seja, permite que ao acessar um site, a pessoa usuária possa ter uma versão instalada em seu celular com a mesma experiência da web, porém com as informações do browser removidas.

PWA são diferentes de aplicativos nativos, pois eles não podem ser encontrados nas lojas de aplicativos. E geralmente, são construídos com poucas alterações no código original: html, css e javascript.

Mas por outro lado, dá pr acessar de offline e ainda usar algumas caracteristicas como por exemplo o push notification.

Dá pra construir PWA com Angular, React, Vue, Ionic entre outros.

## 6.3 WebComponents

Os Web Components são uma forma de criar componentes reutilizáveis para a Web nativamente, utilizando apenas HTML, CSS e JavaScript. E carregam os benefícios de códigos menores, modulares e reutilizáveis.

Os Web Components possuem quatro fundamentos:

* Custom Elements: Permite a criação de novas tags HTML.
* Shadow DOM: Permite esconder elementos do DOM. Eles são renderizados pelo navegador e não são acessíveis pelas formas convencionais (document.querySelector).
* HTML Templates: Permite declarar fragmentos de HTML para serem utilizados como modelo. Eles não são renderizados pelo navegador.
* HTML Imports: Permite importar páginas HTML completas, incluindo o JavaScript e CSS embutidos nelas.

# Você pode usar o stencilJS que faz parte do Ionic Framework.