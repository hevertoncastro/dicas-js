Entender [hoisting](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var#var_hoisting) irá te ajudar a organizar o escopo de funções. Lembre-se, declarações de variáveis e definições de funções são içadas para o topo. Definições de variáveis não, mesmo se você declarar e definir uma variável na mesma linha. A **declaração** de uma variável permite que o sistema saiba que ela existe enquanto a **definição** lhe atribui um valor.


```javascript
function fazerAlgo() {
  // ReferenceError: naoDeclarada is not defined
  console.log(naoDeclarada);

  // Saída: undefined
  console.log(definidaDepois);
  var definidaDepois;

  definidaDepois = 'Eu estou definida!'
  // Saída: 'Eu estou definida!'
  console.log(definidaDepois);

  // Saída: undefined
  console.log(definidaSimultaneamente);
  var definidaSimultaneamente = 'Eu estou definida!'
  // Saída: 'Eu estou definida!'
  console.log(definidaSimultaneamente);

  // Saída: 'Eu fiz isto!'
  fazerOutraCoisa();

  function fazerOutraCoisa(){
    console.log('Eu fiz isto!');
  }

  // TypeError: undefined is not a function
  funcaoVar();

  var funcaoVar = function(){
    console.log('Eu fiz isto!');
  }
}
```

Para tornar as coisas fáceis de se ler, declare todas variáveis no topo do escopo da sua função para que fique claro de qual escopo elas estão vindo. Defina suas variáveis antes de precisar usá-las. Defina suas funções no final do seu escopo para que fiquem fora do seu caminho.
