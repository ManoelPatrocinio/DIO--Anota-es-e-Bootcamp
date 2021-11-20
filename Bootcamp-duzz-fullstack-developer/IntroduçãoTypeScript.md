## Introdução ao typeScript

        .fortimente tipado;
        .usa-se Interfarse para definir contratos de estrutura
        .E types p/ definir diferentes interfaces e funções 

### Generic types

Usado quando não sabe qual tipo de valor irá receber, Então usa-se geralmento o valor <T> para definir que não se sabe o tipo de recebido e retornado da função

            ex: function add<T>(array:any[],valor:T){
                    return array.map(item => item + valor);
                 }
                add([1,1,3], 2)
