Uma das características mais apreciadas do AngularJs é o two-way data binding. Para fazer este trabalho o AngularJs avalia as mudanças entre o model e a view através de ciclos ( $digest ). Você precisa entender esse conceito para entender como o framework funciona debaixo do capô.

Angular avalia cada observador quando um evento é disparado. Esse é o ciclo conhecido como `$digest`. Algumas vezes você precisa forçar a execução de um novo ciclo manualmente e deve escolher a opção correta pois esta fase é uma das que mais influencia em termos de performance.

### `$apply`
This core method lets you to start the digestion cycle explicitly. That means that all watchers are checked; the entire application starts the `$digest loop`. Internally, after executing an optional function parameter, it calls `$rootScope.$digest();`.

### `$digest`
In this case the `$digest` method starts the `$digest` cycle for the current scope and its children. You should notice that the parent's scopes will not be checked.
 and not be affected.

### Recommendations
- Use `$apply` or `$digest` only when browser DOM events have triggered outside of AngularJS.
- Pass a function expression to `$apply`, this has an error handling mechanism and allows integrating changes in the digest cycle.

```javascript
$scope.$apply(() => {
	$scope.tip = 'Javascript Tip';
});
```

- If you only need to update the current scope or its children, use `$digest`, and prevent a new digest cycle for the whole application. The performance benefit is self-evident.
- `$apply()` is a hard process for the machine and can lead to performance issues when there is a lot of binding.
- If you are using >AngularJS 1.2.X, use `$evalAsync`, which is a core method that will evaluate the expression during the current cycle or the next. This can improve your application's performance.
