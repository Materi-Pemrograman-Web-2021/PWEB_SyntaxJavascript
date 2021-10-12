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

Pada tipe data ini juga bisa diterapkan perhitungan aritmatika seperti,
| Operasi | Penjelasan |
--- | --- |
| + | Plus |
| - | Minus |
| / | Divide |
| * | Multiply |
| % | Mod |
| `x`++ | Gunakan `x` dulu, baru tambah 1 |
| ++`x` | tambah 1 dulu, baru gunakan `x` |

### 3. BigInt
Pada JavaScript, tipe data “Number” hanya mencakup nilai dari -(253 - 1) hingga (253 - 1).

Untuk nilai di luar Number, kita bisa menggunakan tipe BigInt. Untuk membedakan tipe BigInt dan Number, tambahkan karakter n di akhir angka.

```js
const bigNumber = 1234567890123456789012345678901234567890n;
const Numbers = 1234567890123456789012345678901234567890;

console.log(bigNumber);
console.log(Numbers);

/* output
1234567890123456789012345678901234567890n
1.2345678901234568e+39
*/
```

### 4. Strings
Berupa teks

```js
let halo = "halo bang";
```

### 5. Boolean
Berupa true or false

```js
let x = true;
let y = false;
```

### 6. Null
Tipe berikutnya adalah null. Serupa dengan undefined, namun null perlu diinisialisasikan pada variabel.

```js
let ini_null = null;
```
### 7. Symbol
Symbol adalah tipe data baru yang dikenalkan pada ES6. Tipe data Symbol digunakan untuk menunjukkan identifier yang unik. Ketika membuat Symbol, kita bisa memberikan deskripsi atau nama symbol seperti ini:

```js
const id = Symbol("id");

console.log(id);

/* output
Symbol(id)
*/
```

Symbol disebut sebagai identifier yang unik karena meskipun kita membuat dua variabel symbol dengan nama atau deskripsi yang sama, kedua nilainya tetap dianggap berbeda. 

```js
const id1 = Symbol("id");
const id2 = Symbol("id");

console.log(id1 == id2);

/* output
false
*/
```
