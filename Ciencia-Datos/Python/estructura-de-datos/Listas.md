

# Listas en Python

## 1. Formas de inicializar una lista en Python

- **Lista vacía**:
  ```python
  lista_vacia = []
```

- **Lista con elementos**:
  ```python
  lista = [1, 2, 3, 4, 5]
  ```

- **Inicializar con un número repetido** (usando multiplicación de listas):
  ```python
  lista = [0] * 5  # Resultado: [0, 0, 0, 0, 0]
  ```

- **Inicializar a partir de una función o expresión**:
  - Usando **comprensión de listas**:
    ```python
    lista = [i for i in range(5)]  # Resultado: [0, 1, 2, 3, 4]
    ```

- **Inicializar una lista con el constructor `list()`**:
  ```python
  lista = list()  # Crea una lista vacía
  lista = list("Python")  # Crea una lista a partir de un string: ['P', 'y', 't', 'h', 'o', 'n']
  ```

## 2. Rellenar una lista con `range()` o un bucle

- **Usando `range()`**: 
  ```python
  lista = list(range(10))  # Resultado: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
  ```

- **Usando un bucle `for`**:
  ```python
  lista = []
  for i in range(5):
      lista.append(i)
  print(lista)  # Resultado: [0, 1, 2, 3, 4]
  ```

## 3. Añadir elementos o colecciones a una lista

- **Añadir un elemento** con `append()`:
  ```python
  lista = [1, 2, 3]
  lista.append(4)  # Añade el 4 al final
  print(lista)  # Resultado: [1, 2, 3, 4]
  ```

- **Añadir varios elementos** con `extend()`:
  ```python
  lista = [1, 2, 3]
  lista.extend([4, 5, 6])  # Añade todos los elementos de la lista
  print(lista)  # Resultado: [1, 2, 3, 4, 5, 6]
  ```

- **Añadir un elemento en una posición específica** con `insert()`:
  ```python
  lista = [1, 2, 3]
  lista.insert(1, "a")  # Inserta "a" en la posición 1
  print(lista)  # Resultado: [1, 'a', 2, 3]
  ```

## 4. Eliminar elementos de una lista

- **Eliminar un elemento por su valor** con `remove()`:
  ```python
  lista = [1, 2, 3, 4]
  lista.remove(3)  # Elimina el primer elemento que coincida con el valor 3
  print(lista)  # Resultado: [1, 2, 4]
  ```

- **Eliminar un elemento por su índice** con `pop()`:
  ```python
  lista = [1, 2, 3, 4]
  lista.pop(1)  # Elimina el elemento en la posición 1 (el 2)
  print(lista)  # Resultado: [1, 3, 4]
  ```

- **Eliminar todos los elementos de una lista** con `clear()`:
  ```python
  lista = [1, 2, 3]
  lista.clear()  # Vacía la lista
  print(lista)  # Resultado: []
  ```

### Eliminación concurrente:
Cuando necesitas eliminar elementos durante la iteración, es mejor hacerlo en una **copia de la lista**, para evitar problemas de modificación del tamaño de la lista mientras se itera.

```python
lista = [1, 2, 3, 4, 5, 6]
lista_copy = lista[:]  # Hacer una copia superficial

for num in lista_copy:
    if num % 2 == 0:  # Eliminar números pares
        lista.remove(num)

print(lista)  # Resultado: [1, 3, 5]
```

## 5. Funciones útiles como `sum()`, `max()`, etc.

- **`sum()`**: Devuelve la suma de todos los elementos en una lista de números.
  ```python
  lista = [1, 2, 3, 4]
  print(sum(lista))  # Resultado: 10
  ```

- **`max()`**: Devuelve el valor máximo de una lista.
  ```python
  lista = [1, 2, 3, 4]
  print(max(lista))  # Resultado: 4
  ```

- **`min()`**: Devuelve el valor mínimo de una lista.
  ```python
  lista = [1, 2, 3, 4]
  print(min(lista))  # Resultado: 1
  ```

- **`len()`**: Devuelve la longitud de la lista (el número de elementos).
  ```python
  lista = [1, 2, 3, 4]
  print(len(lista))  # Resultado: 4
  ```

- **`sorted()`**: Devuelve una lista ordenada (no modifica la lista original).
  ```python
  lista = [4, 2, 3, 1]
  print(sorted(lista))  # Resultado: [1, 2, 3, 4]
  ```

## 6. Filtrado de listas usando programación avanzada

- **Filtrar con comprensión de listas**:
  ```python
  lista = [1, 2, 3, 4, 5, 6, 7, 8]
  pares = [x for x in lista if x % 2 == 0]  # Filtra solo los números pares
  print(pares)  # Resultado: [2, 4, 6, 8]
  ```

- **Filtrar con `filter()`**:
  ```python
  lista = [1, 2, 3, 4, 5, 6, 7, 8]
  pares = list(filter(lambda x: x % 2 == 0, lista))  # Usa una lambda para filtrar pares
  print(pares)  # Resultado: [2, 4, 6, 8]
  ```

- **Filtrar por varias condiciones** (con programación avanzada):
  ```python
  lista = [1, 2, 3, 4, 5, 6, 7, 8]
  pares_mayores_que_cuatro = [x for x in lista if x % 2 == 0 and x > 4]
  print(pares_mayores_que_cuatro)  # Resultado: [6, 8]
  ```

## Resumen:

- **Inicialización**: Puedes inicializar listas de muchas maneras, como usando corchetes (`[]`), `list()`, o comprensiones de listas.
- **Generación de listas**: Puedes usar `range()` o bucles para llenar listas de manera eficiente.
- **Agregar elementos**: Con `append()`, `extend()`, e `insert()` puedes añadir elementos a la lista.
- **Eliminar elementos**: Puedes usar `remove()`, `pop()`, o `clear()` para eliminar elementos.
- **Funciones útiles**: Funciones como `sum()`, `max()`, `min()`, `len()` y `sorted()` son muy comunes y útiles para trabajar con listas.
- **Filtrado avanzado**: Puedes filtrar listas usando **comprensión de listas** o la función `filter()` para escribir código conciso y poderoso.
