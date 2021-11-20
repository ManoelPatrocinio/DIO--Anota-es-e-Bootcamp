

## Currying
 é uma tecnica que transforma um função com n parametros em uma função que receber apenas um parametro e para cada param retorna uma nova função

## Hoisting
 compotamento em js que ocorre em declarações de variaveis e funções. onde a declarações de variaveis e funções são elevadas ao escopo onde ela estar.
    . hoisting de variaveis: só eleva a criação mas não sua atribuição
    . hoisting de função: eleva a função como um todo

## Imutabildade
Em linguagem funcional a variavel nunca muda, se precisar alterar-la crie uma nova, baseada na antiga, adicionando o novo elemento.
    ex: 
            ` function getUserWithFullname(user){
                return{
                    ...user,
                    fullName: `${user.name} ${user.lastName}`  
                }            
            }    
            `
## tipos de variaveis:
    O js possui 6 tipos primitivos:
    .string
    .number
    .boolean
    .null
    .undefined
    .symbol

    var: não respeita o escopo de bloco
    let :  respeita o escopo de bloco
    const:  respeita o escopo de bloco


A função do reducer é receber um objeto que representa o estado “anterior” da aplicação e baseado na ação que foi realizada (podendo enviar esse estado para uma função transformá-lo, etc), retornar um objeto completamente novo que tenha copiando todas as informações do estado anterior 

## Spread (...)
Spread significa espalhar, ou seja, este operador é usado para ‘espalhar’ os elementos de um array quando interpretado em tempo de execução. Neste último caso, os itens de middle foram espalhados dentro de arr

var middle = [3, 4];
var arr = [1, 2, ...middle, 5, 6];
console.log(arr);
// [1, 2, 3, 4, 5, 6]

## Design patterns
São soluções generalstas para problemas recorrentes durante o desenvolvimento de um software

Possuem 3 tipos:
    .criação 
    .estruturais 
    .comportamentais

## Manipulação e iteração de um Array

### Para criar

    const arr  = [1,2,3]
    const arr2 = new Array(1,2,3)
    const arr  = Array.of(1,2,3)
    const arr = Array.from() para NodeList por exemplo

### Inserir e Remover

.push : adiciona no final do array e retorna o tamanho do novo array
    ex: const arr  = [1,2,3]
        arr.push(1)  -> return 4

.pop : remove o ultimo elemento do array e retorna o elemento removido
    ex: const arr  = [1,2,3]
        arr.pop()  -> return 3

.unshift: adiciona um ou mais elementos no inicio do array e retona o tamanho do novo array.
    ex: const arr  = [1,2,3]
        arr.unshift(0)  -> return 4

.shift: remove o primero elemento do array e retorna o removido


.concat: junta dos arrays e retorna um novo
    ex: const alimentos = frutas.concat(verduras)

.slice: retorna um novo array dividindo de acordo com o inicio e fim.
    ex: const arr  = [1,2,3,4,5]
        arr.slice(0,2) -> [1,2]
        arr.slice(2)   -> [3,4,5]
        arr.slice(-3)  -> [3,4,5]

.splice: altera o array adicionando novos elementos enquanto remove os antigos

     ex: const arr  = [1,2,3,4,5]
        arr.splice(2) -> [1,2]  e remove 3,4,5
        arr.slice(apartir de onde remover,quantos remover, oq inserir)
        arr.slice(0,0,'first')  -> ['first',1,2]

### Iterar elemento
.forEach
    ex: const arr  = [1,2,3,4,5]
        arr.forEach =((value,index) =>{
            console.log(`${index} : ${value}`)
        })

.map: retorna um array de msm tamanho iterando cada item de um array.

    ex: const arr  = [1,2,3,4,5]
    arr.map(value => value * 2) -> [2,4,6,8,10]

.flatMap: retorna um novo array como no função map e executa um flat de profundide 1

### Buscar elementos

.find:irá buscar o primeiro elemento que atender uma condição

     ex: const arr  = [1,2,3,4,5]
         const res = arr.find(value => value > 2) -> [3]
.findIndex: semelhante ao Find, porém retorna o index do elemento

.filter: retorna um novo array com os elementos que satisfazem a condição

.includes: retorna um booleno se o elemento estiver no array

.reverse: inverte a ordem dos elementos 
