# Funções fat arrow ES6

Introduzido como um novo recurso no ES6, funções fat arrow (seta larga) podem vir como uma ferramente útil para escrever mais código em menos linhas. O nome vem da sua síntaxe, => é uma seta larga se comparada com a seta fina ->. Alguns programadores já conhecem este tipo de função de diferentes linguages com o Haskell, como 'expressões lambda' ou como 'funções anônimas'. Isto é chamado de anônimo, já que funções de seta não possuem um nome descritivo.

Quais são os benefícios?

Sintaxe: Menos linhas de código; não é preciso digitar a palavra-chave function toda hora
Semântica: capta a palavra-chave this do seu contexto

Exemplo simples de sintaxe

Dê uma olhada nesses dois trechos de código que fazem exatamente a mesma coisa e entenderá rapidamente o que as funções de seta larga fazem:

//code

// sintaxe geral para funções fat arrow

// também pode ser escrito com parênteses
// parênteses são obrigatórios em múltiplos parâmetros

// usando funções
// usando fat arrow

Como pode ver, a função fat arrow nesse caso poupou tempo removendo os parênteses assim como as palavras-chaves function e return. Aconselho sempre escrever os parêntese em volta dos parâmetros, já que eles serão necessários em múltiplos parâmetros, como em (x,y) => x+y. É apenas uma maneira de não esquecê-los em diferentes casos. Mas o código acima também funcionaria assim: x => x*x. Até então, estas são apenas algumas melhorias que levam a [...]
