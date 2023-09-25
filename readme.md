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

Se puedes también agregar, anidar o modificar clases

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

Desde JS se puede crear un elemento desde cero. Esto es muy útil cuando los usuarios interactúan con la página o la aplicación.  Lo primero que debemos hacer es crear un elemento nuevo de la siguiente manera. Primero debemos crear una variable que nos sirva de referencia para que al crear el nuevo elmento, que debe ser del mismo tipo que la referencia, el sistema sepa cómo debe crearlo.

![Untitled](img/Untitled%2076.png)

## Agregar un Elemento

Para esto vamos a usar el método .append. Que nos permite crear un nuevo nodo en la lista. 

Primero, vamos a definir la clase dle nuevo elemento y el texto que debe contener. Para este caso, será de clase topping y fondo marrón. Adicional a esto su texto será ‘Queso Extra’

![Untitled](img/Untitled%2077.png)

![Untitled](img/Untitled%2078.png)

## Remover un Elemento

Para eliminar un elemento, solamente lo llamamos y con el método remove lo eliminamos, de la siguiente manera

![Untitled](img/Untitled%2079.png)

# Recorrer el DOM

Si queremos obtener el elemento padre de un elemento, primero creamos una variable con elemento, y con el método .parentElement podemos conocer su elemento padre

![Untitled](img/Untitled%2080.png)

![Untitled](img/Untitled%2081.png)

También con el método children podremos conocer lo elementos hijos de un elemento

![Untitled](img/Untitled%2082.png)

![Untitled](img/Untitled%2083.png)

Tambien hay más elementos que nos permitirán concoer los nodos, padres, hijos y hermanos tales como parentElement y parentNode, children, firstChild y firstElementChild, lastChild y lastElementChild, nextSibling y nextElementSibling, previousSiblign y previousElementSibling. Recuerda que se pueden encadenar estos métodos

# Eventos del DOM

Es algo que ocurre en el sitio web como resultado de interacción con el usuario o por otra causa como cambios en el estado del dispositivo o de la ventana. Por ejemplo Click o presionar una tecla del techado, cambios del tamaño de la ventana. Otros son por ejemplo arrastrar una imagen. Con dispositivos touch pueden ser tocar arrastrar y muchisisimos más. Los más comunes son los del cursor y los del teclado

# Conceptos Importantes

- target (blanco): Es el elemento con el que el ususrio puede interactuar, puede ser un botón o una imagen. Este le indica al navegador que algo ocurrió
- Trigger: Es desencadenar, es la acción que desencadena la interacción con el target
- Event handler: Es una función que se ejecuta cuando ocurre un evento

![Untitled](img/Untitled%2084.png)

- Event Listener:  Es la conexión para asociar un evento en un elemento con una función específica

![Untitled](img/Untitled%2085.png)

# Eventos en HTML

Para crear eventos, hay atributos que nos representan distintos eventos

![Untitled](img/Untitled%2086.png)

Para este caso, onclick es el atributo que nos dice que en el dado caso que se haga click en este elemento se ejecute la función mostratrClic. Entonces en JS debemos definir la función mostrarClic

![Untitled](img/Untitled%2087.png)

![Untitled](img/Untitled%2088.png)

Podemos personalizar la salida en la consola con esta dunción definida en el atributo. Vamos a definir que la función mostrarClic muestre el nombre del topping de la siguiente manera

![Untitled](img/Untitled%2089.png)

![Untitled](img/Untitled%2090.png)

![Untitled](img/Untitled%2091.png)

# .addEventListener

Esto es mucho más práctico que lo que hace el atributo onClick. Ya que solo lo hacemos desde el archivo javaScript. Primero creamos una constante con el elemento con el que vamos a trabajar y definimos la función que debe realizarse. Luego debemos crear una conexión entre estos dos. Esto lo hacemos llamando al elemento seguido por el método addElementListener. Este método llama dos parámetro, el detonante (que para este caso es un click) y la función que debe realizar

![Untitled](img/Untitled%2092.png)

Estos eventos se representan como un objeto en la consol

![Untitled](img/Untitled%2093.png)

dentro de la función, por medio de notación de punto, poder que se imprima cualquier propiedad de este objeto

![Untitled](img/Untitled%2094.png)

Definamos una función que nos haga esto con todos los toppings

Definidmos el conjunto toppings, llamandolo del html por su clase. Luego, definimos la función mostrar clic definido en el parámetro topping. Esta funcion nos va a mostrar el texto del elemento, es decir el nomsbre del topping. Y finalmente hacermos una función for of. Esta itera en todos los elementos de un grupo. En este caso itera en todos los topping del grupo toppings (definido al inicio)

En este ciclo for, agregaremos un listener que lo detona un click y ejecuta la función mostrarClic cuando ocurra

![Untitled](img/Untitled%2095.png)

![Untitled](img/Untitled%2096.png)

La función también puede definirse como una función flecha dentro del ciclo

![Untitled](img/Untitled%2097.png)

# Proyecto: Colores Aleatorios

Este proyecto será una página que muestre un color en hexadecimal y al hacer click en un botón, este cambiará el color de manera aleatoria. EL fondo de la página deberá ser del mismo color que se muestra en texto

![Untitled](img/Untitled%2098.png)

## HTML

Vamos a definir el cuerpo del archivo html. Usamos la abreviatura Emmet para que nos de una referencia y vamos agregando lo que necesitemos. Cambiamos el idioma y creamos en la carpeta del proyecto los archivos de estilo y js

![Untitled](img/Untitled%2099.png)

- Head: Acá, partiendo de lo que nos da la abreviatura Emmet, agregamos el título de la página, relacionamos el archivo css y ponemos un favicon

![Untitled](img/Untitled%20100.png)

- Body: Le damos una clase “centrar-flex” al body. Luego creamos un div, un párrafo y un botón. Para el div, le damos clase “centrar-flex” y le ponemos como id contenedor. Para párrafo, le ponemos de id color y como texto un color aleatorio en hexadecimal. Y para el botón, le ponemos como id “boton-color” y como texto Cambiar Color. Finalmente, fuera del div, relacionamos el archivo js

![Untitled](img/Untitled%20101.png)

## CSS

- Estilos Generales: Se define como estilo general, luego las características del body y la clase .centrar-flex

![Untitled](img/Untitled%20102.png)

- Contenedor: Flex wrap establece que si es necesario usar mas de una línea, puede que las palabras se vean en dos renglones. Flex direction establece que una sea debajo de otra.

![Untitled](img/Untitled%20103.png)

- Texto

![Untitled](img/Untitled%20104.png)

- Boton: User-select none es para que el ususrio no pueda seleccionar el texto del botón .Cursor es para que cuando el usuario esté con el cursor sobre el botón, este sea una manita. Transition-duration es el tiempo que tarda la transición de boton no seleccionado a seleccionado. El hover, son las propiedades del botón seleccionado.

![Untitled](img/Untitled%20105.png)

## JavaScript

Primero vamos a llamar al DOM los elementos con los que vamos a trabajar. Puntualmente son el recto del color y el botón

![Untitled](img/Untitled%20106.png)

Ahora vamos a definir una función que escriba aleatoriamente el nombre de un color hexadecimal

![Untitled](img/Untitled%20107.png)

Y una función que actualice el texto del color y su color sea el mismo del texto

![Untitled](img/Untitled%20108.png)

Y ahora los ligamos por medio del listener, que sea detonado por el clic del usuario en el botón y que accione la función de actualizar texto y color

![Untitled](img/Untitled%20109.png)

Resultado

![Untitled](img/Untitled%2098.png)

![Untitled](img/Untitled%20110.png)

# Proyecto Colores RGB

Este proyecto será una pagina que contiene 3 sliders, uno para cada color RGB. A medida que se mueva el slider, cambiará el valor de cada color y debe mostrarse el valor que cambió y actualizar el color de fondo de la página

![Untitled](img/Untitled%20111.png)

## HTML

Creamos la estructura de la página. Vamos a definir el cuerpo del archivo html. Usamos la abreviatura Emmet para que nos de una referencia y vamos agregando lo que necesitemos. Cambiamos el idioma y creamos en la carpeta del proyecto los archivos de estilo y js

![Untitled](img/Untitled%20112.png)

- Head: Usamos la abreviatura Emmet para la estructura inicial. También referenciamos el archivo de estilo style y definimos el favicon y lo relacionamos

![Untitled](img/Untitled%20113.png)

- Body: Creamos un div de clase contenedor-principal, dentro de este otro div de clase contenedor interno. Dentro de este, irán 3 divs correspondientes a los selectores de color. Cada uno de ellos será de clase color, tendrán una etiqueta con su nombre y un input de tipo range (slider) con sus valores de referencia como se muestra en la imagen (Dentro de esos valores de referencia vamos a poner un valor inicial que correspondrá al valor inicial del color cuando la página se inicie). Finalmente un p que mostrará el valor numérico del color. Finalmente linkeamos el archivo .js ya creado

![Untitled](img/Untitled%20114.png)

## CSS

- Estilos Generales. Acá definimos el mismo valor inicial definido en el html en el color de fondo

![Untitled](img/Untitled%20115.png)

- Contenedores

![Untitled](img/Untitled%20116.png)

- Colores RGB:

![Untitled](img/Untitled%20117.png)

- Etiquetas

![Untitled](img/Untitled%20118.png)

## JavaScript

Primero vamos a llamar desde el html las variables que vamos a necesitar en el programa.

![Untitled](img/Untitled%20119.png)

Luego actualizamos el texto de los párrafos p con el valor del slider

![Untitled](img/Untitled%20120.png)

Creamos una función que actualice el color según los valores del slider

![Untitled](img/Untitled%20121.png)

Finalmente, enlazamos la interacción del usuario al mover el slider con los valores del texto y con el color de fondo. El listener se activará con el detonante change y la función interna será definida mediante la obtención del valor del slider (target) y colocando ese valor como texto en los párrafos y como valor numérico del color en RGB.

![Untitled](img/Untitled%20122.png)