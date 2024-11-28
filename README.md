# challenge-backend-1

### Prueba Técnica: Simulación de Batalla Pokémon

#### Objetivo
Desarrollar una aplicación en Python que simule una **batalla Pokémon** entre dos Pokémon ingresados como argumento desde la línea de comandos. La información de los Pokémon se deberá obtener de la **PokeAPI (https://pokeapi.co/)** , y se evaluará la implementación basada en **buenas prácticas de programación**.

#### Requisitos Funcionales
1. **Entradas:**
   - La aplicación debe recibir los nombres de **dos Pokémon** como argumentos desde la línea de comandos.
   - Ejemplo: `python3 battle.py pikachu charizard`.

2. **Batalla:**
   - La batalla se desarrollará en **tres turnos** y se calculará el daño eligiendo de forma aleatoria en cada turno una de las dos fórmulas:
     1. `damage = (attack / defense del oponente) * 10`
     2. `damage = (special-attack / special-defense del oponente) * 10`
   - El turno lo inicia el Pokémon con mayor velocidad.
   - Se registrará y mostrará en pantalla lo que sucede en cada turno (ejemplo: "Turno 1: Pikachu ataca a Charizard y causa 35 puntos de daño").
   - La vida total ("HP"), ataque, defensa, ataque especial, defensa especial y velocidad de los Pokémon se obtendrán de "stats" de la API.

3. **Determinación del ganador:**
   - Si uno de los Pokémon pierde todo su HP en algún turno, el otro será declarado ganador.
   - Si después de los tres turnos ambos Pokémon tienen HP restantes, gana el que tenga **más HP restante**.
   - En caso de empate en el HP restante, se declara un empate.

4. **Salidas:**
   - Se debe mostrar en la consola:
     - Información básica de los Pokémon antes de la batalla (nombre, tipo(s), estadísticas relevantes).
     - Registro detallado de los tres turnos (qué Pokémon atacó, cuánto daño infligió, y el estado del HP de ambos).
     - Resultado final: ganador, empate, o error en caso de una batalla incompleta.

#### Requisitos Técnicos
1. **Buenas prácticas:**
   - Uso de **arrow annotations** en todas las funciones y métodos (Obligatorio).
   - Documentación clara utilizando **docstrings** en clases y funciones (Obligatorio).
   - Contrato de datos utilizando **dataclasses** o **Pydantic** para modelar las entidades de Pokémon (Obligatorio).

2. **Estructura del código:**
   - Uso de clases que incluyan métodos públicos y privados para encapsular la lógica de la batalla y la interacción con la API (Obligatorio).
   - Separación de responsabilidades: por ejemplo, una clase para gestionar la interacción con la API y otra para manejar la lógica de la batalla (Opcional).

3. **Diseño:**
   - Modularidad: evita que todo el código resida en un único archivo (Obligatorio).
   - Implementación de patrones de diseño si son necesarios (por ejemplo, Factory o Strategy para manejar el cálculo del daño) (Opcional).

4. **Manejo de errores:**
   - Controlar situaciones como:
     - Pokémon no encontrado.
     - Fallos en la conexión a la API.
     - Estadísticas faltantes o inconsistentes.
   - Mostrar mensajes claros al usuario en caso de errores.


#### Evaluación
Se contemplará en la solución los siguientes aspectos:
1. **Calidad del código:**
   - Legibilidad, uso correcto de métodos públicos y privados, estructura modular.
   - Cumplimiento de los principios SOLID.

2. **Buenas prácticas:**
   - Uso adecuado de anotaciones de tipo, docstrings y contratos de datos.

3. **Manejo de errores y robustez:**
   - Soluciones claras y elegantes para errores comunes.

4. **Diseño y creatividad:**
   - Inclusión de patrones de diseño cuando sea relevante.
   - Implementación lógica de la batalla y cómo se presenta al usuario.

5. **Entrega:**
   - Subir el código a un repositorio de GitHub y enviar el enlace al correo electrónico proporcionado.
   - Archivo `README.md` que explique cómo ejecutar la aplicación, dependencias necesarias, y una breve descripción de la lógica utilizada.

