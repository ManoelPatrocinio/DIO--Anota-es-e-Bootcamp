
## Spread Operator

https://www.devmedia.com.br/javascript-operadores-rest-e-spread/41200 

O operador Spread é um recurso que permite acessar o conteúdo de um objeto iterável. Objeto iterável é um objeto, ou estrutura de dados, que permite acessar seu conteúdo com for … of loop. O exemplo mais popular de um iterável é um array. Outro exemplo de iterável pode ser objetos literais ou strings 

## Destricturing Assignment

é uma expressão JavaScript que possibilita extrair dados de arrays ou objetos em variáveis distintas.

ex: var foo = ["one", "two", "three"];

    var [one, two, three] = foo;


## Symbols e iterators
    
Symbols: é uma maneira de gerar um indentificos único

    const uniqueId = Simbol();

seu valor não é um number ou text.
    const uniqueId = Simbol('user'); : pode passar um valor,mas serve apenas como identificado ou debug

A única utilização sensata para para essa construção é armazená-la em uma variável que será utilizada como chave para uma propriedade de objeto cujo objetivo é torná-lo anônimo.

Iterators : os iterables permitem que você define como um objeto vai se comportar quando eles são iterados

    var myIterable = {}
myIterable[Symbol.iterator] = function* () {
    yield 1;
    yield 2;
    yield 3;
};
[...myIterable] // [1, 2, 3]


## Generators
https://medium.com/nossa-coletividad/es6-generators-est%C3%A3o-mudando-nosso-modo-de-escrever-javascript-e99f7c79bdd7

Generators são funções especiais que podem ser executadas, pausadas e continuadas em diferentes estágios da sua execução, tudo isso graças a nova palavra reservada yield.

function* myGenerator() {
  yield ‘first’;
  let input = yield ‘second’;
  yield input;
}

Para instanciar o objeto do generator:
    let gen = myGenerator();

Executando o generator pela primeira vez:
    console.log(gen.next());
// { value: ‘first’, done: false }

## Fetch
https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API/Using_Fetch

https://developer.mozilla.org/en-US/docs/Web/API/fetch

## Async / Await

Uma forma mais simple de lidar com promese, só de por Async antes do nome da função, já a torna uma promese

então usa-se o await para aguada que uma 

## Qualidade de software e teste em js

### Testes unitários
servem para testar a menor parte do codigo, como componentes,funções e metodos
### Tests integrados

testa a integração entres a menores partes testadas anteriormente

### Testes funcionais 

Também conhecido como teste end-to-end, testa a integra do sistema com outro sistema, testando suas funcionalidade de ponto a ponto. Também é posssivel usar a abordagem black-box

TDD (test Drive Development)
É um dos pilares do exteme programming, consiste em testar e refatorar em pequenos ciclos, onde voçê escreve o teste antes do codigo, faz o mesmo passar e refatora o código.

ciclo: escrita do teste -> escrita do codigo -> refatoração
#### vantagens
 * feedback rápido
 * maior segurança em alterações e novas funcionalidades
 * codigo mais limpo
 * produtividade

### BDD (Behavior driver development)

Tecnica de desenvolvimento agil que busca integra regras de negocio com linguagens de programação

 * testes;
 * documentação
 * exemplos

#### Vantagens
 * compartilhamento de conhecimento
 * ducumentação dinâmica 
 * visão de tudo

### Mocha, chai e sinon

#### Mocha 

é uma ferramenta para executar seus teste.

## Tatramento e exceções

o forma tradicional de tratamento é usando um TRY CATCH.

`
        try{
            console.log(name)
            const name = "manoel"
        }catch(err){
            console.log("error", err)
        }

`
caso queira que uma parte do codigo execute msm com ou sem error, usasse o finally:
`
        try{
            console.log(name)
            const name = "manoel"
        }catch(err){
            console.log("error", err)
        }finally{
            console.log("keep going")        
        }

`

Em js Error é uma classe, logo pode ser usada como uma.


OBS: pesquisa as demais funções do console

