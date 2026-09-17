Ejercicio 2.E.1 10 - Personaje

Lógica del programa
Para este ejercicio, desarrollé un simulador de combate por turnos trabajando con dos clases: `Personaje` y la clase principal `Main`.

Primero, diseñé la clase `Personaje` con los atributos privados `nombre` (String), `puntosVida` (int) y `puntosAtaque` (int), junto con un constructor para inicializar las estadísticas de cada luchador. 

El comportamiento de la clase lo definí con los siguientes métodos:
1. `atacar(Personaje objetivo)`: Este método es clave porque muestra cómo interactúan dos objetos. Recibe como parámetro a otro objeto de tipo `Personaje` y le resta a sus `puntosVida` el valor de los `puntosAtaque` del personaje que está ejecutando la acción, imprimiendo el resultado en pantalla.
2. `estaVivo()`: Evalúa si los puntos de vida del personaje son mayores a 0 y retorna un valor booleano (`true` o `false`).
3. `obtenerNombre()`: Un método *getter* simple para poder acceder al nombre del personaje de forma segura.

Por otro lado, en la clase `Main`, desarrollé la lógica del combate:
1. Instancié dos objetos `Personaje` ("Jorge Selva" y "Nicolas Rincon") con sus respectivos atributos de vida y ataque.
2. Implementé un bucle `while` que evalúa constantemente que ambos personajes sigan con vida (usando el método `estaVivo()`).
3. Dentro del bucle, los personajes se atacan por turnos. Agregué una validación (`if`) para asegurarme de que el segundo personaje solo pueda contraatacar si sobrevivió al primer golpe.
4. Una vez que el bucle termina (cuando uno de los dos se queda sin vida), el programa sale de la estructura iterativa y utiliza una última condición `if/else` para anunciar al ganador.

Ejecución en consola
<img width="1366" height="720" alt="imagen" src="https://github.com/user-attachments/assets/87aee006-cf34-42be-9e67-030aa8e9b674" />
