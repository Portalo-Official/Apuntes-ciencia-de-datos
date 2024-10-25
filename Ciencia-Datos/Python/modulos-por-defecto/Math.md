
# Introducción

El módulo `math` en Python proporciona acceso a muchas funciones matemáticas comunes, como operaciones trigonométricas, exponenciales y logaritmos, junto con algunas funciones de redondeo y manipulación de números. Este módulo es muy útil para realizar cálculos numéricos precisos y trabajar con datos matemáticos.

# Métodos Comunes

### Valor Absoluto

- `fabs( x ): float`  
  Devuelve el valor absoluto de `x`, siempre como un número flotante, incluso si `x` es un entero.

  ```python
  import math
  print(math.fabs(-3.14))  # Salida: 3.14
```

### Máximo común divisor

- `gcd( x, y ): int`
	Devuelve el máximo común divisor (MCD) de los enteros `x` y `y`.

```python
import math
print(math.gcd(60, 48))  # Salida: 12
```
### Redondeo hacia abajo

- floor(x): z --> Valor entero más grande que es **menor o igual** a x

### Redondeo hacia arriba

- ceil(x): z --> Valor entero mas pequeño  x

