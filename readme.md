# JS Manipulación DOM

Date Created: 18 de septiembre de 2023 11:59
Status: Doing

# DOM

El modelo de objeto de documento (DOM) es una interfaz de programación para los documentos HTML y XML. Facilita una representación estructurada del documento y define de qué manera los programas pueden acceder, al fin de modificar, tanto su estructura, estilo y contenido

![Untitled](img/Untitled.png)

Es la representación de los objetos (elementos) que conforman la estructura de un documento en la web

![Untitled](img/Untitled%201.png)

![Untitled](img/Untitled%202.png)

Representar el documento HTML a través del DOM nos permite acceder a sus elementos y manipularlos. EL DOM representa a los elementos como nodos y objetos con los cuales podemos trabajar en JS. Podemos trabajar con propiedades, métodos y con distintos eventos

- NODOS: Son puntos específicos del diagrama o árbol de nodos DOM. Son aquellos bordeados de amarillo. Los nodos incluyen el documento en sí, elementos HTML, Texto y comentarios

![Untitled](img/Untitled%203.png)

# Conceptos Importantes

- Root Node (Nodo Raíz): Es el nodos en la parte superior del árbol, en HTML, es <html>

![Untitled](img/Untitled%204.png)

- Parent Node (Nodo Padre): Nodo que contiene a otro nodo en la jerarquía DOM. En este caso head es nodo padre de title

![Untitled](img/Untitled%205.png)

- Child Node (Nodo Hijo): Es el nodo contenido directamente sobre otro nodo. En este caso, title es nodo hijo de head

![Untitled](img/Untitled%206.png)

- Descendant Node (Nodo Descendiente): Es el nodo contenido en la jerarquía de DOM (directa o indirectamente).

![Untitled](img/Untitled%207.png)

Para este caso h1 y a son nodos descendientes de body. También lo son div y p.

- Sibling Nodes (Nodos hermano): Son nodos ubicados en el mismo nivel de la jerarquía DOM

![Untitled](img/Untitled%208.png)

# Nodo vs. Elemento

El concepto nodo es más amplio que el concepto elemento en el DOM. Usualmente nos referimos a los elementos del documento HTML domo elementos. Un nodos puede ser un elemento HTML pero también pueden ser texto o comentarios en el documento

![Untitled](img/Untitled%209.png)

# DOM en Google Chrome

## Archivo HTML

![Untitled](img/Untitled%2010.png)

## Herramientas de desarrollo de Chrome

Usando la extensión Live Server de VSCode. Abrimos la página del código que estamos desarrollando. 127.0.01 es la dirección IP local, el 5500 es el puerto local y finalmente el nombre del archivo.

![Untitled](img/Untitled%2011.png)

Haciendo clicck derecho, Inspeccionar podemos abrir la herramientas de desarrollo de Chrome

![Untitled](img/Untitled%2012.png)

Este es el DOM

![Untitled](img/Untitled%2013.png)

## Cambiar el DOM

Se puede editar el texto desde el DOM haciendo click derecho

![Untitled](img/Untitled%2014.png)

Estos cambios será temporales y se pueden visualizar con ENTER después hacerlos, pero al momento de actualizar la página, volverá a como está el código en VSC. Es una buena herramienta para ver cambios previamente a hacerlos definitivamente

## Nodos que no son elementos

Texto y Comentarios, por ejemplo

# Proyecto: Toppings de Pizza

Creamos la ubicación del proyecto, y vamos a crear el archivo html, css y uno llamada app.js

![Untitled](img/Untitled%2015.png)

Primero vamos a definir el archivo html, con su head y body

- Head: contiene los metas definidos por html 5 y se linkea el archivo de estilos al style.css y el icono del título

![Untitled](img/Untitled%2016.png)

- Body: Vamo a definir un div llamado contenedor, donde van a estar todos los toppings . El ítulo será Toppings de Pizza y definiremos una lista con los diferentes Toppings. A cada uno le vamos a definir una clase y un id que le daremso estilo en el archivo css

![Untitled](img/Untitled%2017.png)

- Archivo CSS

![Untitled](img/Untitled%2018.png)

![Untitled](img/Untitled%2019.png)

![Untitled](img/Untitled%2020.png)

# Vincular JavaScript a HTML

Al final de body, pero dentro de este, llamamos de la siguiente manera al archivo app.js que tendrá nuestro contenido JavaScript

![Untitled](img/Untitled%2021.png)

# Seleccionar Elementos

## .getElementById()