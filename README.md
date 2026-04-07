# Python - Fundamentos

Este repositorio contiene apuntes y ejercicios básicos de programación en Python, incluyendo variables, estructuras de datos, operadores y condicionales.

Autor: Alejandro López  
Carrera: Ingeniería en Computación Inteligente

## Variables

#### Definiendo variables

- Definiendo una variable con **dameCase**.
```python
nombreCompleto = "Alexander López"
```
- Definiendo una varible con **snake_Case** (Útilizar esta).
```python
nombre_completo = "Alexander López"
```

---

#### Concatenar

- Concatenar con **+**.

```python
bienvenida = "Hola"  + "¿Cómo estas?"
```

- Concatenar con **f-strings**.

```python
bienvenida = f"Hola {nombre_completo} ¿Cómo estas?"
```

---

## Datos Compuestos

- Son datos que adentro tienen datos simples u otros datos compuestos pero que podemos agruparlos.

#### Listas

- En las listas se cuenta desde el **0** hasta **n** (se le conoce como **indice**).
- Las listas van entre **corchetes**.

```python
lista = ["Gaba", "Python", True, 1.73]

print(lista[0])
```

- Podemos módificar la variable que querramos, llamando la lista y accediendo al índice.


```python
lista[3] = 1.71

print(lista)
```

---

#### Tuplas

- La tupla **no se pueden modificar**.
- Las tuplas van entre **parentesis**.

```python
tupla = ("Gaba", "Python", True, 1.73) 

print(tupla)
```

- **No podemos modificar el caracter en la tupla** debido a que jamas se van a poder modificar despues de asignarlas.  

```python
tupla[3] = 1.71

print(tupla)
```

---

#### Conjuntos

- Para los conjuntos se utilizan las **llaves**.
- **No tienen un orden fijo**, pueden intercambiar la posición.
- **No se puede acceder por el índice** a un elemento del conjunto solo muestra todo el índice.

```python
conjunto = {"Gaba", "Python", True, 1.73}

print(conjunto)
```

- No podemos modificar elementos.

```python
conjunto[1] = "Dart"

print(conjunto)
```

- **No se pueden poner elementos repetidos** (Lo puedes poner, pero no se imprime).

```python
conjunto = {"Gaba", "Python", True, 1.73, "Gaba"}

print(conjunto)
```

- Se pueden redefinir.

```python
conjunto = {"Hola mi nombre es Gaba"}

print(conjunto)
```

---

#### Diccionario (dict)

```python
diccionario = {
    'Key': 'value',
    'nombre' : "Gaba", 
    'edad' : 20,
    'altura' : 1.73,
    'esta_emocionado' : True
}

print (diccionario)
```

- A la hora de querer llamar un elemento por el índice ya no es con la posición del elemento ahora se llama a través del diccionario con el nombre de la **llave**.

```python
print(diccionario['nombre']) # Aqui imprimirá lo que contiene ese carácter.
```

---

## Operadores

####  Aritmeticos

- Suma y Resta ('+' y '-').

```python
suma = 2 + 2
resta = 4 - 2

print(suma)
print(resta)
```

- Multiplicacion y Division ('*' y '/').

```python
multiplicacion = 2 * 2
division = 4 / 2 # Siempre devuelve un dato float (flotante).

print(multiplicacion)
print(division)
```

- Potenciación (exponente) (**).

```python
exponente = 2**3 # Es como si fuera un elevación '^'.

print(exponente)
```

- Division baja. 

```python
division_baja = 15//5 # Devuelve un entero redondeado hacia abajo.

print(division_baja)
```

- Resto o modulo.

```python
resto = 12 % 5 # Solo calcula lo que sobro de la división.

print(resto)
```

---

#### Operadores de Comparación

- Es igual que '=='.

```python
igual_que = 5 == 6

print(igual_que)
```

- Es distinto de '!='.


```python
distinto_de = 5 != 6

print(distinto_de)
```

- Es menor que '<'.

```python
menor_que = 5 < 6 

print(menor_que)
```

- Es menor o igual que '<='.

```python
menor_igual_que = 5 <= 6

print(menor_igual_que)
```

- Es mayor que '>'.

```python
mayor_que = 5 > 6

print(mayor_que)
```

- Es mayor o igual que '>='.

```python
mayor_igual_que = 5 >= 6

print(mayor_igual_que)
```

- Cálculos combinados.

```python
a = 10
b = 20
c = 10
comparacion = a + c == b

print(comparacion)
```

- Comparar usuarios.

```python
contraseña_almacenada = "Gaba15"
contraseña_escrita = "TheGaba15"

print(contraseña_almacenada == contraseña_escrita) # Validando contraseña.
```

---

### Logicos

- Compara uno y otro

#### AND

```python
resultado1 = True & True # Devolver True.
resultado2 = False & True # Devolver False.
resultado3 = True & False # Devolver False.
resultado4 = False & False # Devolver False.
```

---

#### OR

```python
resultado5 = True | True # Devolver True.
resultado6 = False | True # Devolver True.
resultado7 = True | False # Devolver True.
resultado8 = False | False # Devolver False.
```

---

#### NOT

```python
resultado9 = not True # Devolver False.
resultado10 = not False # Devolver True.
```

---

## Condicionales

#### if - else 

```python
if True:
    # El codigo se ejecuta en este bloque.
    print("")

if False:
    # Se ejecuta este codigo.
    print("")
```

- Si eres mayor de edad puedes entrar al bar.
- Si no eres mayor de edad no puedes entrar al bar.

```python
edad = 17

if edad >= 18: # El 'if' funciona para validar la primera condicion.
    print("Eres mayor de edad, puedes pasar") # Este bloque se ejecuta en caso de que la primera condicion se cumpla.
else: # El else funciona en caso de que la primera condicion no se cumpla (if).
    print("No eres mayor de edad, no puedes pasar") # Este bloque se ejecuta en caso de que la primera condicion no se cumpla.
```

-  Comparar usuarios.

```python

contraseña_almacenada = "Gaba15"
contraseña_escrita = "TheGaba15"

if contraseña_almacenada == contraseña_escrita:
    print("Iniciando sesion...")
else:
    print("Contraseña incorrecta, vuelve a intentarlo.")
```

---

#### else if

```python
ingreso_mensual = 100000

if ingreso_mensual > 10000:
    print("Estas bien en cualquier parte del mundo")

# 'elif' Es la conbinacion del 'if' y el 'else'. Es la segunda condicion en caso de que la primera no se cumpla.
elif ingreso_mensual > 1000: 
    print("Estas bien economicamente en latinoamerica")

# Se puede usar las veces que quieras para acomular condiciones.
elif ingreso_mensual > 500: 
    print("Estas bien economicamente en Argentina")

elif ingreso_mensual > 200:
    print("Estas bien economicamente en venezuela")

else:
    print("Eres pobre")
```

```python
ingreso_mensual = 12000
gasto_mensual = 9000

if ingreso_mensual > 10000:
    if ingreso_mensual - gasto_mensual > 3000:
        print("Estas bien")
    else: 
        print("Estas gastando mucho")
```

```python
cant_producto = 10
ing_producto = 6
ret_producto = 2

if cant_producto + ing_producto > 20:
    print("Almacen lleno.")

elif cant_producto + ing_producto > 15:
    print("¡Cuidado! el almacen esta apunto de llenarse.")

if cant_producto - ret_producto < 0:
    print("Ya no hay existencias")

elif cant_producto - ret_producto < 5:
    print("¡Cuidado! se esta agotando este producto")
```

#### Repaso

```python
# Definir Variables
nombre1 = "Diana Jazmin"
nombre2 = "Jahir Alejandro"

sueldo1 = 1200.00
sueldo2 = 1500.00

s = "-"

# Concatenar 
salario1 = f"El salario de {nombre1} es de ${sueldo1}"
salario2 = f"El salario de {nombre2} es de ${sueldo2}"

print(salario1)
print(salario2)
print(s * 152)


# Listas
lista1 = [salario1, salario2, "Esto es una lista"]

print(lista1)
print(s * 152)


# Tuplas
tupla1 = (salario1, salario2, "Esto es una tupla")

print(tupla1)
print(s * 152)


# Conjuntos
conjunto1 = {salario1, salario2, "Esto es un conjunto"}

print(conjunto1)
print(s * 152)


# Diccionarios
diccionario1 = {
    'salario1': salario1,
    'salario2': salario2,
    'mensaje': "Esto es un diccionario"
}

print(diccionario1)
print(s * 152)


# Operadores Áritmeticos
salarioTotal = 0
salarioTotal = sueldo1 + sueldo2

print(salarioTotal)
print(s * 152)
```
