---
layout: post
title: "Lenguaje Python"
author: "Cristobal Sandoval"
header-style: text
catalog: true
tags:
  - Lenguage code
  - Python
---

# Introducción

```python
print("Hola mundo")
```

# Sintaxis básica

#### Comentarios

```python

# <= soy un comentario en una sola línea

"""
hola
soy un
comentario
en multiples líneas
"""

```

#### Secuencia de escape

```python

# \ muestra un elemento propio del lenguaje como un string para se pueda ver
# \n salto de línea

```

#### Variables

```python
# String => Cadena de carácteres
nombre_variable = tipo_de_dato

# REFERENTE AL NOMBRE DE LA VARIABLE
#1 NO se puede iniciar con un número
#2 NO se puede iniciar con un número + letras
#3 NO se puede escribir con "Ñ"
#4 NO se puede escribir con "-"
#5 NO se puede escribir con alguna PALABRA RESERVADA

```

#### Operadores

| Descripción           | Operadores aritméticos |
| :-------------------- | :--------------------: |
| Multiplicar           |           \*           |
| Dividir               |           /            |
| Dividir sin decimales |           //           |
| Sumar                 |           +            |
| Restar                |           -            |
| Modulo/Residuo        |           %            |
| Elevar un N°          |          \*\*          |

```python

"""
Hay una manera elegante y no elegante de aplicar
los operadores numéricos

EJEMPLO CON LA SUMA, PERO SE APLICA CON TODOS LOS
OTROS OPERADORES NUMÉRICOS
"""
sumar_no_elegante = sumar_no_elegante + 2
sumar_elegante += 2

```

| Descripción      | Operadores comparación |
| :--------------- | :--------------------: |
| Es igual         |           ==           |
| Es igual o menor |           <=           |
| Es igual o mayor |           >=           |
| Es mayor         |           >            |
| Es menor         |           <            |
| No es igual a    |           !=           |

| Descripción     | Operadores lógicos |
| :-------------- | :----------------: |
| Y               |        and         |
| O               |         or         |
| Negar resultado |        not         |

| Descripción          | Operadores de concatenación |
| :------------------- | :-------------------------: |
| Combinar dos cadenas |              +              |

#### Metadata

#### Importación / librería

#### Palabras reservadas

| Palabra reservada |                 Descripción                 |
| :---------------- | :-----------------------------------------: |
| False             |               Valor booleano                |
| True              |               Valor booleano                |
| and               |               Operador lógico               |
| or                |               Operador lógico               |
| or                |               Operador lógico               |
| not               |               Operador lógico               |
| if                |           Declaración condicional           |
| elif              |           Declaración condicional           |
| else              |           Declaración condicional           |
| import            |             Importar un módulo              |
| as                |           Alias de para un import           |
| From              |        Importar partes de un módulo         |
| assert            |         Contrato para pre condición         |
| async             |             Código concurrente              |
| await             |             Código concurrente              |
| for               |                    Bucle                    |
| while             |                    Bucle                    |
| break             |    Alteral un comportamiento de un bucle    |
| continue          |    Alteral un comportamiento de un bucle    |
| class             |               Crear una clase               |
| def               |              Crear una función              |
| return            |       Retorna un valor en una función       |
| try               |              Crear excepciones              |
| except            |              Crear excepciones              |
| raise             |              Crear excepciones              |
| Global            |          Declarar variable global           |
| Del               |             Eliminar un objeto              |
| finally           | Ejecutar código aunque ocurra una excepción |
| is                |     Compara si dos valores son iguales      |
| in                |   Saber si un valor esta en una coleccion   |

# Tipos básicos

#### Carácteres

```python
# String => Cadena de carácteres
nombre = "Cristobal Sandoval"

```

#### Enteros

```python

# Integer => Número entero
edad = 27

```

#### Decimal

```python

# Float => Número decimal
altura = 1.76

```

#### Imaginarios

```python

# Número imaginario
numero_imaginario = 2 + 2j

```

#### Booleanos

```python

# boolean => Verdadero o falso
casado = False
soltero = True

```

# Tipos Avanzados

#### Lista

```python

# Sintaxis
nombre_de_la_lista = [dato,dato]
# Ejemplo de una lista de caracteres
amigos = ["Miguel","Mauricio","Benjamin"]
print(amigos)

```

#### Lista sin dato repetido (set)

```python

# Sintaxis
nombre_de_la_lista_set = {dato,dato}
# Ejemplo de una lista de caracteres
amigos = {"Miguel","Mauricio","Benjamin","Miguel"}
print(amigos)

```

#### Diccionario

```python

# Sintaxis
nombre_del_diccionario = {"llave":valor,"llave":valor}
# Ejemplo de una lista de caracteres
amigos = {"1":"Miguel","2":"Mauricio","3":"Benjamin"}
print(amigos)

```

#### Tuplas

```python

# Sintaxis
nombre_de_la_tupla = (dato,dato)
# Ejemplo de una lista de caracteres
amigos = ("Miguel","Mauricio","Benjamin","Miguel")
print(amigos)

```

#### Operaciones generales

```python

# Ejemplo aplicado con los diccionarios
amigos = {"1":"Miguel","2":"Mauricio","3":"Benjamin",
"4":"Javier","5":"Nicolas"}

# Desestructuración o desempaquetar
amigo1,amigo2,amigo3 = amigos
amigo1,*otros = amigos
*otros,amigo3 = amigos

# Iterar
for amigo in amigos:
  print(amigo)

# Compresión
posiciones = [amigo[0] for amigo in amigos]

# Manipular
new_amigos = amigos[:1]
new_amigos = amigos[0:]
new_amigos = amigos[0:1]
new_amigos = amigos[3::]
new_amigos = amigos[1:3:4]
new_amigos = amigos[::3]
new_amigos = amigos[2::]

```

# Funciones

#### Sintaxis de la función

```python

# Sintaxis de la función

def nombre_funcion_sin_retorno(
  parametro_obligatorio:any,
  parametro_opcional="Soy opcional",
  ):
    # Ejecutar código de la función

def nombre_funcion_con_retorno(
  parametro_obligatorio:any,
  parametro_opcional="Soy opcional",
  ):
    # Ejecutar código de la función
    return parametro


# Incovar una función

nombre_funcion_sin_retorno(
  parametro_obligatorio= "soy un parametro",
  parametro_opcional= "Soy opcional"
  )

 """
 Si invoco el nombre de un argumento debo hacerlo con todos
 """

nombre_funcion_con_retorno("soy un parametro")

```

# Flujo de control

#### Sintaxis del Bucle "for"

```python

amigos = ["Miguel", "Mauricio", "Benjamin"]

# Sintaxis de FOR
for amigo in amigos:
    print(amigo)


# Sintaxis de FOR-ELSE
buscar_amigo = "Mauricio"
for amigo in amigos:
    if amigo == buscar_amigo:
        print(f"encontrado a {buscar_amigo}")
        break
else:
    print("No se encontro el \"amigo\"")

```

#### Sintaxis del Bucle "while"

```python

amigos = ["Miguel", "Mauricio", "Benjamin"]
buscar_amigo = "Mauricio"
# Sintaxis de WHILE

while buscar_amigo in amigos:
    print("Es mi amigo")
    break
```

#### Sintaxis de la declaración condicional "if", "elif" y "else"

```python

# Sintaxis de IF
edad = 26
if edad >= 10:
    print("Mi edad es mayor a 10 años")
# Sintaxis de ELIF
elif edad <= 30:
    print("Mi edad es menor a 30 años")
# Sintaxis de ELSE
# NO ES OBLIGACIÓN UTILIZARLO
else:
    print("Mi edad se encutra fuera del rango de 10-30 años")

```

```python

# Cadena de comparadores
edad = 26
if edad >= 10 and edad <= 30:
  print("Mi edad se encuentra entre los 10-30 años")

```

# Excepciones

#### Sintaxis de try-except

```python

# Sintaxis 1 de TRY-EXCEPT

try:
    # Ejecutar código
except:
    # Ejecutar código si falla

# Sintaxis 2 de TRY-EXCEPT

try:
    # Ejecutar código
except:
    # Se ejecuta si falla el código
else:
    # Se ejecuta si no falla el código
finally:
    # Se ejecuta siempre

```

==> [Jerarquia de excepciones](https://docs.python.org/3/library/exceptions.html#exception-hierarchy)

# Clase y objeto

#### Sintaxis de una clase

```python

class NombreDeLaClase:
    # Variables explicitas
    nombre = ""

    # Constructor
    def __init__(self,nombre:str, edad):
        self.nombre = nombre
        self.edad = edad

    # función
    def funcion_de_la_clase(self):
        return "Hola"

# instanción o ejemplo de una clase
ejemplo_de_la_clase = NombreDeLaClase()

# SELF  representa el objeto de la clase de si mismo

```

#### Constructor de la clase

```python

class NombreClase:
    def __init__(self):
        """ Constructor de la clase """

```

#### Propiedades de la clase

```python

class NombreClase:

    nombre_del_atributo_propiedad = "Nombre del atributo o propiedad"

```

#### Métodos de la clase

```python

class NombreClase:
    def nombre_metodo(self):
        """Nombre función """

```

#### Super de la clase

```python

class NombreClase:
    # Ideal para herencia multiple de los atributos
    NombreDeLaOtraClase.__init__(self)
    # Ideal para herencia simple y metodos
    super()

```

#### Objeto de la clase

```python

NombreClase()

nombre_clase = NombreClase()

```

#### Herencia

```python

"""Module providing a function printing python version."""

class Vehiculo:
    """Class representing a CRUD"""
    def __init__(self, name_vehicle):
        self.name_vehicle = name_vehicle

    def __str__(self):
        return f"Vehiculo seleccionado: {self.name_vehicle}"

    def encender(self):
        """ Encender vehiculo """
        return "Encendiendo vehiculo"

    def apagar(self):
        """ Apagando vehiculo """
        return "Apagando vehiculo"

class Motocicleta(Vehiculo):
    """Class representing a Service aplicando CRUD"""


motocicleta = Motocicleta(name_vehicle="Honda xblade 160")

print(motocicleta)
print(motocicleta.encender())
print(motocicleta.apagar())

```

#### Herencia multiple

```python

"""Module providing a function printing python version."""

class Vehiculo:
    """Class Vehiculo"""
    def __init__(self, name_vehicle):
        self.name_vehicle = name_vehicle

    def __str__(self):
        return f"Vehiculo seleccionado: {self.name_vehicle}"

    def encender(self):
        """ Encender vehiculo """
        return "Encendiendo vehiculo"

    def apagar(self):
        """ Apagando vehiculo """
        return "Apagando vehiculo"


class LeyesDeTransito:
    """ Class Leyes de transito """
    def __init__(self,licencia_aprobada):
        self.licencia_aprobada = licencia_aprobada

    def tipos_de_licencia(self):
        """ Tipo de licencia """
        return "D,C,B y Profecional"


class Chofer(LeyesDeTransito,Vehiculo):
    """ CHofer de vehiculo """
    def __init__(self,licencia_aprobada,name_vehicle):
        LeyesDeTransito.__init__(self, licencia_aprobada)
        Vehiculo.__init__(self, name_vehicle)

chofer = Chofer(licencia_aprobada=True,name_vehicle="Honda xblade 160")

print(chofer)
print(chofer.encender())
print(chofer.apagar())
print(chofer.tipos_de_licencia())
print(chofer.licencia_aprobada)

```

#### Clase abstracta

```python

"""Module providing a function printing python version."""
from abc import ABC, abstractmethod

#print a text
class Crud(ABC):
    """Class representing a CRUD"""

    @property
    @abstractmethod
    def name_service(self):
        """ nombre del servicio """

    @abstractmethod
    def create(self):
        """ crear """
        # pass <= sse puede colocar o no,
        # si la comunidad lo indica que no entonces NO colocarlo

    @abstractmethod
    def delete(self):
        """ eliminar """

    @abstractmethod
    def update(self):
        """ actualizar """

    @abstractmethod
    def get_all(self):
        """ obtener todo """

    @abstractmethod
    def get_id(self):
        """ obtener por id """

class ServiceHttp(Crud):
    """Class representing a Service aplicando CRUD"""

    name_service = "HTTP"

    def create(self):
        """ crear """
        return "creando"

    def delete(self):
        """ eliminar """
        return "eliminando"

    def update(self):
        """ actualizar """
        return "actualizando"

    def get_all(self):
        """ obtener todo """
        return "obteniendo todo"

    def get_id(self):
        """ obtener por id """
        return "obteniendo por id"


servicio_http = ServiceHttp()

print(servicio_http.name_service)
print(servicio_http.delete())

```
