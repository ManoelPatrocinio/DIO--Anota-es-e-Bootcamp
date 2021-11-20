## Desenvolvimento de aplicações para internet com ReactJS

### Stateful vs Stateless

        Stateful: o componente usa estados,logo possui gerenciamento de estado dentro do componente.
        Stateless: o componente não usa estados, é construido usando funções

    * componentes controlados: aceitão a atributo value e podemos mudar esses valor com o atributo onChange.
        ex: select,input,textArea,radio ...

### arquitetura redux

    REACT(view): acrecenta 3 novos conceitos
    ACTION: tem como diferença do flux, o fato de não enviar a action em si para o despatcher, mais retornam um objeto de action formtado
    STORE: Em redux temos apenas uma store, que cuida de toda arvore de estados, e os reducer que cuidam de descobrir qual estado muda
    REDUCER: a store se conecta ao root reducer, que divide os estados em pequenos reducers para descobrir como lidar com esse estado, que são imutáveis.


### Rest HTTP com React

APIs HTTP servem para conectar um ou mais servidores HTTP

FETCH API: nativa do browser, não envia ou recebe cookies(precisa definir as credentials e não rejeita o status do erro http)

Axios: Lib de HTTP APi, cross-browser, pode monitorar o progreso de uma request,melhor tratamento de erro e teste.

### Imutabilidade e Redux
 seus três principos são:

1º Uma vez criada uma coleção não pode ser alterada.
2 Novas coleções podem ser criadas a partir da anterior ou mutação
3º Novas coleçõe são criadas usando o maximo da estrutura original, reduzindo a copia e aumentando a performace.

Beneficios: Perfomace, Programação e debugging mais simples.


É possivel aplicar usando shouldComponentUpdate ou React.PureComponent.

### TDD e BDD com Jest

TDD(Test-Driven Development) antecipa erros a nivel de desenvolvimento, com teste feitos antes do escrita da funcionalidade.

        .Teste Unitário: teste de parte/funcionalidade
        . E2E: teste de fluxo
BDD Behavior-Driven Development, teste de especificação que une teste automatizado e premissa de teste(documento de teste)

