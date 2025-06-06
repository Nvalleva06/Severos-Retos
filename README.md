# Severos-Retos (Reto 5)

### 1 Área y volumen de una esfera

```python
import math

def Calcular_volumen_esfera(r: float) -> float:
    return (4/3) * math.pi * r**3

def Calcular_area_esfera(r: float) -> float:
    return 4 * math.pi * r**2

if __name__ == "__main__":

    r = float(input("Ingrese el radio de la esfera: "))

    area = Calcular_area_esfera(r)
    volumen = Calcular_volumen_esfera(r)

    print("El área de la esfera es " + str(area))
    print("El volumen de la esfera es " + str(volumen))
```

### 2 Una función matemática para calcular el área y el perimetro de la figura

```python
def Calcular_perimetro(a:float, b:float, r:float) -> float:
    perimetro_figura = 2*a + 2*b + 2*(2*math.pi*r)
    return perimetro_figura

def Calcular_area(a:float, b:float, r:float) -> float:
    area_figura = a*b + 2*(math.pi * r**2)
    return area_figura

if __name__ == "__main__":
    a = float(input("Ingrese la altura del rectangulo "))
    b = float(input("Ingrese la base del rectangulo "))
    r = float(input("Ingrese el radio de los circulos "))
    
    Area = Calcular_area(a, b, r)
    Perimetro = Calcular_perimetro(a, b, r)
    
    print("El perímetro es " +str(Perimetro))
    print("El área es " +str(Area))
```

### 3 Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.
```python
import math

def Calcular_kilos_de_carne (N:int, M:int, K:int) -> int:
    Kilos_de_carne = N*6 + M*7 + K
    return Kilos_de_carne


if __name__ == "__main__":
    
    N = int(input("Ingrese la cantidad de gallinas "))
    M = int(input("Ingrese la cantidad de gallos "))
    K = int(input("Ingrese la cantidad de pollitos "))
    
    Peso_de_la_carne = Calcular_kilos_de_carne(N, M, K)
    print("Tienes " +str(Peso_de_la_carne) +" kilos de carne")
```

### 4 Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.
```python
def calcular_prestamo(P:float, i:float, n:int) -> float:
    return P * (1 + i)**n

if __name__ == "__main__":
    P = float(input("Ingrese el monto del préstamo: "))
    i = float(input("Ingrese la tasa de interés mensual (por ejemplo. 0.03 para 3%): "))
    n = int(input("Ingrese la cantidad de meses: "))
    
    total = calcular_prestamo(P, i, n)
    print("El valor final del préstamo es: " + str(total) + " unidades monetarias")
```

### 5 Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:
- El promedio
- El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
- La potencia del mayor número elevado al menor número
- La raíz cúbica del menor número
```python
import math

def calcular_promedio(a, b, c, d, e):
    total = a+b+c+d+e
    return total / 5

def promedio_multiplicativo(a, b, c, d, e):
    producto = a*b*c*d*e
    return producto**(1 / 5)

def potencia_mayor_menor(a, b, c, d, e):
    mayor = a
    menor = a

    if b > mayor: mayor = b
    if c > mayor: mayor = c
    if d > mayor: mayor = d
    if e > mayor: mayor = e

    if b < menor: menor = b
    if c < menor: menor = c
    if d < menor: menor = d
    if e < menor: menor = e

    return mayor ** menor

def raiz_cubica_menor(a, b, c, d, e):
    menor = a

    if b < menor: menor = b
    if c < menor: menor = c
    if d < menor: menor = d
    if e < menor: menor = e

    return menor**(1 / 3)

if __name__ == "__main__":
    a = float(input("Ingrese el número 1: "))
    b = float(input("Ingrese el número 2: "))
    c = float(input("Ingrese el número 3: "))
    d = float(input("Ingrese el número 4: "))
    e = float(input("Ingrese el número 5: "))
```

### 6 Consultar qué es y cómo funciona pip en python.

pip es el administrador de paquetes de Python. Se utiliza para instalar, actualizar y desinstalar paquetes o librerías de terceros desde PyPI, el índice oficial de paquetes de Python.

### 7 Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos
| Módulo           | Uso principal                    | Cómo instalar                |
| ---------------- | -------------------------------- | ---------------------------- |
| `requests`       | Hacer peticiones HTTP            | `pip install requests`       |
| `numpy`          | Cálculos numéricos y matrices    | `pip install numpy`          |
| `pandas`         | Análisis y manipulación de datos | `pip install pandas`         |
| `matplotlib`     | Gráficas y visualizaciones       | `pip install matplotlib`     |
| `scikit-learn`   | Machine Learning                 | `pip install scikit-learn`   |
| `flask`          | Microframework web               | `pip install flask`          |
| `django`         | Framework web completo           | `pip install django`         |
| `openpyxl`       | Manipular archivos Excel         | `pip install openpyxl`       |
| `beautifulsoup4` | Scraping de páginas web          | `pip install beautifulsoup4` |
