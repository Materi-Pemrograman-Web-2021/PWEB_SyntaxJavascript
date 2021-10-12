# Struktur Data

## Object
Object berisi pasangan key dan value yang juga dikenal dengan property.

```js
let object = {
    key1: "value1", 
    key2: "value2", 
    key3: "value3",
}
```
Berikut contoh akses nilai dari properties object

```js
const user = {
    name: "Prima",
    age: 19,
    isMarried: true,
};

console.log(`Halo, nama saya ${user.name} dan umurku ${user.age} tahun`);

// output: Halo, nama saya Prima dan umurku 19 tahun
```

Selain menggunakan `dot` operator, kita bisa pakai `bracket` operator juga

```js
console.log(user["name"]);

// output: Prima
```

Sekarang kita coba memodifikasi object yang sudah ada.

```js
const user = {
    name: "Prima",
    age: 19,
    isMarried: true,
};

user.name = "Prima Update";
console.log(user);

/* output:
 {
     name: "Prima Update",
     age: 19,
     isMarried: true,
 }
*/
```

Kita juga bisa hapus property pada object.

```js
const user = {
    name: "Prima Update",
    age: 19,
    isMarried: true,
};

delete user.name;
console.log(user);

/* output:
 {     
     age: 19,
     isMarried: true,
 }
*/
```

## Array
Array merupakan tipe data yang dapat mengelompokkan lebih dari satu nilai dan menempatkannya dalam satu variabel.

Kalau di JS, satu array bisa macam2 tipe nya

```js
let myArray = ["Ini Teks", 42.5, 22, true, "Hehe"];
console.log(myArray);
console.log(myArray[0]);
console.log("Panjang Array: " + myArray.length);

/* output:
    ["Ini Teks", 42.5, 22, true, "Hehe"]
    Ini Teks
    Panjang Array: 5
*/
```

Untuk modifikasi array, ada beberapa method yang bisa digunakan seperti `push()`, `pop()`, dll. Detailnya bisa dilihat [disini](https://www.freecodecamp.org/news/manipulating-arrays-in-javascript/)

Contoh method `push()`

```js
let myArray = ["Ini Teks", 42.5, 22, true, "Hehe"];

myArray.push(69);
console.log(myArray);

/* output:
    ["Ini Teks", 42.5, 22, true, "Hehe", 69]
*/
```

## Spread Operator
Menyebarkan nilai array atau lebih tepatnya iterable object menjadi beberapa elemen

```js
const foods = ["babi", "nasi", "dadar jagung", "sup"];
    
console.log(foods);
console.log(...foods);
    
/* output
["babi", "nasi", "dadar jagung", "sup"]
babi nasi dadar jagung sup

*/
```

Karenaaaaa.....

```js
console.log(...foods);
```

itu sama dengan

```js
console.log(foods[0],foods[1],foods[2],foods[3],);
```

## Destructuring Object & Array
Intinya, destructuring itu bisa "mengekspos" isi dari sesuatu (object/array) menjadi variable sendiri.

```js
// array destructuring, sesuai index
const nama = ["lorem", "ipsum"]
const [namaDepan, namaBelakang] = nama

console.log(namaDepan) // "lorem"
console.log(namaBelakang) // "ipsum"

// object destructuring, sesuai key
const mhs = {
  nama = "foobar",
  password = "verysecret123andri"
  nrp = "05311940000003"
}

const {nama, nrp} = mhs;

console.log(nama) // "foobar"
console.log(nrp) // "05311940000003"


// rest assignment
const halo = ["halo", "bandung", "ibu", "kota"]
const [kata_pertama, ...kata_sisanya] = halo

console.log(kata_pertama) // "halo" -- string
console.log(kata_sisanya) // ["bandung", "ibu", "kota"] -- array

```

## Map
Mirip object. Bedanya, Map memperbolehkan key dengan tipe data apa pun, dibandingkan Object yang hanya mengizinkan key bertipe String atau Symbol.

Contoh deklarasi Map

```js
const myMap = new Map([
    ['1', 'a String key'],
    [1, 'a number key'],
    [true, true]
]);
```

Pada Map juga terdapat beberapa method untuk modifikasi Map, seperti `.size`, `.get()`, dll. Bisa cari sendiri :)

## Set
Mirip array. Bedanya, data di dalam Set juga bersifat unik dan tidak ada duplikasi. Dan juga tidak memiliki indeks

```js
const numberSet = new Set([1, 4, 6, 4, 1]);

console.log(numberSet);

/* output
Set(3) { 1, 4, 6 }
*/

numberSet.add(69);
numberSet.add(1);

console.log(numberSet);

/* output
Set(3) { 1, 4, 6, 69}
*/

```
