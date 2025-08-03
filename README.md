## Introducción a los algoritmos con JS

JavaScript fue creado por Brendan Eich en 1995 para Netscape Navigator.es un lenguaje de programación de alto nivel, interpretado y orientado a objetos. Principalmente utilizado en el desarrollo web, permite agregar interactividad, dinamismo y manipulación de contenido en las páginas. Ejecutado en el navegador del usuario, JavaScript se utiliza para controlar el comportamiento de los elementos HTML, responder a eventos del usuario y comunicarse con servidores, lo que contribuye a crear experiencias web interactivas y atractivas.

Facilidad de Desarrollo Web: Es fundamental en el desarrollo web, proporcionando la capacidad de interactuar con el DOM (Document Object Model) para crear experiencias interactivas en los navegadores.

## TIPOS DE DATOS EN JAVASCRIPT

En JavaScript existen dos tipos de datos: 

- [**Objetos](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Working_with_objects):** En ****[JavaScript](https://developer.mozilla.org/es/docs/Glossary/JavaScript) sigue un paradigma simple basado en objetos, donde un objeto es una colección de propiedades, y cada propiedad se asocia con una clave y un valor. Estas propiedades pueden contener funciones, que se denominan métodos cuando están asociadas a objetos.
- [**Primitivos**](https://developer.mozilla.org/es/docs/Glossary/Primitive): En [JavaScript](https://developer.mozilla.org/es/docs/Glossary/JavaScript), un **primitivo** (valor primitivo, tipo de dato primitivo) son datos que no son un [objeto](https://developer.mozilla.org/es/docs/Glossary/Object) y no tienen [métodos](https://developer.mozilla.org/es/docs/Glossary/Method). Hay 6 tipos de datos primitivos:
    - **Booleano:** Representa valores de verdad, **`true`** o **`false`**.
    - **Null:** Representa la ausencia intencional de cualquier objeto o valor.
    - **No Definido (Undefined):** Representa la falta de un valor asignado, especialmente cuando una variable no se ha inicializado.
    - **Número:** Representa valores numéricos, ya sean enteros o de punto flotante.
    - **Cadena (String):** Representa una secuencia de caracteres.
    - **Símbolo:** Introducido en ECMAScript 6, representa un identificador único e inmutable.

## Comentarios de JavaScript
``
// Comentario de una sola línea

/*
comentarios de varias líneas
linea uno
linea dos
linea tres
 */
``
## VARIABLES EN JAVASCRIPT

let a = 5;
let b = 6;
let c = a + b;

<aside>
🧐 *La `var`palabra clave se utilizó en todo el código JavaScript desde 1995 hasta 2015.*

*Las palabras clave `let`y `const`se agregaron a JavaScript en 2015.*

*La `var`palabra clave sólo debe usarse en código escrito para navegadores más antiguos*

</aside>

<aside>
🙄 **¿Cuándo utilizar** `var` **,** `let` **o** `const` **?**

1. Declarar siempre variables

2. Utiliza siempre `const` si el valor no debe cambiarse.

3. Utiliza siempre `const` si no se debe cambiar el tipo (matrices y objetos)

4. Solo usa `let` si no puedes usar `const` 

5. Utiliza `var` únicamente si DEBE admitir navegadores antiguos.

</aside>

## **Funciones de JavaScript**

Una función en JavaScript es esencialmente un conjunto de instrucciones organizadas para llevar a cabo una tarea específica. Estas instrucciones están encapsuladas en un bloque de código, que es un grupo de declaraciones entre llaves **`{}`**. Este bloque define las acciones que la función realizará cuando sea invocada.

Cuando algo invoca o llama a la función, el bloque de código asociado se ejecuta, llevando a cabo la tarea para la cual la función fue creada. Es como un paquete de acciones que se activa cuando se necesita realizar una operación específica. En resumen, una función no solo es un conjunto de instrucciones, sino que esas instrucciones están organizadas y encapsuladas en un bloque de código para una ejecución coherente.

## Sintaxis de funciones de JavaScript
Una función de JavaScript se define con la functionpalabra clave, seguida de un nombre , seguido de paréntesis () .
Los nombres de funciones pueden contener letras, dígitos, subrayados y signos de dólar (las mismas reglas que las variables).
Los paréntesis pueden incluir nombres de parámetros separados por comas:
( parámetro1, parámetro2,... )
El código a ejecutar, por la función, se coloca entre llaves: {}
## Invocación de función
El código dentro de la función se ejecutará cuando "algo" invoca 

`/ Definición de la función llamada "saludar"
function nombreEdad(nombre, edad) {
  // Bloque de código de la función
  console.log( nombre + "Tiene" +edad+ "años");
}

// Invocación de la función
nombreEdad("Juan", 30);
`
## Función Retorno

Cuando JavaScript encuentra una declaración **`return`**, la función se detiene de inmediato. Si la función fue llamada desde otra parte del código, JavaScript "retornará" a la ejecución justo después de la declaración que hizo la invocación.

```

function miFuncion(a, b) {
// Function returns the product of a and b

  return a + b;

}

const x = miFuncion(2, 1); 
console.log(x) // output 3
```

En términos más simples, imagina que la función es como un mensajero. Cuando encuentra la palabra **`return`**, entrega un mensaje y se va. Si alguien le pidió algo (invocó la función), el mensajero (JavaScript) vuelve al lugar desde el cual lo llamaron.

Las funciones comúnmente calculan algo llamado un **valor de retorno**. Este valor de retorno es como el mensaje que el mensajero trae de vuelta y se entrega a la "persona que llama" (la parte del código que invocó la función). Es como obtener un resultado después de realizar un cálculo.

#### JS avanzado

## Objetos en JavaScript

En JavaScript, los objetos son estructuras de datos fundamentales y versátiles que permiten almacenar y organizar información de manera estructurada. Un objeto en JavaScript puede contener propiedades y métodos, lo que le proporciona una capacidad de modelado rica y dinámica. Aquí hay algunas características clave de los objetos en JavaScript:

1. **Propiedades y Métodos:**
    - **Propiedades:** Los objetos pueden contener propiedades, que son pares clave-valor. Una propiedad tiene un nombre (clave) y un valor asociado.
    - **Métodos:** Los métodos son funciones almacenadas como propiedades en un objeto.
2. **Sintaxis de Notación de Objetos:**
    - Los objetos se definen utilizando la notación de llaves **`{}`**. Dentro de las llaves, se especifican las propiedades y sus valores, separados por comas.
    
    ```jsx
    let persona = {
      nombre: "Juan",
      edad: 25,
      decirHola: function() {
        console.log("Hola, soy " + this.nombre);
      }
    };
    ```
    
3. **Acceso a Propiedades:**
    - Puedes acceder a las propiedades de un objeto utilizando la notación de punto (**`objeto.propiedad`**) o la notación de corchetes (**`objeto['propiedad']`**).
    
    ```jsx
    console.log(persona.nombre);      // Imprime "Juan"
    console.log(persona['nombre']);   // Imprime "Juan"
    ```
    
4. **Métodos Abreviados (ES6):**
    - En ECMAScript 2015 (ES6) y versiones posteriores, puedes utilizar métodos abreviados de notación de objetos para definir métodos más concisamente.
    
    ```jsx
    let persona = {
      nombre: "Juan",
      edad: 25,
      decirHola() {
        console.log("Hola, soy " + this.nombre);
      }
    };
    ```
    
5. **Referencia por Valor:**
    - Los objetos se manejan por referencia en JavaScript, lo que significa que cuando asignas un objeto a una variable, estás asignando la referencia al objeto, no una copia del objeto.
6. **Dinámicos y Flexibles:**
    - Los objetos en JavaScript son dinámicos y flexibles. Puedes agregar o eliminar propiedades y métodos en tiempo de ejecución.
    

Los objetos en JavaScript son fundamentales para el desarrollo web y se utilizan ampliamente para modelar datos y comportamientos en aplicaciones. Pueden representar entidades del mundo real, como usuarios, productos, etc., y son una parte esencial del lenguaje.

## **Métodos para manipular Objetos:**

**1. Copia de Propiedades con Object.assign():**

```jsx
// Crear una copia del objeto persona
let copiaPersona = Object.assign({}, persona);

console.log(copiaPersona);
// Resultado: { nombre: "Juan", edad: 25, decirHola: [Function: decirHola] }
```

**2. Copia con Spread Operator (ES6+):**

```jsx
// Crear una copia del objeto persona usando el operador de propagación
let copiaPersona = { ...persona };

console.log(copiaPersona);
// Resultado: { nombre: "Juan", edad: 25, decirHola: [Function: decirHola] }
```

**3. Copia Profunda con JSON.parse() y JSON.stringify():**

```jsx
// Crear una copia profunda del objeto persona
let copiaProfundaPersona = JSON.parse(JSON.stringify(persona));

console.log(copiaProfundaPersona);
// Resultado: { nombre: "Juan", edad: 25 }
```

**4. Eliminar una Propiedad con `delete`:**

```jsx
// Eliminar la propiedad 'edad' del objeto persona
delete persona.edad;

console.log(persona);
// Resultado: { nombre: "Juan", decirHola: [Function: decirHola] }
```

Bucle for
Un bucle for es una estructura de control en programación que permite ejecutar un bloque de código repetidamente hasta que se cumple una condición especificada. Este bucle consta de cuatro partes principales:
Inicialización: Al principio, se establece una condición inicial (como let i = 0;), que actúa como el punto de partida.
Condición: Luego, hay una condición que se verifica antes de cada repetición (i < 5;). Mientras esta condición sea verdadera, el bucle continuará.
Iteración: Después de cada repetición, se realiza una acción (por ejemplo, i++ significa aumentar i en 1). Esto es como avanzar al siguiente paso o elemento.
bloque de código : Dentro de las llaves {...} está el código que se ejecuta repetidamente.
Aquí está la estructura básica:

for (let i = 0; i < 5; i++) {
  // Código a repetir
}

## Algunas características y conceptos clave sobre los arrays en JavaScript:

1. **Índices:**
    - Los índices en un array comienzan desde 0. Puedes acceder a un elemento utilizando su índice, por ejemplo, **`miArray[0]`** accederá al primer elemento.
2. **Longitud del Array:**
    - La propiedad **`length`** indica la cantidad de elementos en un array. Por ejemplo, **`miArray.length`** devolverá 5.
3. **Métodos de Array:**
    - JavaScript proporciona una variedad de métodos integrados para manipular arrays.
        
        ### **`forEach()` - Iteración sobre Elementos:**
        
        El método **`forEach()`** se utiliza para ejecutar una función para cada elemento del array.
        
        ```jsx
        let frutas = ["manzana", "banana", "uva"];
        
        frutas.forEach(function(fruta) {
          console.log(fruta);
        });
        
        // Imprime:
        // "manzana"
        // "banana"
        // "uva"
        ```
        
        ### **Uso de `for...of` para Iteración:**
        
        Además de **`forEach()`**, puedes utilizar un bucle **`for...of`** para iterar sobre los elementos de un array.
        
        ```jsx
        let frutas = ["manzana", "banana", "uva"];
        
        for (let fruta of frutas) {
          console.log(fruta);
        }
        
        // Imprime:
        // "manzana"
        // "banana"
        // "uva"
        
        ```
        
        **`map()`** 
        
        El método **`map()`** crea un nuevo array aplicando una función a cada elemento del array original.
        
        ```jsx
        let numeros = [1, 2, 3, 4];
        
        let duplicados = numeros.map(function(numero) {
          return numero * 2;
        });
        
        console.log(duplicados);  // Imprime [2, 4, 6, 8]
        ```
        
        ### **`filter()`**
        
        El método **`filter()`** crea un nuevo array con los elementos que pasan una condición específica.
        
        ```jsx
        let numeros = [1, 2, 3, 4, 5, 6];
        
        let impares = numeros.filter(function(numero) {
          return numero % 2 !== 0;
        });
        
        console.log(impares);  // Imprime [1, 3, 5]
        ```
        
        ### **`reduce()`**
        
        El método **`reduce()`** reduce el array a un solo valor aplicando una función acumulativa.
        
        ```jsx
        let numeros = [1, 2, 3, 4];
        
        let suma = numeros.reduce(function(acumulador, numero) {
          return acumulador + numero;
        }, 0);  // El segundo parámetro es el valor inicial del acumulador
        
        console.log(suma);  // Imprime 10
        ```
        
        ### **`slice()`**
        
        El método **`slice()`** devuelve un nuevo array con una porción del array original.
        
        ```jsx
        let frutas = ["manzana", "banana", "uva", "kiwi"];
        
        let primerasDosFrutas = frutas.slice(0, 2);
        
        console.log(primerasDosFrutas);  // Imprime ["manzana", "banana"]
        ```
        
        ### **`splice()`**
        
        El método **`splice()`** cambia el contenido de un array eliminando o reemplazando elementos.
        
        ```jsx
        let frutas = ["manzana", "banana", "uva", "kiwi"];
        
        // Eliminar dos elementos desde la posición 1
        frutas.splice(1, 2);
        
        console.log(frutas);  // Imprime ["manzana", "kiwi"]
        ```
        
        **Operador Spread (`...`)**
        
        El operador de propagación (**`...`**) se utiliza para copiar, concatenar o expandir arrays.
        
        ```jsx
        let numeros1 = [1, 2, 3];
        let numeros2 = [4, 5, 6];
        
        let numerosConcatenados = [...numeros1, ...numeros2];
        
        console.log(numerosConcatenados);  // Imprime [1, 2, 3, 4, 5, 6]
        ```
        
        ### **`push()`**
        
        El método **`push()`** se utiliza para agregar uno o más elementos al final de un array.
        
        ```jsx
        let frutas = ["manzana", "banana"];
        
        frutas.push("uva");
        
        console.log(frutas);  // Imprime ["manzana", "banana", "uva"]
        ```
        
        ### **`shift()`**
        
        El método **`shift()`** elimina el primer elemento de un array y devuelve ese elemento.
        
        ```jsx
        let frutas = ["manzana", "banana", "uva"];
        
        let primeraFruta = frutas.shift();
        
        console.log(primeraFruta);  // Imprime "manzana"
        console.log(frutas);  // Imprime ["banana", "uva"]
        ```
        
4. **Flexibilidad de Tipos:**
    - Los arrays en JavaScript pueden contener elementos de diferentes tipos, lo que los hace muy versátiles.

<aside>
🧐 Los arrays son una herramienta fundamental en la programación y se utilizan para almacenar y manipular colecciones de datos de manera eficiente.

</aside>

## **Tipos de operadores de JavaScript**

Existen diferentes tipos de operadores de JavaScript:

1. **Operadores aritméticos**
    
    Los operadores aritméticos se utilizan para realizar operaciones aritméticas con números:
    
    ```jsx
    let a = 2;
    let b = 3;
    let c = 4;
    let d = (a + b) * c;
    
    console.log(d)
    ```
    
    | Operador | Descripción | Ejemplo |
    | --- | --- | --- |
    | + | Suma | `let sum = a + b;` |
    | - | Resta | `let res = a - b;` |
    | * | Multiplicación | `let mult = a * b;` |
    | / | División | `let div = c / a;` |
    | % | Resto | `let resto = b % a;` |
    | ** | Exponenciación | `let exp = a ** b;` |
    | ++ | Incremento | `let x = 10; x++; let z = x;` |
    | -- | Decremento | `let x = 10; x--; let z = x;` |
    
    **Precedencia del operador**
    
    La precedencia de operadores describe el orden en el que se realizan las operaciones en una expresión aritmética.
    
    Como en las matemáticas escolares tradicionales, primero se hace la multiplicación.
    
    La multiplicación ( `*`) y la división ( `/`) tienen mayor **prioridad** que la suma ( `+`) y la resta ( `-`).
    
    Y (como en matemáticas escolares) la precedencia se puede cambiar usando paréntesis.
    
    Cuando se utilizan paréntesis, las operaciones dentro de los paréntesis se calculan primero:
    
    ```jsx
    let x = (2 + 2) * 3;
    ```
    
    Cuando muchas operaciones tienen la misma precedencia (como suma y resta o multiplicación y división), se calculan de izquierda a derecha:
    
    ```jsx
    let a = 10 + 2 - 3;
    let b = 10 / 2 * 3;
    ```
    
2. **Operadores de comparación**
    
    Los operadores de comparación se utilizan en declaraciones lógicas para determinar la igualdad o diferencia entre variables o valores.
    
    | Operador | Descripción | Ejemplo |
    | --- | --- | --- |
    | == | Igualdad | `x == y` |
    | === | Igualdad estricta | `x === y` |
    | != | Desigualdad | `x != y` |
    | !== | Desigualdad estricta | `x !== y` |
    | > | Mayor que | `x > y` |
    | < | Menor que | `x < y` |
    | >= | Mayor o igual que | `x >= y` |
    | <= | Menor o igual que | `x <= y` |
    
    **Comparación de String en JavaScript**
    
    Todos los operadores de comparación anteriores también se pueden utilizar en cadenas, comparándolas alfabéticamente:
    
    ```jsx
    let texto1 = "A";
    let texto2 = "B";
    let resultado = text1 > text2;
    ```
    
3. **Operadores de String**
    
    
    | Operador | Descripción | Ejemplo | Resultado |
    | --- | --- | --- | --- |
    | + | Concatenación de cadenas | "Hola" + " Mundo" | "Hola Mundo" |
    | += | Concatenación y asignación | let saludo = "Hola"; saludo += " Mundo"; | "Hola Mundo" |
4. **Operadores lógicos**
    
    
    | Operador | Descripción | Ejemplo | Resultado |
    | --- | --- | --- | --- |
    | && | AND lógico | (5 > 3) && (10 < 20) | true |
    | || | OR lógico | (5 > 3) || (10 > 20) | true |
    | ! | NOT lógico | !(5 > 3) | false |
5. **Operadores ternarios**
    
    Los operadores ternarios, también conocidos como operadores condicionales, son una forma concisa de expresar una operación condicional en una sola línea. Estos operadores toman tres operandos y se utilizan para evaluar una expresión que luego produce un resultado basado en una condición. El formato general de un operador ternario es:
    
    <aside>
    ❓ condición ? expresión_si_verdadero : expresión_si_falso;
    
    </aside>
    
    ```jsx
    let edad = 18;
    let mensaje = (edad >= 18) ? "Eres mayor de edad" : "Eres menor de edad";
    
    console.log(mensaje);  // "Eres mayor de edad"
    ```
    
6. **Operadores de tipo**
    
    
    | Operador | Descripción |
    | --- | --- |
    | typeof | Devuelve el tipo de una variable |
    | instanceof | Devuelve true si un objeto es una instancia de un tipo de objeto |

## refactorización

La refactorización en programación se refiere al proceso de modificar el código fuente de un programa sin cambiar su comportamiento externo. El objetivo principal de la refactorización es mejorar la estructura interna del código para que sea más fácil de entender, mantener y extender, sin afectar la funcionalidad del programa.

En el contexto de JavaScript u otros lenguajes de programación, la refactorización puede incluir una variedad de acciones, como reorganizar bloques de código, renombrar variables, funciones o clases, dividir funciones largas en funciones más pequeñas, eliminar código duplicado y aplicar patrones de diseño más eficientes.

Algunos principios clave de la refactorización incluyen:

1. **Mantenimiento de la Funcionalidad:**
    - La refactorización debe realizarse de manera que no introduzca errores en la funcionalidad del programa. Es crucial tener pruebas automatizadas para asegurarse de que el código refactorizado sigue funcionando correctamente.
2. **Incremental y Continua:**
    - La refactorización es un proceso continuo e incremental. En lugar de intentar refactorizar todo el código de una vez, es preferible realizar pequeñas refactorizaciones paso a paso.
3. **Legibilidad y Entendimiento:**
    - El objetivo final de la refactorización es mejorar la legibilidad y el entendimiento del código. Un código más claro facilita el mantenimiento, la colaboración y la detección de posibles errores.
4. **Eficiencia y Rendimiento:**
    - La refactorización también puede incluir mejoras en la eficiencia y el rendimiento del código. Esto puede involucrar la optimización de algoritmos o la eliminación de operaciones innecesarias.

- **REVISIÓN DE PUNTOS
CLAVE 1/3**
    - Las arreglos son un tipo de objeto en
    Javascript. Las matrices son una estructura de
    datos que contiene una lista de elementos.
    - La longitud y el tipo de arreglos Javascript no
    son fijos.
    - Cada elemento de una arreglos tiene una
    ubicación llamada índice. Podemos acceder a
    un elemento de la arreglo haciendo referencia a
    su índice.
    - Los índices de la arreglo siempre comienzan
    con 0, que apunta al primer elemento de la
    matriz.
- **REVISIÓN DE PUNTOS
CLAVE 2/3**
    - Ordenamiento es ordenar una lista de
    elementos.
    - Las arreglos en Javascript tienen una función
    de ordenamiento incorporada. La función de
    ordenamiento toma una función de
    comparación para ordenar elementos.
    - Los bucles For se utilizan para iterar a través
    de una secuencia/arreglo de tipos de datos u
    objetos. Su ejecución depende de una
    condición booleana (verdadera o falsa) - si la
    condición es verdadera, entonces el bucle
    continúa ejecutándose, pero si la condición es
    falsa, entonces el bucle se rompe.
- **REVISIÓN DE PUNTOS
CLAVE 3/3**
    - Un objeto es una colección de propiedades,
    definidas como un par clave-valor. Cada
    propiedad tiene una clave y un valor.
    - La refactorización de código es el proceso
    de reestructurar el código de computadora
    existente sin cambiar su comportamiento
    externo.
    - La refactorización está destinada a mejorar
    los atributos del código, como la
    mantenibilidad, la legibilidad y la eficiencia.

