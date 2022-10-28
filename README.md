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

 Las imàgenes son una 