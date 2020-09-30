# notes-forms

- los elementos de tipo `input` son `inline`.
- `<input />` no tiene tag de cierre.
- usamos el atributo `type` para determinar el [tipo de campo](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input), según el contenido y formato.
- podemos usar `input`s de forma independiente (si sólo nos interesa leer sus valores), pero si es información que queremos enviar/pedir de algún lado, necesitamos agruparlos dentro de un `form`.
- un `form` funciona como un _container_ de inputs, para enviar/requerir ciertos datos, en un único request.
- los formularios nos sirven para recolectar input.
- asociar las `label`s correspondientes a cada input:

```html
<label for='full-name'>Name</label>
<input id='full-name' name='full-name' type='text'/>
```

- setear el atributo `action` del form para decir a dónde queremos enviar los datos (URL).
- setear el atributo `name` del input para identificar los datos que enviamos en el form.

```html
<form action="http://www.google.com/search" method="get">
  <input type="search" id="search-box" name="q" placeholder="Search..." autocomplete="on" />
  <button type="submit">Search with Google</button>
</form>
```

## Autocomplete Dropdowns sin JS

[Creating Autocomplete Dropdowns with the Datalist Element](https://blog.teamtreehouse.com/creating-autocomplete-dropdowns-datalist-element)

## tips

- es muy recomendable **hacer un wireframe del form antes de empezar a codearlo**, al menos una versión _lo-fi_.
- setear `label` e `input` asociado siempre en el mismo orden, para ser consistentes (y chequear que los atributos `id` y `for` coincidan).
- setear el atributo `required` para los campos que sean obligatorios (`<input required .../>`)
- elegir el tipo de input más apropiado en cada caso, también suma a la accesibilidad/ux.
- si usamos el método `get` para el formulario, los datos de los inputs van a quedar expuestos en la URL. Suele utlizarse para búsquedas.
- si vamos a _enviar_ datos (sobre todo datos sensibles), setear el atributo `method` del form como `post`. De esta forma, los datos se agregan al `body` del request y no se muestran en la URL (ej: passwords).

```html
<form action="https://google.com" method="post">
  ...
</form>
```
