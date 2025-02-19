---
title: ':active'
slug: Web/CSS/:active
tags:
  - CSS
  - Diseño
  - Pseudo-clase
  - Referencia
  - Web
translation_of: Web/CSS/:active
---
{{CSSRef}}

La [pseudo-clase](/es/docs/CSS/Pseudo-classes) `:active` de [CSS](/es/docs/Web/CSS) representa un elemento (como un botón) que el usuario está activando. Cuando se usa un mouse, la "activación" generalmente comienza cuando el usuario presiona el botón primario del mouse y termina cuando se suelta. La pseudo-clase `:active` se usa comúnmente en los elementos {{HTMLElement("a")}} y {{HTMLElement("button")}}, pero también se puede usar en otros elementos.

```css
/* Selecciona cualquier <a> que esté siendo activado */
a:active {
  color: red;
}
```

Los estilos definidos por la pseudoclase `:active` serán anulados por cualquier pseudoclase posterior relacionada con el enlace ({{cssxref(":link")}}, {{cssxref(":hover")}} o {{cssxref(":visited")}}) que tenga al menos la misma especificidad. Para darle un estilo apropiado a los enlaces, coloque la regla `:active` después de todas las demás reglas relacionadas con el enlace, tal como lo define el orden LVHA: `:link` — `:visited` — `:hover` — `:active`.

> **Nota:** En los sistemas con los ratones de varios botones, CSS3 especifica que la pseudo-clase `:active` sólo debe aplicarse al botón primario; en ratones diestros, este suele ser el botón más a la izquierda.

## Sintaxis

{{csssyntax}}

## Ejemplo

### HTML

```html
<a href="#">Este enlace cambiará a color lima mientras hace clic en él.</a>
```

### CSS

```css
a:link { color: blue; }          /* Enlaces no visitados */
a:visited { color: purple; }     /* Enlaces visitados */
a:hover { background: yellow; }  /* El usuario esta sobre el enlace */
a:active { color: lime; }        /* Enlaces activos */
```

### Resultado

{{EmbedLiveSample('Ejemplo')}}

## Especificaciones

| Especificación                                                                                   | Estado                               | Comentarios         |
| ------------------------------------------------------------------------------------------------ | ------------------------------------ | ------------------- |
| {{SpecName('HTML WHATWG', 'scripting.html#selector-active', ':active')}} | {{Spec2('HTML WHATWG')}}     |                     |
| {{SpecName('CSS4 Selectors', '#active-pseudo', ':active')}}                 | {{Spec2('CSS4 Selectors')}} | Ningún cambio.      |
| {{SpecName('CSS3 Selectors', '#useraction-pseudos', ':active')}}             | {{Spec2('CSS3 Selectors')}} | Ningún cambio.      |
| {{SpecName('CSS2.1', 'selector.html#dynamic-pseudo-classes', ':active')}} | {{Spec2('CSS2.1')}}             | Ningún cambio.      |
| {{SpecName('CSS1', '#anchor-pseudo-classes', ':active')}}                     | {{Spec2('CSS1')}}             | Definición Inicial. |

## Compatibilidad con navegadores

{{Compat("css.selectors.active")}}

## Ver también

- Pseudo-clases relacionadas con enlaces: {{cssxref(":link")}}, {{cssxref(":visited")}}, y {{cssxref(":hover")}}
