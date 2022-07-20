# Markdown Tutorial
This is a short summary about Markdown functionalities and how to use this language

**Autor:** Santiago González Montealegre

# Aprendiendo _Markdown_

## Índice

1. [Párrafos y funciones de texto](#párrafos-y-funciones-de-texto)
1. [Encabezados](#encabezados)
1. [Enlaces](#enlaces)
1. [Imágenes](#imágenes)
1. [Divisiones](#divisones)
1. [Listas](#listas)
1. [Citas](#citas)
1. [Tablas](#tablas)
1. [Código](#código)
1. [HTML](#html)
1. [Comentarios](#comentarios)
1. [Escape de carácteres](#escape-de-carácteres)

---

## Párrafos y funciones de texto

[Índice](#índice)

En _Markdown_ los párrafos funcionan solamente escribiendo el código directamente, no es necesario usar ningún tipo de comando especial.

Por ejemplo:

```markdown
    Esto es un párrafo
```

Que se muestra así:

Esto es un párrafo

Nota: Un enter funciona de forma normal.

#### Cursiva

```markdown
    _Texto en Cursiva_
```

_Texto en Cursiva_

<br>

#### Negrita

```markdown
    **Texto en Negrita**
```

**Texto en Negrita**

<br>

De igual forma, puedes combinar ambos atributos al tiempo

```markdown
    **_cursiva y negrita_**
```

**_cursiva y negrita_**

---

## Encabezados

[Índice](#índice)

En _Markdown_ existen 6 niveles de encabezado, siendo 1 el más importante y el número 6 el menos. Para poner un encabezado es necesario el símbolo `#` seguido de un es espacio (` `) para posteriormente si escribir el título.

Por ejemplo:

```markdown
    # Ejemplo de Encabezado Tipo 1
```

Se muestra así:

# Ejemplo de Encabezado Tipo 1

Como se mencionó anteriormente hay 6 niveles o tipos de encabezados, se accede a cada nivel dependiendo del número de `#` que se utilicen.

Por ejemplo:

```markdown
    ## Encabezado 2

    ### Encabezado 3

    #### Encabezado 4

    ##### Encabezado 5

    ###### Encabezado 6
```

Se muestra así:

## Encabezado 2

### Encabezado 3

#### Encabezado 4

##### Encabezado 5

###### Encabezado 6

---

## Enlaces

[Índice](#índice)

- Enlaces a páginas web

```markdown
    [Texto a mostrar como preview del link](url)

    [Youtube](https://youtube.com)
```

[Youtube](https://youtube.com)

<br>

- Enlaces a elementos dentro del documento

```markdown
    [Texto a mostrar como preview del link o de la sección a donde se mandará](#aprendiendo-markdown)

    [Aprendiendo _Markdown_](#aprendiendo-_markdown_)
```

[Aprendiendo _Markdown_](#aprendiendo-_markdown_)

---

## Imágenes

[Índice](#índice)

- Las imágenes se insertan de forma similar a los links

```markdown
    ![Texto a mostrar como resumen de la imagen](url de la imagen o ubicación local)

    ![Imagen de prueba](https://i.ibb.co/58F21MR/image.png)
```

![Imagen de prueba](https://i.ibb.co/58F21MR/image.png)

<br>

- Lo malo de esta implementación es que no se puede modificar el ancho o la altura (`withxheight`), por lo tanto, debemos usar código html.

```html
<img src="url de la imagen" width="250" height="250" />

<img
	src="https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg"
	width="250"
	height="250"
/>
```

<img src="https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg" width="250" height='250'/>

<br>
<br>

- Hay una tercera opción donde combinamos los links de markdown con las imágenes de html. Esta consite en insertar un link donde está la imagen, de forma que al hacer click en la imagen nos redirija al sitio de la imagen. Mientras que la preview del link en markdown tendrá el valor del código html de la imagen, por lo tanto, la preview del link será la misma imagen.

```markdown
    [<img src="url de la imagen" width="250" height='250'/>](url de la imagen)

    [<img src="https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg" width="250"/>](https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg)
```

[<img src="https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg" width="250"/>](https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg)

---

## Divisones

[Índice](#índice)

Podemos usar las divisiones para seperar partes del documento, esto simboliza que se tratará un tema aparte al de la sección anterior.
Se realiza esta división de la siguiente forma:

```markdown
    ---
```

---

## Listas

[Índice](#índice)

#### Ordered list

Se coloca de la siguiente forma:

```markdown
    1. Primavera
        1. Abril
        1. Mayo
        1. Junio
    1. Verano
        1. Julio
        1. Agosto
        1. Septiembre
```

Notese que se usa siempre el `1.` así estemos ya en el segundo elemento de la lista. Esto se debe a que markdown se encarga de poner los números siguientes sin que nosotros nos preocupemos.

A continuación se muestra esta lista

1. Primavera
   1. Marzo
   1. Abril
   1. Mayo
1. Verano
   1. Junio
   1. Julio
   1. Agosto

<br>

#### Unordered list

Se coloca de la siguiente forma:

```markdown
    * Primavera
        - Marzo
        - Abril
        - Mayo
    * Verano
        - Junio
        - Julio
        - Agosto
```

Nota: es equivalente usar `*` o usar `-` para inicar un elemento de la lista.

A continuación se muestra esta lista

- Primavera
  - Marzo
  - Abril
  - Mayo
- Verano
  - Junio
  - Julio
  - Agosto

---

## Citas

[Índice](#índice)

#### Cita en línea

Se usa el siguiente símbolo `>` (mayor que) para iniciar una cita

```markdown
> Siempre tienes opción de no tener opinión. - Marco Aurelio
```

Se muestra de la siguiente forma:

> Siempre tienes opción de no tener opinión. - Marco Aurelio

<br>

#### Cita en bloque

Para realizar una cita más larga, o que necesita de varias líneas podemos usar dos métodos:

- Iniciar una cita **en línea** y poner enter en cada salto de línea (obviamente):

```markdown
    > Todo lo que escuchamos es una opinión, no un hecho.
    Todo lo que vemos es una persepectiva, no la verdad.
    _Marco Aurelio_
```

Se muestra de la siguiente forma:

> Todo lo que escuchamos es una opinión, no un hecho.
> Todo lo que vemos es una persepectiva, no la verdad.
> _Marco Aurelio_

Nota: Este método no funciona en GitHub, pero si en el navegador normal. Por lo tanto, se recomienda el siguiente método.

<br>

- Iniciar una cita **en línea** en cada una de las líneas del bloque, esto permite poner líneas vacías entre cada renglón:

```markdown
    > Todo lo que escuchamos es una opinión, no un hecho.
    >
    > Todo lo que vemos es una persepectiva, no la verdad.
    >
    > _Marco Aurelio_
```

Se muestra de la siguiente forma:

> Todo lo que escuchamos es una opinión, no un hecho.
>
> Todo lo que vemos es una persepectiva, no la verdad.
>
> _Marco Aurelio_

---

## Tablas

[Índice](#índice)

Para crear una tabla se debe primero crear la línea de encabezados, seguido por una línea de guiones (`---`). Cada celda de la tabla (intersección de fila y columna) debe ir rodeada de `|` de apertura y de cierre. e.g. `| texto |`:

```markdown
    | Nombre   | Edad | Correo             |
    | -------- | ---- | ------------------ |
    | Santiago | 18   | santiago@gmail.com |
```

Se muestra de la siguiente forma:

| Nombre   | Edad | Correo             |
| -------- | ---- | ------------------ |
| Santiago | 18   | santiago@gmail.com |

---

## Código

[Índice](#índice)

#### Código en línea

Para insertar un ejemplo de código dentro de un párrafo se usa el siguiente símbolo ` `` `. Es una tilde al revés la cual se puede poner con la combinación de teclas `alt + }`.

#### Código en bloque

Para insertar un bloque entero de código debemos poner 3 veces el símbolo ` `` `, posteriormente, de forma opcional pero para visualizar de mejor manera el código se puede digitar el lenguaje del cual estamos colocando código. En una nueva línea insertamos el código; finalemente, en una nueva línea repetimos el primer paso.

Ahora obsevamos un ejemplo del código _markdown_

````markdown
    ```js
    function sumar(a, b) {
        return a + b;
    }
    ```
````

Que se visualiza de la siguiente forma:

```js
function sumar(a, b) {
	return a + b;
}
```

---

## Html

[Índice](#índice)

Se puede usar cualquier tipo de etiqueta que funciona en html

```html
<form>
	<label for="q">Buscar:</label>
	<input type="search" name="q" id="q" />
</form>
```

<form>
    <label for='q'>Buscar:</label>
    <input type='search' name='q' id='q'>
</form>

---

## Comentarios

[Índice](#índice)

Para poner comentarios dentro de nuestro código es igual a la forma en que se usa en _html_. Con los símbolos de inicio `<!--` y final `-->`

Un ejemplo:

```markdown
<!-- Esto es un comentario -->
```

Nota: también es posible usar el shortcut de VSCode `alt + shift + a`.

---

## Escape de carácteres

[Índice](#índice)

Para el escape de carácteres se hace uso del símbolo `\` seguido del caracter especial.

Ejemplo:

```markdown
    **negrita**
    \*\*negrita\*\*
```

Resultado:

**negrita**

\*\*negrita\*\*
