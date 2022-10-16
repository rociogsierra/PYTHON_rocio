# PYTHON_rocio

https://github.com/rociogsierra/PYTHON_rocio.git

# ejercicio 1
#consiste en trabajar el concepto de puntos, coordenadas y vectores sobre el plano cartesiano y cómo la programación Orientada a Objetos
#hay que importar math para hacer la raíz cuadrada

import math

#crear una clase llamada Punto con sus dos coordenadas X e Y:
#uso "__init__", que es un método especial para una clase de python (inicializa los atributos del objeto que creamos)
#uso también "self", que hará referencia al nombre del objeto en el que se encuentra escrito

class Punto:
def __init__(self, x=0, y=0):
self.x = x
self.y = y 

#para mostrar objetos, Python indica que hay que agregarle a la clase un método especial, llamado "__str__" que debe devolver una cadena de caracteres con lo que queremos mostrar. Ese método se invoca cada vez que se llama a la función str 

def __str__(self):
return "({},{}).format(self.x, self.y)



# ejercicio 2
#consiste en modificar el texto propuesto utilizando todo lo que sabemos de listas, cadenas, métodos internos, etc., sin modificar directamente el texto

texto_original= "un día que el viento soplaba con fuerza#mira como se mueve aquella banderola -dijo un monje#lo que se mueve es el viento -respondió otro monje#ni las banderolas ni el viento, lo que se mueve son vuestras mentes -dijo el maestro"
def modificar_texto_original(texto):
texto= texto.replace("#","\n")
oracion= texto.split("\n")
for lugar in range(len(oracion)):
if lugar==0:
oracion[lugar]= oracion[lugar].capitalize() + "..."
else:
oracion[lugar]= "-" + oracion[lugar].capitalize() + "."
texto = "\n".join(oracion)
return texto
print(modificar_texto_original(texto_original))

# ejercicio 3
#consiste en crear una función denominada "modificar" que a partir de una lista de números realice ciertas tareas sin modificar la original

def modificar(lista):
print("en esta lista hemos borrado los elementos duplicados:")
duplicados_borrados= list(dict.fromkeys(lista))
print(duplicados_borrados)

print("esta lista está ordenada de mayor a menor:")
orden_de_mayor_a_menor= sorted(duplicados_borrados, reverse=True)
print(orden_de_mayor_a_menor)

print("en esta lista hemos borrado los números impares:")
impares_borrados= []
for num in orden_de_mayor_a_menor:
if num % 2 == 0:
impares_borrados.append(num)
print(impares_borrados)

print("en esta lista realizaremos una suma de todos los números que quedan:")
#usamos la función "sum(list)" propuesta en el enunciado
suma_del_resto= sum(impares_borrados)
print(suma_del_resto)

print("aquí añadimos como primer elemento de la lista, la suma realizada:")
impares_borrados.insert(0, suma_del_resto)
return impares_borrados

lista_1= [1, 3, 5, 7, 2, 6, 9, 4, 6, 8, 5, 2, 2, 3]
nueva_lista= modificar(lista1)
print(nueva_lista[0] == sum(nueva_lista[1:]))
True
print(lista1)
