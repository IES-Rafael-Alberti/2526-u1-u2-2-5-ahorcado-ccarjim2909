# Documentación del Programa: Juego del Ahorcado

## 1. Descripción General
Este programa implementa el clásico juego del **Ahorcado** en consola.  
Un jugador introduce una palabra secreta y el otro debe adivinarla letra por letra antes de quedarse sin intentos.

Este proyecto sirve como práctica de:
- Variables y tipos de datos
- Manipulación de cadenas
- Listas
- Sentencias condicionales (`if`)
- Bucles (`while`, `for`)
- Funciones

---

## 2. Objetivo del Programa
Simular el juego del ahorcado validando entradas del usuario y mostrando el progreso hasta que el jugador gane o pierda.

---

## 3. Lenguaje Utilizado
- **Python 3**

---

## 4. Funciones del Programa

| Función | Descripción | Parámetros | Retorno |
|---------|-------------|------------|---------|
| [`limpiar_pantalla()`](https://github.com/IES-Rafael-Alberti/2526-u1-u2-2-5-ahorcado-ccarjim2909/blob/535afaf1e803b87c8ee77a7ab6032258541fa0a3/src/ahorcado.py#L16-L21) | Limpia la consola imprimiendo saltos de línea | Ninguno | Ninguno |
| [`solicitar_palabra()`](https://github.com/IES-Rafael-Alberti/2526-u1-u2-2-5-ahorcado-ccarjim2909/blob/535afaf1e803b87c8ee77a7ab6032258541fa0a3/src/ahorcado.py#L24-L46) | Solicita una palabra válida al jugador 1 (mínimo 5 letras y solo caracteres alfabéticos) | Ninguno | String en mayúsculas |
| [`solicitar_letra(letras_usadas)`](https://github.com/IES-Rafael-Alberti/2526-u1-u2-2-5-ahorcado-ccarjim2909/blob/535afaf1e803b87c8ee77a7ab6032258541fa0a3/src/ahorcado.py#L49-L79) | Solicita una letra válida al jugador 2 que no haya sido utilizada | Lista con letras usadas | Letra válida en mayúsculas |
| [`mostrar_estado()`](https://github.com/IES-Rafael-Alberti/2526-u1-u2-2-5-ahorcado-ccarjim2909/blob/535afaf1e803b87c8ee77a7ab6032258541fa0a3/src/ahorcado.py#L82-L97) | Muestra intentos restantes, palabra oculta y letras usadas | Palabra oculta, intentos, lista de letras | Ninguno |
| [`actualizar_palabra_oculta()`](https://github.com/IES-Rafael-Alberti/2526-u1-u2-2-5-ahorcado-ccarjim2909/blob/535afaf1e803b87c8ee77a7ab6032258541fa0a3/src/ahorcado.py#L100-L130) | Reemplaza guiones por letras correctas | Palabra real, palabra oculta y letra introducida | Palabra oculta actualizada |
| [`jugar()`](https://github.com/IES-Rafael-Alberti/2526-u1-u2-2-5-ahorcado-ccarjim2909/blob/535afaf1e803b87c8ee77a7ab6032258541fa0a3/src/ahorcado.py#L133-L196) | Ejecuta toda la lógica del juego | Ninguno | Ninguno |
| [`main()`](https://github.com/IES-Rafael-Alberti/2526-u1-u2-2-5-ahorcado-ccarjim2909/blob/535afaf1e803b87c8ee77a7ab6032258541fa0a3/src/ahorcado.py#L199-L208) | Punto de entrada del programa | Ninguno | Ninguno |

---

## 5. Variables Importantes

| Variable | Tipo | Descripción |
|----------|------|-------------|
| `INTENTOS_MAXIMOS` | `int` | Cantidad de fallos permitidos (5) |
| `palabra` | `str` | Palabra que debe adivinarse |
| `palabra_oculta` | `str` | Representación con guiones bajos “_ _ _ _” |
| `letras_usadas` | `list` | Letras introducidas por el jugador |
| `intento` | `int` | Número de fallos acumulados |
| `juego_terminado` | `bool` | Indica si el jugador ha adivinado la palabra |

---

## 6. Estructuras Condicionales
El programa utiliza condicionales `if` para:

- Validar que la palabra introducida sea correcta
- Verificar que la letra no esté repetida
- Comprobar si la letra está en la palabra
- Determinar si el jugador ha ganado o perdido

---

## 7. Bucles Usados

| Bucle | Ubicación | Función |
|-------|-----------|---------|
| `while` | Solicitar palabra, solicitar letra, bucle principal del juego | Repetir hasta que la entrada sea válida o la partida termine |
| `for` | Actualizar palabra oculta, contar aciertos | Recorrer carácter por carácter la palabra |

---

## 8. Flujo del Programa

1. El jugador 1 introduce una palabra válida.
2. Se limpia la pantalla para ocultarla.
3. El jugador 2 comienza a adivinar la palabra.
4. Mientras queden intentos disponibles:
   - Se muestra la palabra oculta y las letras usadas.
   - Se pide una letra válida.
   - Se actualiza la palabra oculta.
   - Si se completan todas las letras sin guiones, el jugador gana.
5. Si se acaban los intentos, el jugador pierde y se muestra la palabra correcta.

---

## 9. Ejemplo de Funcionamiento del Programa

El programa pide una palabra al jugador 1 y posteriormente muestra al jugador 2 el número de intentos, la palabra oculta con guiones y las letras usadas. Cada vez que el jugador introduce una letra válida, el programa indica si dicha letra está en la palabra y actualiza el progreso. Si la palabra es adivinada antes de gastar los intentos, muestra un mensaje de victoria. En caso contrario, muestra un mensaje de derrota indicando la palabra correcta.

---

## 10. Posibles Mejoras

- Representar el dibujo del ahorcado con texto ASCII.
- Selección de palabras aleatorias desde una lista.
- Modo de dificultad con diferente cantidad de intentos.
- Contador de partidas ganadas y perdidas.
- Reemplazar la limpieza de pantalla por comandos del sistema (`cls` o `clear`).

---

## 11. Autor
- **Cristian Carrasco Jiménez**
- Fecha del proyecto: *06/11/2025*

---

