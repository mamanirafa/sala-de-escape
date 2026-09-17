# Circuito Cerrado — Guía docente

**Sala de escape digital · Educación Tecnológica · 3.º año Ciclo Básico (14–15 años)**
Duración estimada: 40 minutos de juego + 15 de puesta en común.
Modalidad: individual, cada estudiante en su PC o celular. No pide registro ni datos personales.

---

## 1. Qué es y qué evalúa

Ocho estaciones, una por eje de contenido. Cada estación resuelta entrega una **palabra clave**; la **inicial de cada palabra, en el orden en que se consiguieron**, arma el código de salida.

| # | Estación | Contenido | Palabra clave | Inicial |
|---|----------|-----------|---------------|---------|
| 01 | Taller de componentes | Reconocer componentes reales y su función | CONDENSADOR | **C** |
| 02 | Panel de simbología | Símbolos normalizados e instrumentos de medición | INTERRUPTOR | **I** |
| 03 | Banco de circuitos | Serie / paralelo, circuito abierto y cerrado | RAMA | **R** |
| 04 | Sala de control | Lazo abierto vs. cerrado, sensor, actuador | CERRADO | **C** |
| 05 | La placa del laboratorio | Partes de una placa Arduino Uno | USB | **U** |
| 06 | El semáforo del pasillo | Cablear 3 LEDs + completar el sketch | INTERVALO | **I** |
| 07 | Alarma de proximidad | Cablear HC-SR04 y zumbador + lógica de distancias | TRIGGER | **T** |
| 08 | Servidor de BIT-3 | IA generativa, tipos de IA, riesgos | ORIGEN | **O** |

> **Código final en el orden normal: C I R C U I T O**

El nivel es de reconocimiento y aplicación simple. No hay Ley de Ohm ni cálculos.

---

## 2. Qué cambia en cada partida

El juego **nunca se juega igual dos veces**:

- **Preguntas al azar.** Cada estación tiene un banco de 8 a 10 desafíos y en cada partida se sortean solo los que se juegan (4 en las estaciones de reconocimiento, 3 en circuitos e IA). Nadie recibe la misma combinación.
- **Opciones barajadas.** En las preguntas de opción múltiple la respuesta correcta cambia de lugar; en los tableros de componentes y símbolos las piezas cambian de posición.
- **Ítems sorteados.** En las consignas de clasificar, los casos salen de un conjunto mayor del que se muestra.
- **Orden de estaciones (opcional).** En la pantalla de inicio hay una casilla: **“Mezclar el orden de las estaciones”**. Activada, cada jugador recorre las estaciones en otro orden, así que **cada uno obtiene un código de salida distinto y copiarse no sirve**. Desactivada, el código siempre es CIRCUITO, que es más cómodo si querés cerrar la clase con una sola palabra en el pizarrón.

Recomendación: para trabajo en clase, activar la mezcla. Para una demostración o un cierre grupal, dejarla desactivada.

---

## 3. Los tres desafíos interactivos

**05 · La placa del laboratorio.** Se muestra una placa Arduino Uno dibujada desde arriba. El estudiante toca la parte que se le pide: puerto USB, jack de alimentación, pines digitales, entradas analógicas, pines de alimentación, botón de reset, microcontrolador y LED integrado “L”.

**06 · El semáforo del pasillo.** Dos pasos.
1. *Cableado.* Se toca un terminal y después el otro, y el cable se tiende solo, con color, estilo Tinkercad. Hay que hacer 6 conexiones: cada LED (+) a su pin digital (13 rojo, 12 amarillo, 11 verde) y cada LED (–) a GND. Los tres negativos pueden compartir el mismo GND. Cada LED ya trae dibujada su resistencia de 220 Ω: buena oportunidad para explicar por qué está ahí.
2. *Programa.* Un sketch de Arduino con cuatro huecos desplegables: `OUTPUT`, `HIGH`, `delay` y `LOW`. Se comprueba con un botón y los huecos mal quedan marcados en rojo.

**07 · Alarma de proximidad.** Tres pasos.
1. *Cableado* del HC-SR04 (VCC→5V, GND→GND, Trig→pin 9, Echo→pin 8) y del zumbador (+→pin 6, –→GND).
2. *Lógica:* asignar cada rango de distancia a su aviso — menos de 10 cm → LED rojo y zumbador; entre 10 y 25 cm → amarillo; más de 25 cm → verde.
3. *Concepto:* cómo mide el sensor (pulso de ultrasonido y tiempo del eco).

En los dos cableados: si la conexión no corresponde, el terminal parpadea en rojo y no pasa nada más — se puede probar sin miedo. La lista de la derecha va tildando lo que ya está conectado.

---

## 4. Flujo de trabajo para implementarlo

### Antes de la clase (15 min, una sola vez)
1. Jugalo completo una vez, con la mezcla activada, para ver la variedad del banco de preguntas.
2. Elegí cómo lo repartís: **link** (aula virtual o QR proyectado) o **archivo** (`circuito-cerrado.html` subido al aula virtual; se abre sin internet una vez descargado).
3. Papel y lapicera por estudiante para anotar las palabras clave. Escribir a mano obliga a releer.

### Durante la clase (55 min)
| Momento | Tiempo | Qué hacés |
|---|---|---|
| Encuadre | 5 min | Contás la historia y mostrás dónde se anotan las palabras. **No** explicás los contenidos antes: el juego es el disparador. |
| Juego | 35–40 min | Circulás. No des respuestas: mandá a usar **Pedir una pista**. Anotá qué estación traba a más estudiantes. |
| Cierre | 10–15 min | Puesta en común sobre lo que se trabó. Ahí va la explicación formal. |

### Después
- Quien termina antes ayuda a otro sin decirle la respuesta.
- Las estaciones donde más se pidió pista son tu diagnóstico para la clase siguiente.
- Como cada partida es distinta, el mismo juego sirve de repaso semanas después.

### Preguntas de cierre sugeridas
1. ¿Por qué las luces del aula están en paralelo y no en serie?
2. En el semáforo, ¿qué pasaría si borráramos todos los `delay()`?
3. ¿Qué aparato de tu casa es de lazo cerrado? ¿Cómo se da cuenta de lo que pasa?
4. ¿Alguna vez una IA te dio un dato falso? ¿Cómo lo verificarías?

---

## 5. Solucionario

Las respuestas correctas están **siempre en primer lugar** dentro del archivo (el programa las baraja al mostrarlas), así que se leen fácil abriendo el HTML y buscando `pool:`.

**01 Componentes** — resistencia (limita), LED (polaridad), pulsador (no queda trabado), motor (movimiento), capacitor (guarda carga), zumbador (sonido), pila (fuente), potenciómetro (resistencia variable), LDR (sensor de luz).

**02 Simbología** — pila (rayas larga/corta), lámpara (círculo con cruz), interruptor (palanca), amperímetro (A, en serie), voltímetro (V, en paralelo), resistencia (rectángulo), motor (M), tierra (tres rayas), zumbador (campana), LED (triángulo con flechas).

**03 Circuitos** — en serie se apagan todas; en paralelo solo la que se sacó; circuito abierto no conduce; partes mínimas: fuente, conductores y receptor; en paralelo cada rama recibe la tensión completa; el fusible protege cortando; cortocircuito = camino sin receptor.

**04 Control** — lazo cerrado = sensor + realimentación. Abierto: tostadora, lámpara con interruptor, semáforo de tiempo fijo, microondas. Cerrado: termostato, riego con sensor, control crucero, portón con sensor.

**05 Placa** — USB (programa y alimenta), jack (fuente externa 7–12 V), pines digitales (HIGH/LOW), analógicos A0–A5 (0 a 1023), POWER (5V, 3.3V, GND), reset, microcontrolador, LED “L” del pin 13.

**06 Semáforo** — conexiones: rojo+→13, amarillo+→12, verde+→11, los tres negativos a GND. Código: `OUTPUT`, `HIGH`, `delay`, `LOW`.

**07 Alarma** — VCC→5V, GND→GND, Trig→9, Echo→8, zumbador+→6, zumbador–→GND. Distancias: <10 cm rojo y zumbador, 10–25 cm amarillo, >25 cm verde. Mide con el tiempo del eco.

**08 IA** — generativa crea contenido nuevo; alucinación; no cargar datos personales; sesgo por los datos de entrenamiento; aprende de datos; uso honesto = revisar y aclarar; deepfake; predice lo más probable, no verifica. Ya existen: recomendador, asistente de texto, auto autónomo. Ciencia ficción: máquina con conciencia propia.

---

## 6. Rúbrica breve (opcional, 10 puntos)

| Criterio | 1–4 | 5–7 | 8–10 |
|---|---|---|---|
| Resolución | Completó hasta 3 estaciones | Completó 4 a 6 | Completó las 8 y abrió la puerta |
| Autonomía | Necesitó respuestas | Usó las pistas del juego | Resolvió con pistas mínimas |
| Cableado (est. 6 y 7) | Conectó por prueba y error | Conectó con la pista | Explica por qué cada pata va donde va |
| Transferencia (cierre oral) | No justifica | Justifica con un ejemplo del juego | Aporta un ejemplo propio |

Sugerencia: calificar el **cierre oral**, no el tiempo. El reloj da ritmo, no penaliza.

---

## 7. Adaptaciones rápidas

- **Por parejas:** una computadora cada dos, con roles rotativos. Sube la discusión, baja la ansiedad.
- **Proyectado:** funciona en pantalla grande con la clase votando; los cableados se resuelven de a uno pasando al frente.
- **Menos tiempo:** en el archivo, bajá el valor `n:` de cada estación (por ejemplo de `n:4` a `n:2`) y el juego pide menos desafíos por estación.
- **Puente al taller real:** después de la estación 6 o 7, armar el mismo circuito con componentes reales o en un simulador. El dibujo del juego respeta las conexiones verdaderas.

---

## 8. Cómo modificar el contenido

Es un único archivo HTML. Abrilo con un editor de texto y buscá `var SALAS = [`. Cada estación tiene:

```js
{
  titulo:"Taller de componentes",
  palabra:"CONDENSADOR",   // su inicial entra al código final
  cierre:"explicación al ganar la palabra",
  n:4,                     // cuántos desafíos se sortean del banco
  pool:[ ... ],            // banco de desafíos (se mezcla en cada partida)
  fijos:[ ... ]            // desafíos que aparecen siempre, al final
}
```

Tipos de desafío disponibles:

| Tipo | Para qué sirve | Campos |
|---|---|---|
| `pick` | Tocar la pieza o el símbolo correcto | `ans`, `txt`, `pista`, `ok` |
| `hot` | Tocar una parte de la placa Arduino | `ans`, `txt`, `pista`, `ok` |
| `choice` | Opción múltiple — **la correcta va primera** y se baraja sola | `ops`, `txt`, `pista`, `ok` |
| `clasif` | Clasificar ítems en 2 o 3 categorías | `labels`, `items` (`t`, `a`, `why`), `take` |
| `cablear` | Cableado interactivo | `escena` ("semaforo" u "ultrasonido") |
| `codigo` | Completar los huecos del sketch | `huecos` (`ops`, `ans`) |

Otros ajustes útiles: `var TIEMPO = 40*60;` cambia el reloj; en `escenaSemaforo()` y `escenaUltrasonido()` el arreglo `req` define qué conexiones se piden (cambiar un pin es cambiar un valor). Si cambiás una `palabra`, el código final se recalcula solo.

Todos los dibujos —componentes, símbolos, circuitos, la placa Arduino, el semáforo, el sensor y los cables— son SVG originales escritos dentro del archivo: no hay imágenes externas y el juego funciona sin conexión.

---

*Material de aula. Textos e ilustraciones originales, libres de reutilizar y adaptar en contextos educativos.*
