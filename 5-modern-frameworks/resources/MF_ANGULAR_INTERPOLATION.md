# Changing Interpolation Tokens

Here's an interesting feature of Angular. You can change the tokens that it looks for in your HTML to indicate JavaScript variable interpolation. By default it looks for `{{` at the beginning of a word and `}}` and the end. You can make these whatever you like.

You can use double hash if you like. Having the same pattern for start and end works perfectly fine.

```js
var app = angular
  .module("TodoApp", [])
  .config(function($interpolateProvider) {
    $interpolateProvider.startSymbol('##');
    $interpolateProvider.endSymbol('##');
});
```

How about `-=interpolatedJavaScriptVariable=-`?

```
  $interpolateProvider.startSymbol('-=');
  $interpolateProvider.endSymbol('=-');
```