# PYTHON_rocio

https://github.com/rociogsierra/PYTHON_rocio.git

# ejercicio 1

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

