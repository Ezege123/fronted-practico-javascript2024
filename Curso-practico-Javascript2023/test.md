## Respuestas al test de JavaScript

Recuerda que estas respuestas (o al menos la mayoria) NO SON ABSOLUTAS es completamente valido (en la mayoria de casos) si tienes otras respuestas, recuerda que podemos discutirlo en la seccion de comentarios del curso. :D


## Variables y operaciones

## 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve? 

Cajitas (espacios en memoria) donde podemos guardar informacion (dependiendo de los tipos y estructuras de datos que soporte nuestro lenguaje).

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

Declarar es cuando le decimos a JavaScript que vamos a crear una variable con el nombre tal. Mientras que inicializar (o reinicializar) es asignarle un valor a esa variable

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
- ¿Cuál operador me permite sumar o concatenar?

El operador que nos permite sumar o concatenar es +, este operador nos permite sumar numeros cuando lo usamos con numeros, pero cuando los strings, lo que hace es unir (concatenar, asi se dice) ambos strings.

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre: string
- Apellido: string
- Nombre de usuario en Platzi: string (@fulanito)
- Edad: number
- Correo electrónico: string (lala@gmail.com)
- Mayor de edad: boolean
- Dinero ahorrado: number
- Deudas: number

## 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```
let nombre = 'Juan David';
let apellido = 'Castro Gallego';
let username = 'juandc';
let edad = 19;
let mail = 'juanito@alcachofa.xyz';
let esMayorDeEdad = true;
let dineroAhorrado = 1000;
let deudas = 100;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```
let nombreCompleto = nombre + apellido;
let dineroReal; dineroAhorrado - deudas;
```



### Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?

las funciones nos permiten encapsular (guardar) bloques de codigo para reutilizarlos y ejecutarlos en el futuro.

- ¿Cuándo me sirve usar una función en mi código?

Nos sirve cuando tenemos variables o bloques de codigo muy parecidos que podemos encapsular para reutilizar mas de una vez en el futuro.

tambien nos sirve para ordenar y mejorar la legibilidad de nuestro codigo.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

las funciones reciben parametros cuando las creamos. y les enviamos argumentos cuando las ejecutamos.

### 2️⃣ Convierte el siguiente código en una función, pero cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es" + completeName + ", pero prefiero que me digas" + nickname + ".");
```

```
function nombreCompleto(name, lastName) {
    return name + ' ' + lastName
}

function saludo(name, lastname, username) {
const completeName = nombreCompleto(name, lastname);
    
console.log("Mi nombre es" + completeName + ", pero prefiero que me digas" + username + ".");
}
```


## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?

son la forma en que ejecutamos un bloque de codigo u otro dependiendo de alguna condicion o validacion

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

IF (else y else if), Switch
El condicional if (con el se y else if) nos premite hacer validaciones completamente distintos (si asi queremos) en cada validacion o condicional. En cambio, en el switch todos los cases se comparan con la misma variable o condicion que definimos en el switch.

- ¿Puedo combinar funciones y condicionales?

Si, las funciones pueden encapsular cualquier bloque de codigo, incluyendo condicionales.

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertDuo":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```

```
if (tipoDeSuscripcion == 'Free') {
    console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion == 'Basic') {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if(tipoDeSuscripcion == 'Expert') {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion == 'ExpertDuo') {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏


## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

¿Qué es un ciclo?

la forma de ejecutar un bloque de codigo hasta que se cumpla cierta condicion.

¿Qué tipos de ciclos existen en JavaScript?

while, for, do while y for.

¿Qué es un ciclo infinito y por qué es un problema?

Es cuando la validacion de nuestros condicionales nunca se cumple y termina toteando (da;ando) la aplicacion (e.j cuando el navegador ya no puede mas de tanta ejecucion de ese bloque de codigo).

¿Puedo mezclar ciclos y condicionales?

Si, aunque los ciclos son una especie de condicionales , nada mas nos impide agregar mas condicionales dentro del ciclo.

2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

while (i < 5) {
    console.log("El valor de i es: " + i); 
     i++;
}

for (let i = 10; i >=2; i--) {
    console.log("El valor de i es: " + i);
}

while (i >= 2) {
    console.log("El valor de i es: " + i);
     i--;
}
```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```js
while (respuesta !='4') {
    let pregunta = prompt ('¿Cuanto es 2 + 2?')
    respuesta = pregunta;
}
```


## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?

Es una lista de elementos.

```
const array = [1, 'jaja', true, false, {nombre: 'lala', edad:3});
```

- ¿Qué es un objeto?

Es una lista de elementos PERO cada elemento tiene un nombre clave.

```
const obj = {
    nombre: 'fulanito',
    edad: 3,
    comidasFavoritas: ['Pollo frito', 'vegetales'],
};
```

- ¿Cuándo es mejor usar objetos o arrays?

Arrays cuando lo que haremos en un elemento es lo mismo que en todos los demas (la regla se puede cumplir). Mientras que un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

Si. los arrays pueden guardar objetos. y los objetos guardar arrays entre sus propiedades.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```
function  imprimirPrimerElementoArray(arr) {
    console.log(arr[0])
}
```

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```
function imprimirElementoPorElemento(arr) {
 for (let i = 0; i < arr.length; i++) {
    console.log(arr[i])
 }
}
```

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```

```