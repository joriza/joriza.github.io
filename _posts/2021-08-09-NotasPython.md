---
layout: post
title:  "Notas Python"
date:   2021-08-08 20:46:59 -0300
categories: Notas
---
# pipenv
Entorno virtual de Python
https://www.faztweb.com/curso/python-pipenv/introduccion
https://platzi.com/tutoriales/1378-python/2292-pipenv-virtualenv-y-pip-en-un-solo-comando/

## Para instalar el manejador del entorno virtual.
    pip3 install pipenv

## Crear e Iniciar, o solo para iniciar el entorno virutal
Ir a la carpeta del proyecto

    pip3 shell

cambia el prompt para indicar que está inicializado
-
pipenv shell
## Ahora los módulos se deben instalar dentro del entorno virutal
pip install flask

## Salir del entorno virtual
exit

## Eliminar un environment ejecuta
pipenv --rm

# Datos varios
## Listar los paquetes instalados
pip list
## Eliminar todos los paquetes instalados
pipenv uninstall --all
pip freeze | xargs pip uninstall -y
## Creaar archivo requirements.txt con lo instalado actualmente
pip freeze > requirements.txt
## Instalar paquetes desde requirements.txt
pip install -r requirements.txt
## Quitar los paquetes que están en requirements.txt
pip uninstall -r requirements.txt -y




---

# Tips Sueltos, sin clasificar.

## [Repositorio de manuales y recursos del entrenamiento](https://entrenamiento-python-basico.readthedocs.io/es/latest/index.html#)
## [Agregar help a una funcion](https://platzi.com/clases/1764-python-cs/25242-especificaciones-del-codigo/)  
partes importantes que son las siguientes:  
Primero se da una descripción clara y concisa de la función y su funcionamiento.  
En medio se agrega la descripción de los diferentes parámetros, su tipo, su nombre y que es lo que se espera de esos parámetros..  
Por ultimo se agrega que es lo que devuelve nuestra función.  

## [Recursividad](https://platzi.com/clases/1764-python-cs/25243-recursividad/)

```
#Importamos el modulo sys que nos permitira modificar la recursion
import sys

def factorial(n):
    """Calcula el factorial de n

        n int > 0
        returns n!
    """
    print(n)
    if n == 1:
        return 1
    
    return n * factorial(n - 1)

n = int(input('Escribe un entero: '))

# Imprimimos el limite de recursion que trae python por defecto con la funcion sys.getrecursionlimit() que trae el modulo sys. 
print(sys.getrecursionlimit())

# Modificamos el limite de recursion a 2000 con la funcion sys.setrecursionlimit() que trae el modulo sys
sys.setrecursionlimit(2000)

print(factorial(n))
```

## Tuplas
Es una lista que no se puede modificar.
Utiliza menos memoria y es más rápida para recorrer.
mi_tupla = (1,2)

## Rangos
Son secuencias de enteros.
Son inmutables.
mi_gango = (comienzo, fin, pasos)
El final es no inclusivo

## Listas
mi_lista = [1,2,3]
Se pueden usar slices
-agregar un item
mi_lista.append(valor)
se agrega al final
-
quitar el último item
mi_lista.pop(valor)
-
Tener cuidado al crear una lista de listas.
Porque en realidad es el mismo objeto.
en vez de hacer a=b
para c, usar
c = list(a)
o con slices
d = a[::]
-
### List comprehension.
Es una forma concisa de aplicar operaciones a todos los items de una lista.
my_list = list(range(100))
-
defino una nueva lista, a partir de la primera
pares = (i for i in my_list if i % 2 == 0)
i
for i in my_list
if i % 2 == 0

## Diccionarios
Son como listas, que en vez de acceder a ellos por un indice numérico, se accede a los valores a travez de llaves.
No tienen un orden interno establecido.
Son mutables e iterables.
mi_dicc = {
    'Juan' = 35,
    'Pedro' = 40
}
- Para traer un valor.
mi_dicc ['Juan']
pero la clave debe existir.
mi_dicc.get('Juan',30)
Si existe nos trae el valor, sino trae 30.
- Para asignar un valor a una clave existente.
mi_dicc['Juan'] = 22
Si no existe la llave, crea un nuevo item.

Metodos para listas
https://jarroba.com/list-python-ejemplos/

Métodos para diccionarios
https://jarroba.com/diccionario-python-ejemplos/



