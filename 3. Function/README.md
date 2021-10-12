# Function

## Declare Function


```js
// Function
function perkalian(a, b){
    return a*b
}

console.log(perkalian(6,9));
// output: 54


// Procedure
function halo(){
    console.log("Haloo Bang");
}

halo();
// output: Haloo Bang
```

## Function Parameter

Parameter bisa berupa Object
```js
const user = {
    id: 24,
    displayName: 'kren',
    fullName: 'Kylo Ren',
};

function introduce({displayName, fullName}) {
    console.log(`${displayName} is ${fullName}`);
}

introduce(user);

/* output

    kren is Kylo Ren

*/

```

Contoh default parameter
```js
function exponentsFormula(baseNumber, exponent = 2) {
    let result = baseNumber ** exponent;
    console.log(`${baseNumber}^${exponent} = ${result}`);
}

exponentsFormula(3);

/* output

    3^2 = 9

*/
```

Contoh parameter menggunakan spread operator (Rest Paramater)

```js
function sum(...numbers) {
    let result = 0;
    for (let number of numbers) {
        result += number;
    }
    return result;
}

console.log(sum(1, 2, 3, 4, 5));

/* output

    15

*/
```

## Arrow Function
fungsi didefinisikan menggunakan tanda panah atau fat arrow ( `=>` ). Tentunya penulisan arrow function ini akan lebih singkat.

Contoh tanpa Arrow Function
```js
// function declaration
function sayHello(greet) {
    console.log(`${greet}!`);
}
    
// function expression
const sayName = function (name) {
    console.log(`Nama saya ${name}`)
}
```

Contoh dengan Arrow Function
```js
// function expression
const sayHello = (greet) => {
    console.log(`${greet}!`)
}
    
const sayName = (name) => {
    console.log(`Nama saya ${name}`)
}
```

Contoh lain
```js
// Fungsi cuma 1 parameter
const sayName = name => {
    console.log(`Nama saya ${name}`)
}

// Fungsi tanpa parameter
const sayHello = () => {
    console.log("Selamat pagi semuanya!")
};
```

## Variable Scope
Basic lah. Intinya, yang diluar fungsi bisa dipakai dimana saja. Kalau didalam fungsi, itu bisa dipakai didalam fungsi saja

```js
let x = 420;

const iniFungsi = () => {
    let y = 69;
    console.log(x);
}

iniFungsi();
console.log(y);

/* output:

    420
    undefined

*/



```

## Closure
Lexical scope berarti pada sebuah fungsi bersarang, fungsi yang berada di dalam memiliki akses ke variabel di lingkup induknya.

```js
function init() {
    var name = 'Obi Wan';   // Variabel lokal di dalam scope fungsi init
    
    function greet() {      // Inner function, merupakan contoh closure
        console.log(`Halo, ${name}`);   // Memanggil variabel yang dideklarasikan di parent function
    }

    greet();
}

init();

/* output

    Halo, Obi Wan

 */
```

Harus hati-hati dalam menggunakan variable di JS. Karena di JS tidak ada _private method_

```js
let counter = 0;

let add = () => {
    return ++counter;
}

console.log(add());
console.log(add());
counter = 23;
console.log(add());

/* output

    1
    2
    24

 */
```

Pada contoh diatas `counter` bisa diakses dimana saja. Yang membuat tidak bagus untuk program, sebaiknya dihindari.
Langkah bagusnya adalah dibawah ini, yaitu memanfaatkan _Closure_

```js
let add = () => {
    let counter = 0;
    return () => {
        return ++counter;
    };
}

let addCounter = add();

console.log(addCounter());
console.log(addCounter());
counter = 23;
console.log(addCounter());


/* output

    1
    2
    3

 */
```

Nah, nilai counter tidak berubah kan...