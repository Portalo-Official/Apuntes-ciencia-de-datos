# Introrucción

NumPy es una biblioteca esencial en Python para la manipulación de arrays y cálculos matemáticos, ampliamente utilizada en ciencia de datos debido a su velocidad y versatilidad. A continuación, te explico los métodos más usados en **NumPy**, organizados por categorías clave para ciencia de datos.

### **Resumen de métodos comunes en NumPy para ciencia de datos**

| Método              | Parámetros Principales  | Función                                                                  |
| ------------------- | ----------------------- | ------------------------------------------------------------------------ |
| `np.array`          | `data`, `dtype`, `copy` | Crea un arreglo numpy a partir de datos (listas, tuplas, etc.).          |
| `np.zeros`          | `shape`, `dtype`        | Crea un arreglo lleno de ceros.                                          |
| `np.ones`           | `shape`, `dtype`        | Crea un arreglo lleno de unos.                                           |
| `np.arange`         | `start`, `stop`, `step` | Crea un arreglo con valores igualmente espaciados dentro de un rango.    |
| `np.linspace`       | `start`, `stop`, `num`  | Genera números igualmente espaciados en un intervalo cerrado.            |
| `np.random.rand`    | `shape`                 | Genera valores aleatorios uniformes entre 0 y 1.                         |
| `np.random.randn`   | `shape`                 | Genera valores aleatorios con distribución normal (media 0, varianza 1). |
| `np.random.randint` | `low`, `high`, `size`   | Genera números enteros aleatorios en un rango.                           |
| `np.mean`           | `axis`                  | Calcula el promedio de un arreglo.                                       |
| `np.median`         | `axis`                  | Calcula la mediana de un arreglo.                                        |
| `np.std`            | `axis`                  | Calcula la desviación estándar de un arreglo.                            |
| `np.dot`            | `a`, `b`                | Calcula el producto escalar o matricial.                                 |
| `np.reshape`        | `newshape`              | Cambia la forma de un arreglo sin alterar sus datos.                     |
| `np.transpose`      | `axes`                  | Invierte o intercambia ejes en un arreglo.                               |
#### 1. **`np.array`**

- **Función**: Crea un arreglo de NumPy a partir de datos existentes.
- **Ejemplo**:
    
    ```python
	data = [1, 2, 3, 4] 
	arr = np.array(data) 
	print(arr)  # Output: [1 2 3 4]`
	```
    

#### 2. **`np.zeros`**

- **Función**: Crea un arreglo lleno de ceros.
- **Ejemplo**:
    
    ```python
    arr = np.zeros((2, 3)) 
    print(arr)   
    # Output:  
    # [[0. 0. 0.] 
    #  [0. 0. 0.]]
	```
    

#### 3. **`np.ones`**

- **Función**: Crea un arreglo lleno de unos.
- **Ejemplo**:
    
```python
    arr = np.ones((3, 2)) 
    print(arr) 
    # Output: 
    # [[1. 1.] 
    #  [1. 1.] 
    #  [1. 1.]]
```

#### 4. **`np.arange`**

- **Función**: Crea un arreglo con valores igualmente espaciados dentro de un rango.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.arange(0, 10, 2) print(arr)  # Output: [0 2 4 6 8]`
    

#### 5. **`np.linspace`**

- **Función**: Genera números igualmente espaciados en un intervalo cerrado.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.linspace(0, 1, 5) print(arr)  # Output: [0.   0.25 0.5  0.75 1.  ]`
    

#### 6. **`np.random.rand`**

- **Función**: Genera valores aleatorios uniformes entre 0 y 1.
- **Ejemplo**:
    
```python
arr = np.random.rand(2, 3) 
print(arr)
```

#### 7. **`np.random.randn`**

- **Función**: Genera valores aleatorios con distribución normal.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.random.randn(3) print(arr)`
    

#### 8. **`np.random.randint`**

- **Función**: Genera números enteros aleatorios en un rango.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.random.randint(1, 10, size=(2, 2)) print(arr)`
    

#### 9. **`np.mean`**

- **Función**: Calcula el promedio de los valores en un arreglo.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.array([1, 2, 3, 4, 5]) print(np.mean(arr))  # Output: 3.0`
    

#### 10. **`np.median`**

- **Función**: Calcula la mediana de los valores en un arreglo.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.array([1, 3, 2, 5, 4]) print(np.median(arr))  # Output: 3.0`
    

#### 11. **`np.std`**

- **Función**: Calcula la desviación estándar.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.array([1, 2, 3, 4, 5]) print(np.std(arr))  # Output: 1.4142135623730951`
    

#### 12. **`np.dot`**

- **Función**: Calcula el producto escalar o matricial.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `a = np.array([1, 2]) b = np.array([3, 4]) print(np.dot(a, b))  # Output: 11`
    

#### 13. **`np.reshape`**

- **Función**: Cambia la forma de un arreglo sin alterar sus datos.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.arange(6) reshaped = arr.reshape((2, 3)) print(reshaped)`
    

#### 14. **`np.transpose`**

- **Función**: Invierte o intercambia ejes en un arreglo.
- **Ejemplo**:
    
    python
    
    Copiar código
    
    `arr = np.array([[1, 2], [3, 4]]) print(np.transpose(arr))`