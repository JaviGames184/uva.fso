# Guerra de Naves
Esta es una práctica de la asignatura de Fundamentos de Sistemas Operativos (FSO).

Para ejecutar el programa:

```
./programa ficheroEntrada ficheroSalida bufferSize numNaves
```
- **ficheroEntrada**: Un fichero que contiene:
    - "*": La nave ha recibido un disparo.
    - " ": La nave ha fallado un disparo.
    - "b1" / "b2" / "b3": La nave recibe una curacion de 1,2 o 3.
    - Cualquier otro carácter será ignorado.
- *ficheroSalida*: Un fichero donde se guardan los resultados de la ejecución.
- *bufferSize*: Tamaño del buffer circular donde se colocan los elementos encontrados en el fichero de entrada.
- *numNaves*: Número de naves que generará el programa.

El programa está formado por:

1. **Hilo Disparador**: Se encarga de leer el fichero de entrada y colocar los caracteres en el buffer circular.
   
2. **Hilo Nave**: Cada una de las naves es un hilo que leer el buffer circular y registra los caracteres que encuentra. Cuando el hilo disparador termine de procesar fichero, cada nave tendrá una lista de resultados almacenados en su lista enlazada.
   
3. **Hilo Juez**: Lee las listas enlazadas de las naves para imprimir los resultados. Una vez que todas las naves terminen, el juez también imprimirá las naves que han terminado en primera y segunda posición. 

# Autores 🧑🏻‍💻
- **[AlexMinn](https://github.com/AlexMinn)**
- **[JaviGames184](https://github.com/JaviGames184)**
