# HTML CSS BOOTSTRAP

Html Css y Javascrip son los pilares de toda aplicaciòn o sitio web.
Cualquier cosa que funcione dentro de un navegador web (chrome, mozilla, safari) utiliza estos pilares. Y no solo, hoy tambièn se pueden hacer aplicaciones "nativas" con estas tecnologìas.

## HTML

Significa **Hyper Text Markup Language**, que en castellano serìa algo
como Lenguaje de marcado de hyper texto. Lenguaje de marcado es por la 
*Etiquetas*. Dependiendo de su etiqueta el navegador lo procesa de diferente forma. Y el hyper texto se refiere a que estos documentos estàn enlazados por *links*.

Con HTML crearemos *documentos estructutados* mediante etiquetas que el navegador puede interpretar.

El documentos principal de un sitio o aplicaciòn se debe llamar **index.html**. Todo junto yen minùsculas.

Estas primeras etiqueta indica al navegador la versiòn de HTML. En este caso ìndica que es la versiòn 5.
```html
<!DOCTYPE html>
```
Luego de eso viene la primera etiqueta es es parte del documento. la famosa etiqueta **html**:
```html
<html lang="en">
    ...
<html>
```
Del ejemplo anterior vemos que esta etiqueta se compone de 2 partes principales. La etiqueta de apertura y cierra irà el contenido.

Ademàs vemos la etiqueta de apertura tiene el **atributo** `lang="es"`,lo que le indica al navegador en què idioma està el contenido del documento.

>**ATENCIÒN**: Solo la etiquetas de apertura pueden tener atributos, Las etiquetas de cuerre no.

### head

A continuaciòn viene etiquetas `head`.
Estas etiquetas entrga informaciòn al **Navegador** sobre como visualizar el contenido que vendrà en las siguientes secciones.
Por ejemplo se indica mediante etiquetas `meta` el se de caracteres que utilizarà la pàgina.
Ejemplo:
```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```
La tercera etiqueta `meta` que tiene el atributo `name="viewport"` permite que el contenido se cargue inicialmente considerando el tamaño de pantalla disponible, desde grandes a muy pequeños.

Ademas dentro del head se encuentra la etiqueta `title`, que es la encargada de mostrar el nombre del sitio en la pestaña del navegador,

Por otra parte dentro del `head` podemos cargar otros recursos que utilizrà el documento como por ejemplo hojas de estilo CSS o archivos Javascript

### Estructura Jeràrquica

Algo que es muy muy muy importante notar y que no es tan evidente, es que los documentos HTML forman una estructura jeràrquica bien definida del tipo àrbol.

Donde la etiqueta raìz es la etiqueta `html`. Lo podemos visualizar de la siguiente forma

```html
<html>
    <head></head>
    <body></body>
<html>
```
Esto es muy importante de comprender ya que luego manejaremos las etiquetas pensando en su ubicación relativa dentro del árbol. Y pensaremos que las etiquetas son **nodos** que tienen **nodos padre**, **hermanos** y **nodos hijos**.

## Etiquetas principales

### Tìtulos

Las etiquetas para hacer tìtulos son las etiquetas **h** con nùmeros del 1 al 6. Ejemplos

```html
<h1>Sùper tìtulo</h1>
 <h2>Super sub titulo</h2>   
 <h3>Supr sub sub titulo</h3>
<h4>....</h4>
<h5>...</h5>
<h6>..</h6>
```

### Links

Los links son el corazòn de internet y los crearemos frecuentemente. Se componen de el atributo `href` que indica el destino del link y su contenido, que es lo que se muestra al usuario
```html
 <a href="headings.   html">Tìtulos</a>
 ```

 ### Imagenes

Las imágenes son una de las etiquetas que no require de cierre ya que la imagen que se despliega se indica mediante el atributo `src` y en caso de que la imagen no esté disponible se despliega el texto indicado en el atributo `alt` conocido como texto alternativo.

### Listas

#### Ordenadas

```html
  <ol>Dias de la semana
    <li>Lunes</li>
    <li>Martes</li>
    <li>Miércoles</li>
    <li>Jueves</li>
    <li>Viernes</li>
  </ol> 
```

### No ordenadas

```html
  <ul>Pilares de la Web
    <li>HTML</li>
    <li>CSS</li>
    <li>Javascript</li>
  </ul>
```

### Tablas

```html
  <table>
    <tr>
      <th>Italiano</th>
      <th>Chacarero</th>
    </tr>
    <tr>
      <td>Tomate</td>
      <td>Lechuga</td>
    </tr>
    <tr>
      <td>Palta</td>
      <td>Porotos</td>
    </tr>
    <tr>
      <td>Mayo</td>
      <td>Ají</td>
    </tr>
  </table>
```


# css


Ejemplo de selector por id
```css
#fname{
  border-radius: 6px;
}
```CSS es muy flexible y permite combinar selectores, Ej:
```css
p.centered{
  text-align:center;
  color: purple;
}
```
Si tenemos reglas que se repiten. Ejemplo```cssh1{
  text-align: center;
  color: blue
}h2{
  text-align: center;
  color: blue
}
```
Podemos refactorizarlo en una sola regla:```css
h1, h2{
  text-align: center;
  color: blue
}
```
Selector | Ejemplo | Descripcion
----|----|----
#id | .some-id | Selecciona el elemento con `id="some.id"`
.class | .some-class | Selecciona TODOS los elementos con clase `class="some-class"`
element.class | p.intro | Selecciona solor los `<p>`con clase `class="intro"`
element, element | div, p | Selecciona todos los elementos `<div>` y `<p>`
### Modelo de caja 

En esencia cada elemento html está inserto dentro de una caja que consiste de: Margen, Borde, Padding y contenido.

![Box Model](img/box-model.png)

### Unidades de medida 

En general, no solo en desarrollo, podemos clasificar las unidades de medidas en dos grupos:

- Unidades Absolutas: pixel(px)
- Unidades Relativas: porcentaje(%), rem, em, vh, vw#

## rem
Es una unidad de medida relativa al font-size del elemento raíz.

### em
Es relativa  al font-size del mismo elemento

### vh
Es relativo al 1% del alto de la pantalla o (viewport)

### vw
Es relativo al 1% del ancho de la pantalla o viewport

### Tipos de diseno

- El diseno estatico:Sirve para un solo tamano de pantalla.
- El diseno fluido:Se basa en porcentaje(%)dependiendo del tamano de la pantalla.
- Diseno responsivo: Tiene puntos de quiebre(distintos tamanos) para aplicar diferentes estilos.

### CSS MediaQueries

Utiliza la regla '@media' para incluir un bloque de propiedades CSS solo si la condicion es verdadera.Ejemplo:

```css


/* si el tamano de la pantalla es de 600px o menor, el color de fondo del body sera verde*/
@media only screen and (max-width: 600px){
    body {
        background-color: green;
    }
}
```

Existe ciertos tamanos de pantalla mas o menos estandarizados y estas serian sus respectivas media queries:

```css
/* Extra small devices (phones, 600px and down)*/
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up)*/
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up)*/
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops,992px and up)*/
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up)*/
@media only screen and (min-width: 1200px) {...}
```

### Display

```css
/* si el tamano de la pantalla es de 600px o menor, el color de fondo del body sera verde*/
@media only screen and (max-width: 600px) {...}







