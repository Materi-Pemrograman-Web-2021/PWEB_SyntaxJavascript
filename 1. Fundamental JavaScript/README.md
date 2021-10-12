# Fundamental JavaScript

##  Kode JavaScript Pertama

```js
console.log("Hello, World!");
```

## Comments

```js
// ini comments

// console.log("Hello, World!");
```

## Variable

Di JavaScript ada 3 cara mendeklarasikan variable, yaitu menggunakan keyword `var` , `let`, dan `const`

Pada versi ES6 dikenalkan `let` dan `const` untuk menggantikan `var` yang dinilai kontroversial dan rawan menimbulkan bug

```js
let nama = "Prima";
```

```js
const angka = 100;
console.log(angka);

z = 200;
console.log(z)

// TypeError: Assignment to constant variable
```

## Tipe Data

### 1. Undefined
Tipe data ini terbentuk ketika sebuah variabel tidak memiliki nilai.

```js
let angka;
console.log(type(angka));

// output: undefined
```
### 2. Numbers
Nilai dari tipe data number adalah angka.

```js
let angka1 = 10;
console.log(typeof(angka1))

// output: number

let angka2 = 17.25;
console.log(typeof(angka2))

// output: number
```
### 3. BigInt
### 4. Strings
### 5. Boolean
### 6. Null
### 7. Symbol
### 8. 
