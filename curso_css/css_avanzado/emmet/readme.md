# Emmet

Emmet es un plugin de atajos del teclado en html y más lenguajes con la función
de escribir código de manera más rápida.

## HTML

Para escribir la estructura básica de html usamos el atajo del teclado `html:5`.

De esta forma podrás escribir la estructura de html de manera más fácil cómoda para ahorrar tiempo.

### Elementos

Para escribir cualquier elemento alguno solo debes escrbir el elemento, por ejemplo: `p`, por tanto esto generará:
```html
<p></p>
```
Además el cursor se posicionará en medio de la etiqueta.

### Situar una etiqueta dentro de otra

Para especificar donde irá cada etiqueta, en estos casos usamos > para especificar que etiqueta se posicionará dentro de la otra con `ul>li`:
```html
<ul>
    <li></li>
</ul>
```

### Añadir contenido a una etiqueta

Para ello, añadimos corchetes después de la etiqueta: `ul>li{Lista}`:

Resultado:
```html
<ul>
    <li>Lista</li>
</ul>
```

Si deseamos enumerar cada elemento, como por ejemplo las listas u otro elemento utilizamos el signo del dolar: `ul>li{Lista $}`.

Resultado:
```html
<ul>
    <li>Lista 1</li>
</ul>
```

### Añadir número de etiquetas

En esta situación usaremos los asteríscos, situados despues del nombre de la etiqueta, y después el número que queremos: `ul>li*4>a{Lista $}`.

Resultado:
```html
<ul>
    <li><a href="">Lista 1</a></li>
    <li><a href="">Lista 2</a></li>
    <li><a href="">Lista 3</a></li>
    <li><a href="">Lista 4</a></li>
</ul>
```

### Añadir clases e id

Para añadir una clase o id se utiliza el mismo símbolo para cada uno de ellos después del nombre del elemento.

**Con clase**: `ul>li*4>a.ul__link{Lista $}`

```html
<ul>
    <li><a href="" class="ul__link">Lista 1</a></li>
    <li><a href="" class="ul__link">Lista 2</a></li>
    <li><a href="" class="ul__link">Lista 3</a></li>
    <li><a href="" class="ul__link">Lista 4</a></li>
</ul>
```

**Con id**: `ul>li*4>a#ul__link{Lista $}`

```html
<ul>
    <li><a href="" id="ul__link">Lista 1</a></li>
    <li><a href="" id="ul__link">Lista 2</a></li>
    <li><a href="" id="ul__link">Lista 3</a></li>
    <li><a href="" id="ul__link">Lista 4</a></li>
</ul>
```

También tenemos la posibilidad de añadir por ejemplo la clase al li, y otra al a usando
`ul.list>li.list__item*4>a.list__link`.

```html
<ul class="list">
    <li class="list__item"><a href="" class="list__link"></a></li>
    <li class="list__item"><a href="" class="list__link"></a></li>
    <li class="list__item"><a href="" class="list__link"></a></li>
    <li class="list__item"><a href="" class="list__link"></a></li>
</ul>
```

Con estos atajos del teclado incluso podemos hacer un nav mucho más rápido: 
`header.header>nav.header-nav>ul.list>li.list__item*4>a.list__link{Link $}`.

```html
<header class="header">
    <nav class="header-nav">
        <ul class="list">
            <li class="list__item"><a href="" class="list__link">Link 1</a></li>
            <li class="list__item"><a href="" class="list__link">Link 2</a></li>
            <li class="list__item"><a href="" class="list__link">Link 3</a></li>
            <li class="list__item"><a href="" class="list__link">Link 4</a></li>
        </ul>
    </nav>
</header>
```

### Añadir atributos

Para añadir atributos a etiquetas html, por ejemplo a un script debemos añadir : y el atributo:
`script:src`
```html
<script src=""></script>
```

## CSS

También podemos dar uso a emmet en css para escribir propiedades y atributos más rápido

### Elementos

Por ejemplo para escribir margin solamente escrbimos `m` y damos tab, y en padding usando una `p`.

Para escribir la propiedad border  de un elemento en shorthand solamente escribirmos `bd`:

```css
element {
    border: 1px solid #000;
}
```

Por defecto mostrará esto como borde, y así lo podrás ir editando.

Para width y height: `w` y `h`.

### Medidas

La sintaxis para indicar una medida, son elemento + medida, por ejemplo con margin se usa `m10` para:

```css
element {
    margin: 10px;
}
```

Si no queremos la medida en píxeles, tendremos que añadir `p` después de la medida: `m10p`:

```css
element {
    margin: 10%;
}
```

Si la queremos en em, ponemos e: `m10e`:

```css
element {
    margin: 10em;
}
```

Si queremos un margin con 2 valores, se separan con guiones: `m10-20`:

```css
element {
    margin: 10px 20px;
}
```

O si combinas tipos de medida: `m10p-20`

```css
element {
    margin: 10% 20px;
}
```

Lo mismo pasa con las demás propiedades de css que incluyan medidas.

Para añadir la propiedad **color usamos** `c`:

```css 
element {
    color: #000;
}
```

Para definir desde el emmet el color añadimos # depués de c: `c#1`,
y esto definirá el color a #111.

```css
element {
    color: #111;
}
```

En cambio si ponemos simplemente 2 valores, el sistema hexadecimal mostrará sus 6 dígitos si
definimos `c#12`:

```css
element {
    color: #121212;
}
```

Y con los 3 valores lo muestra normal con `c#347`:

```css
element {
    color: #347;
}
```

Funciona igual que la propiedad **background-color**, con el emmet `bgc`