# Inferential_Statistics
# INTRODUCCIÓN A NUMPY 1

# TEMAS DE LA CLASE
# Conversión de objetos enlistados a arreglos
# Acceso a elementos de un arreglo
# Operaciones vectoriales
# Creación de matrices


# TIPOS DE OBJETOS EN PYTHON

print("1 + 1 =", 1 + 1)
print("Tipo de 1 + 1:", type(1 + 1))
print("Tipo de 1 + 1 + 0.5:", type(1 + 1 + 0.5))

x = "Hola a todos"
print(x)
print("Tipo de x:", type(x))


# LISTAS DE ELEMENTOS

# Una lista es una enumeración de elementos.
# Para crear una lista se utilizan corchetes.

l1 = []
print("Lista vacía:", l1)
print("Tipo de l1:", type(l1))

l1 = [1, 2, 3, 4, 5]
l2 = [6, 7, 8, 9, 10]

print("Lista 1:", l1)
print("Lista 2:", l2)
print("Longitud de l1:", len(l1))
print("Longitud de l2:", len(l2))
print("¿Tienen la misma longitud?", len(l1) == len(l2))


# CONCATENACIÓN DE LISTAS

# Al utilizar el signo + con listas, Python las concatena.
# Todavía no realiza una suma elemento por elemento.

print("Listas concatenadas:", l1 + l2)

l3 = [1]
l4 = [100, 101]

print("l3 + l4:", l3 + l4)


# ACCESO A ELEMENTOS DE UNA LISTA

# Python comienza a contar los elementos desde el índice 0.

print("Elemento con índice 0:", l1[0])
print("Elemento con índice 1:", l1[1])
print("Elemento con índice 2:", l1[2])
print("Elemento con índice 3:", l1[3])
print("Elemento con índice 4:", l1[4])


# SUMA MANUAL DE LISTAS ELEMENTO POR ELEMENTO

l = [
    l1[0] + l2[0],
    l1[1] + l2[1],
    l1[2] + l2[2],
    l1[3] + l2[3],
    l1[4] + l2[4]
]

print("Suma manual:", l)


# RANGOS Y CICLOS

print("Tipo de range:", type(range(0, 5)))

print("Números del rango:")
for i in range(0, 5):
    print(i)


# SUMA DE LISTAS UTILIZANDO UN CICLO

l = [l1[i] + l2[i] for i in range(0, 5)]
print("Suma utilizando un ciclo:", l)


# MULTIPLICACIÓN DE UNA LISTA

# Al multiplicar una lista por 2, Python repite la lista.

print("Lista repetida dos veces:", 2 * l2)


# MULTIPLICACIÓN ELEMENTO POR ELEMENTO

m = [0.5 * l2[i] for i in range(0, 5)]
print("Lista multiplicada por 0.5:", m)

m = [2 * l2[i] for i in range(0, 5)]
print("Lista multiplicada por 2:", m)


# ARREGLOS

# NumPy permite convertir listas en arreglos.
# Los arreglos permiten realizar operaciones vectoriales.

import numpy as np

l1_arreglo = np.array(l1)
l2_arreglo = np.array(l2)
l3_arreglo = np.array(l3)
l4_arreglo = np.array(l4)

print("Arreglo 1:", l1_arreglo)
print("Arreglo 2:", l2_arreglo)
print("Tipo de l1_arreglo:", type(l1_arreglo))


# OPERACIONES CON ARREGLOS

print("Suma de arreglos:", l1_arreglo + l2_arreglo)
print("Arreglo 1 multiplicado por 2:", 2 * l1_arreglo)
print("Arreglo 2 multiplicado por 0.5:", 0.5 * l2_arreglo)
print("Suma de l3_arreglo y l4_arreglo:", l3_arreglo + l4_arreglo)


# MATRICES

# Una matriz tiene renglones y columnas.
# reshape permite cambiar la forma de un arreglo.

lista = [i for i in range(10, 30)]

print("Lista del 10 al 29:", lista)
print("Cantidad de elementos:", len(lista))

array = np.array(lista)

print("Arreglo:", array)


# MATRIZ DE 10 RENGLONES Y 2 COLUMNAS

matriz1 = array.reshape(10, 2)
print("Matriz de 10 x 2:")
print(matriz1)


# MATRIZ DE 2 RENGLONES Y 10 COLUMNAS

matriz2 = array.reshape(2, 10)
print("Matriz de 2 x 10:")
print(matriz2)


# MATRIZ DE 5 RENGLONES Y 4 COLUMNAS

matriz3 = array.reshape(5, 4)
print("Matriz de 5 x 4:")
print(matriz3)
