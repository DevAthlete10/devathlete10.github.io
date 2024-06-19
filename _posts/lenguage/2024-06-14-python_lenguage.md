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

```python

""" Modulos """
# Importar desde la misma carpeta
from usuarios import Usuario, cat_bruno

# Importar desde la misma carpteta el modulo completo
import main

# Importar desde sub_paquetes
from paquete.sub_paquete.usuarios import Usuario, cat_bruno

usuario = Usuario()
CREADO = usuario.create()

```

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

# Paquetes más populares nativos

#### Clasificación de los paquetes nativos

|     Nombre del paquete      |     Clasificación     |
| :-------------------------: | :-------------------: |
|        [_str_](#str)        |     Tipo de dato      |
|      [_float_](#float)      |     Tipo de dato      |
|       [_bool_](#bool)       |     Tipo de dato      |
|        [_int_](#int)        |     Tipo de dato      |
|       [_time_](#time)       |         Fecha         |
|   [_datetime_](#datetime)   |         Fecha         |
| [_webbrowser_](#webbrowser) | Manejo de navegadores |
|     [_random_](#random)     |  Números aleatorios   |
|    [_pathlib_](#pathlib)    |   Rutas de archivos   |
|       [_json_](#json)       |    Tipo de archivo    |
|    [_zipfile_](#zipfile)    |    Tipo de archivo    |
|        [_csv_](#csv)        |    Tipo de archivo    |
|         [_os_](#os)         |         nose          |

#### str

#### float

#### bool

#### int

#### int

#### time

#### webbrowser

```python

import webbrowser

print("productos encontrado!")

webbrowser.open("https://google.com")


```

#### datetime

```python

# https://docs.python.org/3/library/datetime.html#strftime-and-strptime-format-codes

""" Modulos """
from datetime import datetime, timedelta

fecha = datetime(1997,7,2) + timedelta(weeks=1)
fecha_2 = datetime(2017,7,2)
hoy = datetime.now()
print(fecha)
print(hoy)

fechaStr = datetime.strptime("1997-07-02","%Y-%m-%d")

print(fechaStr)
print(fecha.strftime("%Y.%m.%d"))

delta = fecha_2 - fecha
print(delta)

print("dias",delta.days)
print("segundos",delta.seconds)
print("microseconds",delta.microseconds)
print("total_seconds",delta.total_seconds())


```

#### random

```python

import random
import string

numeros = [1,2,3,4,5,6,7,8,9]
numeros_2 = [1,2,3,4,5,6,7,8,9]

random.shuffle(numeros)

print(
    random.random(),
    random.randint(1,10),
    numeros,
    random.choices(numeros_2),
    random.choices(numeros_2,k=3),
    "".join(random.choices("abcdefghi.,123",k=3)),
)

chars = string.ascii_letters
digitos = string.digits
seleccion = random.choices(chars + digitos,k=16)

contrasena = "".join(seleccion)
print(f"contraeña: {contrasena}")


```

#### pathlib

```python

""" Modulos """
from pathlib import Path

# Ruta del archivo a seleccionar
archivo = Path("paquete/creado.txt")

# Leer un texto existente
texto = archivo.read_text("utf-8").split("\n")

# Leer un Modificar un texto existente
texto.insert(0,"Hola perro")
texto.append("Hola perro")
# archivo.write_text("Hola perro","utf-8")
# Se elimina todo el texto y se cambia por lo escrito
# entre los parentesis
archivo.write_text("\n".join(texto),"utf-8")

```

#### os

```python

from io import open

#ESCRITURA
texto = "Hola perro"
archivo = open("paquete/hola-perro.txt","w")
archivo.write(texto)
archivo.close()

# LECTURA
archivo = open("paquete/hola-perro.txt")
texto = archivo.read()
archivo.close()
print(texto)

# LECTURA TIPO LISTA
archivo = open("paquete/hola-perro.txt")
texto = archivo.readlines()
archivo.close()
print(texto)


#  WITH Y SEEK
with open("paquete/hola-perro.txt") as archivo:
    print(archivo.readlines())
    archivo.seek(0)
    for linea in archivo:
        print(f"linea => {linea}")

# AGREGAR
archivo = open("paquete/hola-perro.txt","a+")
archivo.write("Chao perro :(")
archivo.close()

#  LECTURA Y ESCRITURA
with open("paquete/hola-perro.txt","r+") as archivo:
    texto = archivo.readlines()
    archivo.seek(0)
    texto[0] = "Holaaaaaa perrito"
    archivo.writelines(texto)


```

#### zipfile

```python

""" Modulos """
from pathlib import Path
from zipfile import ZipFile

# ESCRIBIR
with ZipFile("paquete/comprimidos.zip", "w") as zip:
    for path in Path().rglob("*.*"):
        print(path)
        if str(path) != "paquete\comprimidos.zip":
            zip.write(path)

# LEER
with ZipFile("paquete/comprimidos.zip") as zip:
    info = zip.getinfo("comprimidos_pruebas.py")
    print(
        info.file_size,
        info.compress_size
    )
    zip.extractall("paquete/descomprimidos")

```

#### json

```python

""" Modulos """
import json
from pathlib import Path

productos = [
    {"id":1,"name":"gato"},
    {"id":2,"name":"perro"},
    {"id":3,"name":"pajaro"},
]

# CREAR JSON
data = json.dumps(productos)
Path("paquete/productos.json").write_text(data)

# LEER JSON
data = Path("paquete/productos.json").read_text(encoding="utf-8")
productos = json.loads(data)
print(productos)

# MODIFICAR JSON
productos[0]["name"] = "Lagartija"
Path("paquete/productos.json").write_text(json.dumps(productos))


```

#### csv

```python

""" Modulos """

import csv
import os


# ESCRIBIR
with open("paquete/cristobal.csv","w") as archivo:
    writer = csv.writer(archivo)
    writer.writerow(["left_id","center_id","texto"])
    writer.writerow([1000,1,"right text"])
    writer.writerow([1001,2,"right ffff"])

# LEER
with open("paquete/cristobal.csv") as archivo:
    reader = csv.reader(archivo)
    print(list(reader))
    archivo.seek(0)
    for linea in reader:
        print(linea)

# ACTUALIZAR
with open("paquete/cristobal.csv") as r,open("paquete/cristobal_sandoval.csv","w") as w:
    reader = csv.reader(r)
    writer = csv.writer(w)
    for linea in reader:
        if linea[0] == "1000":
            writer.writerow([1000,1,"text modificado"])
        else:
            writer.writerow(linea)
    os.remove("paquete/cristobal.csv")
    os.rename("paquete/cristobal_sandoval.csv","paquete/cristobal.csv")

```

# Gestión de dependencias externas

#### Clasificación de los paquetes no nativos

|  Nombre del gestor  | Clasificación |
| :-----------------: | :-----------: |
|   [_pip3_](#pip3)   |               |
| [_pipenv_](#pipenv) |               |

#### pip3

> Instalador de paquetes

```python
# Instalar última versión del paquete
pip3 install nombre_paquete

# Instalar versión deseada del paquete
pip3 install nombre_paquete==2.2.0

# Instalar la última versión según el
# orden versionado semantico deseado del paquete
pip3 install nombre_paquete==2.2.*
pip3 install nombre_paquete==2.*

# Instalar la última versión del paquete según
# el criterio pip3
pip3 install nombre_paquete~=2.2.0

# Desintalar un paquete
pip3 uninstall

# Mostrar la lista de paquete instaldos
pip3 list

# Herramientas para generar empaquetado
pip3 install setuptools wheel twine

```

#### Ambiente virtual (Localmente)

```python
# Crear ambiente virtual
python -m venv env

# Seleccionar ambiente virtual
Desde el editor de código configurarlo

# Activar ambiente virtual
"""
En terminal colocar la ruta del archivo
"activate.bat" => comunmente se encuentra en
"env/scripts/activate.bat" en el terminal

"""
# Desactivar ambiente virutal

```

#### pipenv

```python
# Instalar
pip3 install pipenv

# Activar ambiente virtual
pipenv shell

# Desactivar ambiente virtual
exit

# Saber en donde esta ubicado el ambiente virtual
pipenv --venv

# Eliminar el ambiente virtual
rm -rf Path_del_ambiente_virtual

# Ignorar el archivo "Pipfile"
pipenv install --ignore-pipfile

# Ver las dependencias instaladas
pipenv graph

# Dependencias instaladas no a la última versión
pipenv update --outdated

# Actualizar todas las dependencias instaladas
pipenv update

# Actualizar una dependencia específica
pipenv update nombre_paquete


```

# Paquetes más populares no nativos

#### Clasificación de los paquetes no nativos

|         Nombre del paquete          |    Clasificación     |
| :---------------------------------: | :------------------: |
|       [_requests_](#requests)       |         HTTP         |
| [_beautifulsoup4_](#beautifulsoup4) |     scraping web     |
|       [_openpyxl_](#openpyxl)       |   ead/write Excel    |
|       [_selenium_](#selenium)       | Prueba automatizadas |

#### requests

[Link de la documentación](https://pypi.org/project/requests/)

```python

# pipenv install requests
 import requests

 url = "https://jsonplaceholder.typicode.com/users"

 resp = requests.get(url)

```

#### beautifulsoup4

[Link de la documentación](https://www.crummy.com/software/BeautifulSoup/bs4/doc.es/)

```python
# pipenv install beautifulsoup4, requests
import requests

from bs4 import BeautifulSoup

url = "https://pub.dev/packages"

respuesta = requests.get(url).text

soup = BeautifulSoup(respuesta,"html.parser")

preguntas = soup.select(".packages-item")

for pregunta in preguntas:
    titulo = pregunta.select_one(".packages-title").get_text()
    puntaje = pregunta.select_one(".packages-scores").get_attribute_list("href")
    print(f"Titulo: {titulo} \n link: {puntaje} \n")

```

#### openpyxl

[Link de la documentación](https://openpyxl.readthedocs.io/en/stable/)

```python

# pipenv install openpyxl
import openpyxl

wb = openpyxl.load_workbook("Libro1.xlsx")

hoja_activa = wb.active
wb.create_sheet("gola")
celda = hoja_activa["A1"]
celda_opcion_2 = hoja_activa.cell(row=2,column=2)
celda.value = "Cristobal"
print(wb["Hoja1"])
print(wb.sheetnames)
print(hoja_activa)
print(celda_opcion_2)
print(hoja_activa["A1"])

for fila in range(1,hoja_activa.max_row):
    for column in range(1,hoja_activa.max_column):
        new_celda = hoja_activa.cell(row=fila,column=column)
        print(fila,column,new_celda.value)

wb.save("nuevo_excel.xlsx")

```

#### selenium

[Link de la documentación](https://selenium-python.readthedocs.io/)

```python


```
