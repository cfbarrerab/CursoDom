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

Con este método, podemos seleccionar y ver propiedades de los objetos según su id. El Id de cada elemento DEBE SER ÚNICO

![Untitled](img/Untitled%2022.png)

y console.log podemos ver varias cosas de ese objeto

![Untitled](img/Untitled%2023.png)

![Untitled](img/Untitled%2024.png)

También, con el método inner.HTML podemos ver el código que define ese Id

![Untitled](img/Untitled%2025.png)

![Untitled](img/Untitled%2026.png)

Con el método innerText podemos ver el texto de ese ID

![Untitled](img/Untitled%2027.png)

Y también podemos ver el tipo de etiqueta que tiene con tagName

![Untitled](img/Untitled%2028.png)

![Untitled](img/Untitled%2029.png)

## .getElementByClassName()

De la misma manera que con el seleccionador por Id, lo hacemos con las clases y vemos como sale en la consola

![Untitled](img/Untitled%2030.png)

![Untitled](img/Untitled%2031.png)

Esto muestra la clase como un arreglo, entonces podemos acceder a cualquiera de sus elementos de la siguiente manera

![Untitled](img/Untitled%2032.png)

![Untitled](img/Untitled%2033.png)

## .getElementByTagName()

De manera análoga a las anteriores, ahora buscamos por etiqueta. Para este caso los elementos de lista li

![Untitled](img/Untitled%2034.png)

![Untitled](img/Untitled%2035.png)

## .querySelector() y .querySelectorAll()

Nos permite seleccionar un elemento por su selector CSS. El primero selecciona el primero que cumpla ese selector, el segundo selecciona a todos

![Untitled](img/Untitled%2036.png)

![Untitled](img/Untitled%2037.png)

Tambien puede buscar mas de una clase 

![Untitled](img/Untitled%2038.png)

Para el selector .querySelectorAll, nos retorna TODOS LOS ELEMENTOS con las propiedades indicadas. Aca un ejemplo, donde nos muestra un nodo con dos elementos

![Untitled](img/Untitled%2039.png)

![Untitled](img/Untitled%2040.png)

# Asignar Estilo

Primero, debemos acceder al elemento a darle estilo con los selectores vistos anteriormente

![Untitled](img/Untitled%2041.png)

![Untitled](img/Untitled%2042.png)

Habiendo accedido al objeto, podemos acceder a sus propiedades de estilo. Usamos la notación de punto .style y podemos ver la propiedad en consola

![Untitled](img/Untitled%2043.png)

![Untitled](img/Untitled%2044.png)

Entonces, como asignando valor a una constante, definimos una propiedad de estilo a ese elemnto

![Untitled](img/Untitled%2045.png)

![Untitled](img/Untitled%2046.png)

![Untitled](img/Untitled%2047.png)

![Untitled](img/Untitled%2048.png)

# Texto en el DOM

## Acceder al Texto

Accedemos al elemento, en este caso por ID

![Untitled](img/Untitled%2049.png)

![Untitled](img/Untitled%2050.png)

con innerText accedemos al texto, pero tambien podemos hacerlo con textContent. Este último nos muestra el texto con las indentaciones que tienen en el código HTML

![Untitled](img/Untitled%2051.png)

![Untitled](img/Untitled%2052.png)

Y con innerHTML, nos retorna el código de ese elemento como una cadena de caracteres

![Untitled](img/Untitled%2053.png)

![Untitled](img/Untitled%2054.png)

## Modificar el Texto

Vamos a modificar el título, primero accedemos al elemento. Luego podemos modificar el valor de esta variable

![Untitled](img/Untitled%2055.png)

![Untitled](img/Untitled%2056.png)

# Atributos

Vamos a agregar luego de la lista de toppings, un enlace

![Untitled](img/Untitled%2057.png)

Creamos una constante y validamos que salga bien en la consola

![Untitled](img/Untitled%2058.png)

![Untitled](img/Untitled%2059.png)

Como es una colección, es decir un arreglo, podemos acceder a sus elemento y revisar sus atributos, por ejemplo.

![Untitled](img/Untitled%2060.png)

![Untitled](img/Untitled%2061.png)

Y removerlo así

![Untitled](img/Untitled%2062.png)

También podemos darle atributos al elemento

![Untitled](img/Untitled%2063.png)

# Clases

Se puedes tambien agregar, anidar o modificar clases

Se peude acceder mediante la propiedad classList

![Untitled](img/Untitled%2064.png)

![Untitled](img/Untitled%2065.png)

## Agregar una clase

Habiendo definido el elemento, podemos agregar una clase de la siguiente manera

![Untitled](img/Untitled%2066.png)

Si añadimos propiedades a esa clase en el archivo css, el primer elemento de clase topping tendrá color verde en el texto

![Untitled](img/Untitled%2067.png)

![Untitled](img/Untitled%2068.png)

![Untitled](img/Untitled%2069.png)

![Untitled](img/Untitled%2070.png)

## Verificar si una cadena existe

Con el metodo contains, podemos validar si una clase existe en la lista de clases

![Untitled](img/Untitled%2071.png)

Su salida será booleana

![Untitled](img/Untitled%2072.png)

![Untitled](img/Untitled%2073.png)

## Eliminar una clase

Se hace con el método remove

![Untitled](img/Untitled%2074.png)

![Untitled](img/Untitled%2075.png)

# Crear un elemento en DOM