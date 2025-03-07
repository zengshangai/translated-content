---
title: Math.SQRT1_2
slug: Web/JavaScript/Reference/Global_Objects/Math/SQRT1_2
tags:
  - JavaScript
  - Math
  - Propiedad
  - Referencia
translation_of: Web/JavaScript/Reference/Global_Objects/Math/SQRT1_2
original_slug: Web/JavaScript/Referencia/Objetos_globales/Math/SQRT1_2
---

{{JSRef}}La propiedad **`Math.SQRT1_2`** representa la raiz cuadrada de 1/2, la cual es equivalente al inverso de la raiz cuadrada de 2, aproximadadamente 0.707:

<math display="block"><semantics><mrow><mstyle mathvariant="monospace"><mi>Math.SQRT1_2</mi></mstyle><mo>=</mo><msqrt><mfrac><mn>1</mn><mn>2</mn></mfrac></msqrt><mo>=</mo><mfrac><mn>1</mn><msqrt><mn>2</mn></msqrt></mfrac><mo>≈</mo><mn>0.707</mn></mrow><annotation encoding="TeX">\mathtt{\mi{Math.SQRT1_2}} = \sqrt{\frac{1}{2}} = \frac{1}{\sqrt{2}} \approx 0.707</annotation></semantics></math>

## Descripción

Debido a que SQRT1_2 es una propiedad estatica de Math, siempre debes utilizarla como Math.SQRT1_2, en lugar de invocarla como una propiedad de alguna instancia de Math que hayas creado ( Math no es un constructor ).

## Ejemplos

### Utilizando `Math.SQRT1_2`

La siguiente funcion regresa la raiz cuadrada de 1/2:

```js
function getRoot1_2() {
  return Math.SQRT1_2;
}

getRoot1_2(); // 0.7071067811865476
```

## Especificaciones

| Especificación                                                                   | Estatus                      | Comentarios                                         |
| -------------------------------------------------------------------------------- | ---------------------------- | --------------------------------------------------- |
| {{SpecName('ES1')}}                                                         | {{Spec2('ES1')}}         | Definición inicial. Implementado en Javascript 1.0. |
| {{SpecName('ES5.1', '#sec-15.8.1.7', 'Math.SQRT1_2')}}         | {{Spec2('ES5.1')}}     |                                                     |
| {{SpecName('ES6', '#sec-math.sqrt1_2', 'Math.SQRT1_2')}}     | {{Spec2('ES6')}}         |                                                     |
| {{SpecName('ESDraft', '#sec-math.sqrt1_2', 'Math.SQRT1_2')}} | {{Spec2('ESDraft')}} |                                                     |

## Navegadores Compatibles

{{Compat("javascript.builtins.Math.SQRT1_2")}}

## Ver Tambien

- {{jsxref("Math.pow()")}}
- {{jsxref("Math.sqrt()")}}
