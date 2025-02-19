---
title: Performance.toJSON()
slug: Web/API/Performance/toJSON
translation_of: Web/API/Performance/toJSON
---
{{APIRef("High Resolution Timing")}}

O método **`toJSON()`** da interface {{domxref("Performance")}} é um serializador padrão: Ele retorna uma representação em JSON das propriedades do objeto performance.

## Sintaxe

```
minhaPerf = performance.toJSON()
```

### Argumentos

Nenhum

### Valor de retorno

- minhaPerf
  - : Um objeto JSON que é a serialização do objeto {{domxref("Performance")}}.

## Exemplo

```js
var js;
js = window.performance.toJSON();
console.log("json = " + JSON.stringify(js));
```

## Especificações

| Specification                                                                                                            | Status                                       | Comment            |
| ------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------- | ------------------ |
| {{SpecName('Highres Time Level 2', '#the-performance-interface', 'toJSON() serializer')}} | {{Spec2('Highres Time Level 2')}} | Define `toJson()`. |

## Compatibilidade com navegadores

{{Compat("api.Performance.toJSON")}}
