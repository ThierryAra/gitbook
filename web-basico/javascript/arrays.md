# Arrays

Arrays, também conhecidos como vetores, são estruturas que armazenam dados de maneira sequencial. Além disso, seus elementos são indexados. Sua grande utilidade é armazenar, em uma única variável, uma série de elementos. 

### Declaração

Em javascript, arrays são **dinâmicos.** Não é necessário alocar memória previamente, ou re-alocar memória para inserir ou deletar elementos. Para declarar um array, basta utilizar `[]`

```javascript
let elements = []
```

Também é possível inicializar um array com dados:

```javascript
let elements = ['a', 3, 85, 'maria']
```

Outra propriedade interessante dos arrays em javascript é a sua capacidade de armazenar elementos de diferentes tipos. É possível ter números e strings em um mesmo array. Além disso, arrays são indexados a partir do número 0. 

### Acessando elementos via index

É possível acessar o **i**ésimo elemento de um array por meio de seu índice `[i]`.

```javascript
let my_array = ['b', 'c']
let first_element = my_array[0]

console.log(first_element)
// Imprime 'b'
```

### Acessando elementos via valor

O operador `indexOf` permite encontrar a primeira ocorrência de um valor em um array, retornando -1 caso não haja ocorrência. 

```javascript
let my_array = ['a', 'b', 'c', 'd']
c_index = my_array.indexOf('c')

console.log(c_index)
// Imprime 2
```

### Modificando elementos via index

Ao contrário das Strings, **arrays são mutáveis em Javascript**. Isso significa que é possível acessar e modificar seus elementos. 

```javascript
let my_array = ['b', 'c']
my_array[1] = 'k'

console.log(my_array)
// Imprime ['b', 'k']
```

### Inserindo elementos

É possível inserir elementos em um array utilizando:

* `push`: Insere no **final**
* `unshift`: Insere no **início**

```javascript
let my_array = ['b', 'c']

my_array.push('z')
my_array.unshift('a')

console.log(my_array)

// Imprime ["a", "b", "c", "Z"]
```

### Propriedade "length"

Retorna o tamanho do array. 

```javascript
let my_array = ['a', 'b', 'c']
console.log(my_array.length)
// Imprime 3
```

### Removendo elementos

É possível remover elementos utilizando:

* `pop`: Remove o **último elemento** e o retorna

```javascript
let my_array = ['a', 'b', 'c']
my_array.pop()

console.log(my_array) // Imprime ['a', 'b']
```

* `shift`: Remove o **primeiro elemento** e o retorna

```javascript
let my_array = ['a', 'b', 'c']
my_array.shift()

console.log(my_array)
// Imprime ['b', 'c']
```

### Gerando sub-arrays

O operador `slice(start, end)` corta o array a partir de um índice inicial e final. 

```javascript
let my_array = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']
sub_array = my_array.slice(2, 5)

console.log(sub_array)
// Imprime ["c", "d", "e"]
```

É importante relembrar que arrays são indexados a partir do 0.

Além disso, `slice` inclui o elemento `start`, mas não o `end`. No exemplo acima, `my_array[2] ("c")`, é incluído, mas`my_array[5] ("f")`, não. 

### Iterando sobre arrays

Uma das maiores utilidades do comando `for` é iterar sobre arrays. É possível utilizar o tamanho do array, `my_array.length`, para isto: 

```javascript
let my_array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]

for (let i = 0; i < my_array.length; i++) {
    my_array[i] = my_array[i]**2    
}

console.log(my_array)
// Imprime [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144]
```

Entretanto, como é uma tarefa muito comum **iterar sobre arrays e manipular o elemento atual da iteração**, foi criado um método para isto, o `for(elem of array)`: 

```javascript
let my_array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]

for (number of my_array){
    number = number**2
}

console.log(my_array)
```

Importante notar que essa maneira de iterar sobre  vários elementos não é uma exclusividade da definição do array, além de existir algumas outra maneiras de iterar sobre um array \(como a função map\).

