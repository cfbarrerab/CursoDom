# JS Manipulación DOM

Date Created: 18 de septiembre de 2023 11:59
Status: Done 🙌

# DOM

El modelo de objeto de documento (DOM) es una interfaz de programación para los documentos HTML y XML. Facilita una representación estructurada del documento y define de qué manera los programas pueden acceder, al fin de modificar, tanto su estructura, estilo y contenido

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled.png)

Es la representación de los objetos (elementos) que conforman la estructura de un documento en la web

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%201.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%202.png)

Representar el documento HTML a través del DOM nos permite acceder a sus elementos y manipularlos. EL DOM representa a los elementos como nodos y objetos con los cuales podemos trabajar en JS. Podemos trabajar con propiedades, métodos y con distintos eventos

- NODOS: Son puntos específicos del diagrama o árbol de nodos DOM. Son aquellos bordeados de amarillo. Los nodos incluyen el documento en sí, elementos HTML, Texto y comentarios

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%203.png)

# Conceptos Importantes

- Root Node (Nodo Raíz): Es el nodos en la parte superior del árbol, en HTML, es <html>

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%204.png)

- Parent Node (Nodo Padre): Nodo que contiene a otro nodo en la jerarquía DOM. En este caso head es nodo padre de title

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%205.png)

- Child Node (Nodo Hijo): Es el nodo contenido directamente sobre otro nodo. En este caso, title es nodo hijo de head

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%206.png)

- Descendant Node (Nodo Descendiente): Es el nodo contenido en la jerarquía de DOM (directa o indirectamente).

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%207.png)

Para este caso h1 y a son nodos descendientes de body. También lo son div y p.

- Sibling Nodes (Nodos hermano): Son nodos ubicados en el mismo nivel de la jerarquía DOM

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%208.png)

# Nodo vs. Elemento

El concepto nodo es más amplio que el concepto elemento en el DOM. Usualmente nos referimos a los elementos del documento HTML domo elementos. Un nodos puede ser un elemento HTML pero también pueden ser texto o comentarios en el documento

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%209.png)

# DOM en Google Chrome

## Archivo HTML

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2010.png)

## Herramientas de desarrollo de Chrome

Usando la extensión Live Server de VSCode. Abrimos la página del código que estamos desarrollando. 127.0.01 es la dirección IP local, el 5500 es el puerto local y finalmente el nombre del archivo.

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2011.png)

Haciendo clicck derecho, Inspeccionar podemos abrir la herramientas de desarrollo de Chrome

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2012.png)

Este es el DOM

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2013.png)

## Cambiar el DOM

Se puede editar el texto desde el DOM haciendo click derecho

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2014.png)

Estos cambios será temporales y se pueden visualizar con ENTER después hacerlos, pero al momento de actualizar la página, volverá a como está el código en VSC. Es una buena herramienta para ver cambios previamente a hacerlos definitivamente

## Nodos que no son elementos

Texto y Comentarios, por ejemplo

# Proyecto: Toppings de Pizza

Creamos la ubicación del proyecto, y vamos a crear el archivo html, css y uno llamada app.js

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2015.png)

Primero vamos a definir el archivo html, con su head y body

- Head: contiene los metas definidos por html 5 y se linkea el archivo de estilos al style.css y el icono del título

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2016.png)

- Body: Vamo a definir un div llamado contenedor, donde van a estar todos los toppings . El ítulo será Toppings de Pizza y definiremos una lista con los diferentes Toppings. A cada uno le vamos a definir una clase y un id que le daremso estilo en el archivo css

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2017.png)

- Archivo CSS

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2018.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2019.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2020.png)

# Vincular JavaScript a HTML

Al final de body, pero dentro de este, llamamos de la siguiente manera al archivo app.js que tendrá nuestro contenido JavaScript

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2021.png)

# Seleccionar Elementos

## .getElementById()

Con este método, podemos seleccionar y ver propiedades de los objetos según su id. El Id de cada elemento DEBE SER ÚNICO

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2022.png)

y console.log podemos ver varias cosas de ese objeto

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2023.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2024.png)

También, con el método inner.HTML podemos ver el código que define ese Id

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2025.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2026.png)

Con el método innerText podemos ver el texto de ese ID

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2027.png)

Y también podemos ver el tipo de etiqueta que tiene con tagName

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2028.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2029.png)

## .getElementByClassName()

De la misma manera que con el seleccionador por Id, lo hacemos con las clases y vemos como sale en la consola

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2030.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2031.png)

Esto muestra la clase como un arreglo, entonces podemos acceder a cualquiera de sus elementos de la siguiente manera

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2032.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2033.png)

## .getElementByTagName()

De manera análoga a las anteriores, ahora buscamos por etiqueta. Para este caso los elementos de lista li

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2034.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2035.png)

## .querySelector() y .querySelectorAll()

Nos permite seleccionar un elemento por su selector CSS. El primero selecciona el primero que cumpla ese selector, el segundo selecciona a todos

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2036.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2037.png)

Tambien puede buscar mas de una clase 

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2038.png)

Para el selector .querySelectorAll, nos retorna TODOS LOS ELEMENTOS con las propiedades indicadas. Aca un ejemplo, donde nos muestra un nodo con dos elementos

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2039.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2040.png)

# Asignar Estilo

Primero, debemos acceder al elemento a darle estilo con los selectores vistos anteriormente

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2041.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2042.png)

Habiendo accedido al objeto, podemos acceder a sus propiedades de estilo. Usamos la notación de punto .style y podemos ver la propiedad en consola

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2043.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2044.png)

Entonces, como asignando valor a una constante, definimos una propiedad de estilo a ese elemnto

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2045.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2046.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2047.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2048.png)

# Texto en el DOM

## Acceder al Texto

Accedemos al elemento, en este caso por ID

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2049.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2050.png)

con innerText accedemos al texto, pero tambien podemos hacerlo con textContent. Este último nos muestra el texto con las indentaciones que tienen en el código HTML

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2051.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2052.png)

Y con innerHTML, nos retorna el código de ese elemento como una cadena de caracteres

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2053.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2054.png)

## Modificar el Texto

Vamos a modificar el título, primero accedemos al elemento. Luego podemos modificar el valor de esta variable

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2055.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2056.png)

# Atributos

Vamos a agregar luego de la lista de toppings, un enlace

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2057.png)

Creamos una constante y validamos que salga bien en la consola

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2058.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2059.png)

Como es una colección, es decir un arreglo, podemos acceder a sus elemento y revisar sus atributos, por ejemplo.

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2060.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2061.png)

Y removerlo así

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2062.png)

También podemos darle atributos al elemento

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2063.png)

# Clases

Se puedes también agregar, anidar o modificar clases

Se peude acceder mediante la propiedad classList

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2064.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2065.png)

## Agregar una clase

Habiendo definido el elemento, podemos agregar una clase de la siguiente manera

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2066.png)

Si añadimos propiedades a esa clase en el archivo css, el primer elemento de clase topping tendrá color verde en el texto

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2067.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2068.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2069.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2070.png)

## Verificar si una cadena existe

Con el metodo contains, podemos validar si una clase existe en la lista de clases

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2071.png)

Su salida será booleana

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2072.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2073.png)

## Eliminar una clase

Se hace con el método remove

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2074.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2075.png)

# Crear un elemento en DOM

Desde JS se puede crear un elemento desde cero. Esto es muy útil cuando los usuarios interactúan con la página o la aplicación.  Lo primero que debemos hacer es crear un elemento nuevo de la siguiente manera. Primero debemos crear una variable que nos sirva de referencia para que al crear el nuevo elmento, que debe ser del mismo tipo que la referencia, el sistema sepa cómo debe crearlo.

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2076.png)

## Agregar un Elemento

Para esto vamos a usar el método .append. Que nos permite crear un nuevo nodo en la lista. 

Primero, vamos a definir la clase dle nuevo elemento y el texto que debe contener. Para este caso, será de clase topping y fondo marrón. Adicional a esto su texto será ‘Queso Extra’

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2077.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2078.png)

## Remover un Elemento

Para eliminar un elemento, solamente lo llamamos y con el método remove lo eliminamos, de la siguiente manera

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2079.png)

# Recorrer el DOM

Si queremos obtener el elemento padre de un elemento, primero creamos una variable con elemento, y con el método .parentElement podemos conocer su elemento padre

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2080.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2081.png)

También con el método children podremos conocer lo elementos hijos de un elemento

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2082.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2083.png)

Tambien hay más elementos que nos permitirán concoer los nodos, padres, hijos y hermanos tales como parentElement y parentNode, children, firstChild y firstElementChild, lastChild y lastElementChild, nextSibling y nextElementSibling, previousSiblign y previousElementSibling. Recuerda que se pueden encadenar estos métodos

# Eventos del DOM

Es algo que ocurre en el sitio web como resultado de interacción con el usuario o por otra causa como cambios en el estado del dispositivo o de la ventana. Por ejemplo Click o presionar una tecla del techado, cambios del tamaño de la ventana. Otros son por ejemplo arrastrar una imagen. Con dispositivos touch pueden ser tocar arrastrar y muchisisimos más. Los más comunes son los del cursor y los del teclado

# Conceptos Importantes

- target (blanco): Es el elemento con el que el ususrio puede interactuar, puede ser un botón o una imagen. Este le indica al navegador que algo ocurrió
- Trigger: Es desencadenar, es la acción que desencadena la interacción con el target
- Event handler: Es una función que se ejecuta cuando ocurre un evento

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2084.png)

- Event Listener:  Es la conexión para asociar un evento en un elemento con una función específica

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2085.png)

# Eventos en HTML

Para crear eventos, hay atributos que nos representan distintos eventos

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2086.png)

Para este caso, onclick es el atributo que nos dice que en el dado caso que se haga click en este elemento se ejecute la función mostratrClic. Entonces en JS debemos definir la función mostrarClic

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2087.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2088.png)

Podemos personalizar la salida en la consola con esta dunción definida en el atributo. Vamos a definir que la función mostrarClic muestre el nombre del topping de la siguiente manera

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2089.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2090.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2091.png)

# .addEventListener

Esto es mucho más práctico que lo que hace el atributo onClick. Ya que solo lo hacemos desde el archivo javaScript. Primero creamos una constante con el elemento con el que vamos a trabajar y definimos la función que debe realizarse. Luego debemos crear una conexión entre estos dos. Esto lo hacemos llamando al elemento seguido por el método addElementListener. Este método llama dos parámetro, el detonante (que para este caso es un click) y la función que debe realizar

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2092.png)

Estos eventos se representan como un objeto en la consol

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2093.png)

dentro de la función, por medio de notación de punto, poder que se imprima cualquier propiedad de este objeto

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2094.png)

Definamos una función que nos haga esto con todos los toppings

Definidmos el conjunto toppings, llamandolo del html por su clase. Luego, definimos la función mostrar clic definido en el parámetro topping. Esta funcion nos va a mostrar el texto del elemento, es decir el nomsbre del topping. Y finalmente hacermos una función for of. Esta itera en todos los elementos de un grupo. En este caso itera en todos los topping del grupo toppings (definido al inicio)

En este ciclo for, agregaremos un listener que lo detona un click y ejecuta la función mostrarClic cuando ocurra

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2095.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2096.png)

La función también puede definirse como una función flecha dentro del ciclo

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2097.png)

# Proyecto: Colores Aleatorios

Este proyecto será una página que muestre un color en hexadecimal y al hacer click en un botón, este cambiará el color de manera aleatoria. EL fondo de la página deberá ser del mismo color que se muestra en texto

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2098.png)

## HTML

Vamos a definir el cuerpo del archivo html. Usamos la abreviatura Emmet para que nos de una referencia y vamos agregando lo que necesitemos. Cambiamos el idioma y creamos en la carpeta del proyecto los archivos de estilo y js

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2099.png)

- Head: Acá, partiendo de lo que nos da la abreviatura Emmet, agregamos el título de la página, relacionamos el archivo css y ponemos un favicon

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20100.png)

- Body: Le damos una clase “centrar-flex” al body. Luego creamos un div, un párrafo y un botón. Para el div, le damos clase “centrar-flex” y le ponemos como id contenedor. Para párrafo, le ponemos de id color y como texto un color aleatorio en hexadecimal. Y para el botón, le ponemos como id “boton-color” y como texto Cambiar Color. Finalmente, fuera del div, relacionamos el archivo js

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20101.png)

## CSS

- Estilos Generales: Se define como estilo general, luego las características del body y la clase .centrar-flex

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20102.png)

- Contenedor: Flex wrap establece que si es necesario usar mas de una línea, puede que las palabras se vean en dos renglones. Flex direction establece que una sea debajo de otra.

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20103.png)

- Texto

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20104.png)

- Boton: User-select none es para que el ususrio no pueda seleccionar el texto del botón .Cursor es para que cuando el usuario esté con el cursor sobre el botón, este sea una manita. Transition-duration es el tiempo que tarda la transición de boton no seleccionado a seleccionado. El hover, son las propiedades del botón seleccionado.

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20105.png)

## JavaScript

Primero vamos a llamar al DOM los elementos con los que vamos a trabajar. Puntualmente son el recto del color y el botón

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20106.png)

Ahora vamos a definir una función que escriba aleatoriamente el nombre de un color hexadecimal

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20107.png)

Y una función que actualice el texto del color y su color sea el mismo del texto

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20108.png)

Y ahora los ligamos por medio del listener, que sea detonado por el clic del usuario en el botón y que accione la función de actualizar texto y color

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20109.png)

Resultado

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%2098.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20110.png)

# Proyecto Colores RGB

Este proyecto será una pagina que contiene 3 sliders, uno para cada color RGB. A medida que se mueva el slider, cambiará el valor de cada color y debe mostrarse el valor que cambió y actualizar el color de fondo de la página

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20111.png)

## HTML

Creamos la estructura de la página. Vamos a definir el cuerpo del archivo html. Usamos la abreviatura Emmet para que nos de una referencia y vamos agregando lo que necesitemos. Cambiamos el idioma y creamos en la carpeta del proyecto los archivos de estilo y js

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20112.png)

- Head: Usamos la abreviatura Emmet para la estructura inicial. También referenciamos el archivo de estilo style y definimos el favicon y lo relacionamos

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20113.png)

- Body: Creamos un div de clase contenedor-principal, dentro de este otro div de clase contenedor interno. Dentro de este, irán 3 divs correspondientes a los selectores de color. Cada uno de ellos será de clase color, tendrán una etiqueta con su nombre y un input de tipo range (slider) con sus valores de referencia como se muestra en la imagen (Dentro de esos valores de referencia vamos a poner un valor inicial que correspondrá al valor inicial del color cuando la página se inicie). Finalmente un p que mostrará el valor numérico del color. Finalmente linkeamos el archivo .js ya creado

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20114.png)

## CSS

- Estilos Generales. Acá definimos el mismo valor inicial definido en el html en el color de fondo

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20115.png)

- Contenedores

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20116.png)

- Colores RGB:

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20117.png)

- Etiquetas

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20118.png)

## JavaScript

Primero vamos a llamar desde el html las variables que vamos a necesitar en el programa.

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20119.png)

Luego actualizamos el texto de los párrafos p con el valor del slider

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20120.png)

Creamos una función que actualice el color según los valores del slider

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20121.png)

Finalmente, enlazamos la interacción del usuario al mover el slider con los valores del texto y con el color de fondo. El listener se activará con el detonante change y la función interna será definida mediante la obtención del valor del slider (target) y colocando ese valor como texto en los párrafos y como valor numérico del color en RGB.

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20122.png)

# Proyecto Citas Aleatorias

Para este proyecto vamos a hacer esta página que cuando uno le de click, cambie aleatroaimente de cita y de autor

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20123.png)

## HTML

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20124.png)

## CSS

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20125.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20126.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20127.png)

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20128.png)

## JavaScript

Ternemos dos archivos .jd el que contiene las citas y el funcional

- Citas

```jsx
let citas = [
    {
      'autor': 'Albert Einstein',
      'texto': 'No poseo talentos especiales. Solo soy apasionadamente curioso.'
    },
    {
      'autor': 'Anónimo',
      'texto': 'Semanas de programación te pueden ahorrar horas de planeación.'
    },
    {
      'autor': 'Alan Kay',
      'texto': 'La mejor forma de predecir el futuro es inventarlo.'
    },
    {
      'autor': 'Amelia Earhart',
      'texto': 'Lo más dificil es tomar la decisión de actuar. El resto es simplemente tenacidad.'
    },
    {
      'autor': 'Aristotle',
      'texto': 'La calidad no es un acto, es un hábito.'
    },
    {
      'autor': 'Benjamin Franklin',
      'texto': 'Dímelo y lo olvidaré. Enséñamelo y lo recordaré. Involúcrame y lo aprenderé.'
    },
    {
      'autor': 'Charles R. Swindoll',
      'texto': 'La vida es 10% lo que te ocurre y 90% cómo reaccionas.'
    },
    {
      'autor': 'Jane Goodall',
      'texto': 'Lo que haces hace una diferencia. Y debes decidir si qué tipo de diferencia quieres hacer.'
    },
    {
      'autor': 'John Muir',
      'texto': 'El poder de la imaginación nos hace infinitos.'
    },
    {
      'autor': 'Mark Twain',
      'texto': 'Los dos días más importantes de tu vida son el día que naciste y el día que descubres por qué.'
    }
  ];
```

- Funcional

```jsx
// Seleccionar los elementos HTML.
let botonElem = document.getElementById('boton-cambiar-cita');
let citaElem = document.getElementById('cita');
let autorElem = document.getElementById('autor');

// Para generar indices aleatorios.
function generarEnteroAleatorio(minimo, maximo) {
  minimo = Math.ceil(minimo);
  maximo = Math.floor(maximo);
  // Incluye el minimo pero no el maximo.
  return Math.floor(Math.random() * (maximo - minimo) + minimo);
}

// Seleccionar una cita aleatoria.
function cambiarCita() {
  let indiceAleatorio = generarEnteroAleatorio(0, citas.length);
  citaElem.textContent = `"${citas[indiceAleatorio].texto}"`;
  autorElem.textContent = citas[indiceAleatorio].autor;
}

// Para seleccionar una cita de forma aleatoria
// cuando se inicia la aplicacion.
let indiceAleatorio = generarEnteroAleatorio(0, citas.length);
cambiarCita();

// Para cambiar la cita al hacer click en el boton.
botonElem.addEventListener('click', cambiarCita);
```

# Proyecto Cronómetro

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20129.png)

## HTML

```html
<!DOCTYPE html>
<html lang="es">
        <head>
            <meta charset="UTF-8">
            <meta http-equvi="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <link rel="stylesheet" href="style.css">
            <link rel="icon" type="image/png" href="imagenes/favicon.png">
            <link rel="preconnect" href="https://fonts.googleapis.com">
            <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
            <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.1/font/bootstrap-icons.css">
            <link href="https://fonts.googleapis.com/css2?family=Courgette&family=Noto+Sans+Thai:wght@500&display=swap" rel="stylesheet">
            <title>Mi Cronómetro</title>
        </head>
        <body>
          <main class = contendedor-principal>
            <div id = "cronometro">00:00:00</div>
            <div class = "contenedor-botones">
                <button id="boton-inicio-pausa" class = "boton iniciar">
                    <i class="bi bi-play-fill"></i>
                </button>
                <button id = "boton-reiniciar" class = "boton">
                    <i class="bi bi-arrow-repeat"></i>
                </button>
            </div>            
          </main>    
            <script src="app.js"></script>
        </body>
</html>
```

## CSS

```css
/* Estilos Generales*/

*{
    margin: 0;
    padding: 0;    
}

body {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: url(imagenes/fondo.jpeg) no-repeat center center/cover;

}

/* Contenedores */

.contendedor-principal{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    width: 80vh;
    max-width: 600px;
    min-height: 350px;
    background-color: white;
    border: 3px solid black;
    font-family: Arial, Helvetica, sans-serif;
}

.contenedor-botones {
    padding: 20px;
}

#cronometro {
    width: 100%;
    font-size: 80px;
    font-weight: bold;
    user-select: none;
    font-family: 'Noto Sans Thai', sans-serif;
}

.boton {
    width: 80px;
    height: 80px;
    font-size: 50px;
    margin: 10px;
    padding: 10px;
    cursor: pointer;
}

#boton-inicio-pausa.iniciar,
#boton-inicio-pausa.iniciar i {
    background-color: #08e008;

}

#boton-inicio-pausa.pausar,
#boton-inicio-pausa.pausar i {
    background-color: #ffdc00;

}

#boton-reiniciar {
    background-color: red;
}
```

## JS

```jsx
// Seleccionar los botones.
const botonInicioPausa = document.querySelector('#boton-inicio-pausa');
const botonReiniciar = document.querySelector('#boton-reiniciar');

// Variables para almacenar los segundos, minutos y horas.
let [segundos, minutos, horas] = [0, 0, 0];

// Variables para almacenar el intervalo de tiempo que debe
// transcurrir para actualizar el cronometro y el estado 
// del cronometro.
let intervaloDeTiempo;
let estadoCronometro = 'pausado'; // Dos estados posibles: 'pausado' o 'andando'.

// Actualizar el cronometro.
function actualizarCronometro() {
  segundos++;

  if (segundos / 60 === 1) {
    segundos = 0;
    minutos++;

    if (minutos / 60 === 1) {
      minutos = 0;
      horas++;
    }
  }

  // Agregar un cero a la izquierda si es necesario.
  const segundosConFormato = asignarFormato(segundos);
  const minutosConFormato = asignarFormato(minutos);
  const horasConFormato = asignarFormato(horas);

  // Actualizar el contenido del cronometro.
  const cronometro = document.getElementById('cronometro');
  cronometro.innerText = `${horasConFormato}:${minutosConFormato}:${segundosConFormato}`;
}

// Agregar un cero a la izquierda si se necesita.
function asignarFormato(unidadDeTiempo) {
  return unidadDeTiempo < 10 ? '0' + unidadDeTiempo : unidadDeTiempo;
}

botonInicioPausa.addEventListener('click', function() {
  if (estadoCronometro === 'pausado') {
    // LLamar a la funcion cronometro cada 1000 milisegundos.
    intervaloDeTiempo = window.setInterval(actualizarCronometro, 1000);
    // Si el cronometro esta pausado, se muestra la flecha >
    // y se debe cambiar a || porque va a iniciar.
    document.getElementById('boton-inicio-pausa').innerHTML = `<i class="bi bi-pause" id="boton-inicio-pausa"></i>`;
    botonInicioPausa.classList.remove('iniciar');
    botonInicioPausa.classList.add('pausar');
    // Actualizar el estado del cronometro.
    estadoCronometro = 'andando';
  } else {
    // Detener el cronometro al eliminar el intervalo de tiempo 
    // usado para llamar a la funcion actualizarCronometro().
    window.clearInterval(intervaloDeTiempo);
    // Actualizar los botones y el estado del cronometro.
    document.getElementById('boton-inicio-pausa').innerHTML = `<i class="bi bi-play-fill" id="boton-inicio-pausa"></i>`;
    botonInicioPausa.classList.remove('pausar');
    botonInicioPausa.classList.add('iniciar');
    estadoCronometro = 'pausado';
  }
});

// Reiniciar el cronometro eliminando el intervalo de tiempo,
// reiniciando los segundos, minutos y horas, y actualizando
// el estado del cronometro y de los botones.
botonReiniciar.addEventListener('click', function() {
  // Eliminar el intervalo.
  window.clearInterval(intervaloDeTiempo);

  // Segundos, minutos y horas.
  segundos = 0;
  minutos = 0;
  horas = 0;
  document.getElementById('cronometro').innerHTML = '00:00:00';

  // Botones.
  document.getElementById('boton-inicio-pausa').innerHTML = `<i class="bi bi-play-fill" id="inicio"></i>`;
  botonInicioPausa.classList.remove('pausar');
  botonInicioPausa.classList.add('iniciar');

  // Estado.
  estadoCronometro = 'pausado';
});
```

# Proyecto Lista de Tareas

![Untitled](JS%20Manipulacio%CC%81n%20DOM%20a6bc7304ad8442afaddb528350b74023/Untitled%20130.png)

## HTML

```html
<!DOCTYPE html>
<html lang="es">
        <head>
            <meta charset="UTF-8">
            <meta http-equvi="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <link rel="stylesheet" href="style.css">
            <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.3/font/bootstrap-icons.css">
            <link rel="icon" type="image/png" href="imagenes/faviconcl.png">
            <link rel="preconnect" href="https://fonts.googleapis.com">
            <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
            <link href="https://fonts.googleapis.com/css2?family=Courgette&family=Noto+Sans+Thai:wght@500&family=Roboto:wght@500&display=swap" rel="stylesheet">
            <title>Mi Lista de Tareas</title>
        </head>
        <body>
          <div>
            <div class="contenedor">
                <h1>Mis Tareas</h1>
                <input id="ingresar-tarea">
                <button type="submit">Crear Tarea</button>
                <div id="lista-de-tareas">
                  <!-- Tareas -->
                </div>
            </div>
          </div>   
            <script src="app.js"></script>
        </body>
</html>
```

## CSS

```css
/* Estilos generales */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto', sans-serif;
  }
  
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    padding: 40px 0;
    text-align: center;
    background: url(imagenes/fondo.jpg) no-repeat center center/ cover;
  }
  
  /* Contenedor principal */
  
  .contenedor {
    width: 700px;
    min-height: 500px;
    background-color: white;
    padding: 40px;
    border: 5px solid black;
    border-radius: 20px;
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    align-items: center;
  }
  
  /* Titulo */
  
  h1 {
    font-size: 50px;
    font-weight: bold;
  }
  
  /* Ingresar texto */
  
  input {
    width: 80%;
    height: 50px;
    font-size: 25px;
    margin: 20px;
    padding: 10px;
    border: 4px solid #404040;
    border-radius: 10px;
  }
  
  /* Boton */
  
  button {
    width: 150px;
    height: 60px;
    padding: 10px;
    color: white;
    background-color: #1312a8;
    font-size: 22px;
    border-radius: 20px;
    border: 0px solid black;
    cursor: pointer;
    user-select: none;
  }
  
  /* Lista de tareas */
  
  #lista-de-tareas {
    width: 80%;
    margin-top: 20px;
  }
  
  /* Tareas individuales */
  
  .tarea {
    width: 100%;
    min-height: 70px;
    font-size: 25px;
    padding: 10px;
    margin-top: 10px;
    color: white;
    background-color: #407ba6;
    border: 2px solid black;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    text-align: left;
  }
  
  /* Estilo para tarea completada */
  
  .tarea.completada {
    text-decoration: line-through;
    background-color: black;
    border: none;
  }
  
  .tarea p {
    max-width: 350px;
  }
  
  /* Iconos */
  
  i {
    margin: 5px;
    padding: 10px;
    cursor: pointer;
  }
  
  .icono-completar {
    color: rgb(0, 255, 0);
  }
  
  .icono-eliminar {
    color: rgb(255, 255, 255);
  }
  
  .icono-completar:hover,
  .icono-eliminar:hover {
    background-color: rgba(255, 255, 255, 0.523);
  }
```

## JS

```jsx
// Seleccionar los elementos HMTL.
const input = document.getElementById('ingresar-tarea');
const boton = document.querySelector('button');
const listaDeTareas = document.getElementById('lista-de-tareas');

boton.addEventListener('click', agregarTarea);
input.addEventListener('keydown', (e) => {
  if (e.key == 'Enter') {
    agregarTarea();
  }
});

// Crear y agreagar una tarea a la lista de tareas
// en el DOM.
function agregarTarea() {
  if (input.value) {
    // Crear tarea.
    let tareaNueva = document.createElement('div');
    tareaNueva.classList.add('tarea');
  
    // Texto ingresado por el usuario.
    let texto = document.createElement('p');
    texto.innerText = input.value;
    tareaNueva.appendChild(texto);
  
    // Crear y agregar contenedor de los iconos
    let iconos = document.createElement('div');
    iconos.classList.add('iconos'); 
    tareaNueva.appendChild(iconos);
  
    // Crear y agregar iconos.
    let completar = document.createElement('i');
    completar.classList.add('bi', 'bi-check-circle-fill', 'icono-completar');
    completar.addEventListener('click', completarTarea);
  
    let eliminar = document.createElement('i');
    eliminar.classList.add('bi', 'bi-trash3-fill', 'icono-eliminar');
    eliminar.addEventListener('click', eliminarTarea);
  
    iconos.append(completar, eliminar);
  
    // Agregar la tarea a la lista.
    listaDeTareas.appendChild(tareaNueva);
  } else {
    alert('Por favor ingresa una tarea.');
  }
}

// Marcar una tarea como completada.
function completarTarea(e) {
  let tarea = e.target.parentNode.parentNode;
  tarea.classList.toggle('completada');
}

// Eliminar una tarea del DOM.
function eliminarTarea(e) {
  let tarea = e.target.parentNode.parentNode;
  tarea.remove();
}
```