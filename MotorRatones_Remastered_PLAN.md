# MOTORRATONES — REMASTERED
## Plan maestro del proyecto — PC / uso personal

**Estado:** Fase 1 — Desarrollo de activos 3D  
**Última actualización:** 2026-09-13  
**Dirección del proyecto:** Willy + ChatGPT  
**Objetivo:** Crear un videojuego personal para PC inspirado en la nostalgia de *Biker Mice from Mars*, modernizado con estética 3D actual, nuevas pistas, motos y gameplay arcade de carreras + combate.

---

# 1. Visión del proyecto

Crear una versión moderna, personal y no comercial de los Motorratones, tomando como punto de partida la sensación del videojuego clásico y llevándola a una experiencia actual para PC.

La idea NO es hacer inicialmente un remake AAA ni reproducir exactamente el juego original.

La dirección es:

- esencia noventera
- personajes 3D modernos
- motos rediseñadas
- pistas nuevas
- carreras arcade
- combate
- turbo
- saltos y rampas
- rivales controlados por IA
- 1 jugador
- 2 jugadores local
- teclado y mando
- menú moderno
- garaje
- campeonato
- contenido clásico incorporado posteriormente

---

# 2. Filosofía de desarrollo

Willy no necesita programar directamente.

El proyecto se construirá por etapas, con herramientas visuales y asistencia de IA para generación de modelos, imágenes, animaciones y código.

Principio técnico:

> Primero crear y validar los activos. Después construir un prototipo jugable. Finalmente ampliar contenido.

No intentar crear todo el juego de una sola vez.

---

# 3. Stack propuesto

## Arte / 3D

- Generación de concept art con IA
- Image-to-3D / Multi-view-to-3D
- Hunyuan 3D / servicio web equivalente
- Blender para limpieza y preparación
- GLB/GLTF como formato principal para el juego
- FBX como formato intermedio cuando alguna herramienta lo requiera
- OBJ como formato auxiliar/intercambio
- STL NO es el formato objetivo del videojuego

## Motor

Primera opción propuesta:

- Godot 4

Alternativa:

- Unity

La decisión definitiva del motor se tomará durante el prototipo.

---

# 4. Pipeline general

```text
CONCEPTO 2D
    ↓
HOJA DE REFERENCIA / TURNAROUND
    ↓
IMAGE-TO-3D
    ↓
MODELO 3D
    ↓
REVISIÓN DE GEOMETRÍA Y TEXTURAS
    ↓
BLENDER
    ↓
RETROPOLOGÍA / UV / MATERIALES
    ↓
RIG
    ↓
ANIMACIONES
    ↓
EXPORTACIÓN GLB/GLTF
    ↓
MOTOR DEL JUEGO
    ↓
GAMEPLAY
```

---

# 5. Estado actual — VINNIE

## Modelo 3D

**Estado: GENERADO**

Ya existe un primer modelo 3D de Vinnie.

Características observadas:

- cuerpo coherente
- manos coherentes
- cara coherente
- proporciones coherentes
- apariencia consistente
- modelo en posición normal/neutra
- aparentemente sin errores graves visibles
- posible textura incluida, pendiente de comprobar técnicamente
- pequeño problema con el logo, considerado de baja prioridad

El logo NO es actualmente un bloqueo.

En el juego el personaje tendrá una escala relativamente pequeña y el logo no necesita ser perfecto en esta primera iteración.

## Lo que todavía falta en Vinnie

- comprobar si el modelo tiene texturas
- comprobar materiales
- comprobar calidad de la malla
- comprobar número de polígonos
- comprobar orientación/ejes
- comprobar escala
- revisar partes ocultas
- preparar el modelo para rigging
- crear esqueleto
- crear animaciones
- crear expresiones si realmente son necesarias
- crear la moto independiente
- integrar personaje + moto

---

# 6. Regla visual importante — VINNIE

Para ESTE proyecto:

> VINNIE = ROJO

La identidad visual de Vinnie será roja.

Principalmente:

- moto roja
- detalles rojos de vestuario
- accesorios rojos
- elementos visuales asociados al personaje en rojo

No debemos permitir que una IA cambie accidentalmente la identidad cromática de Vinnie a verde por asociación con versiones anteriores.

---

# 7. Personajes principales

## Héroes

### 01 — Vinnie
Estado:
- Concepto: avanzado
- Modelo 3D: GENERADO
- Rig: pendiente
- Animaciones: pendientes
- Moto: pendiente

### 02 — Throttle
Estado:
- Concept art: definido
- Modelo 3D: pendiente

### 03 — Modo
Estado:
- Concept art: definido
- Modelo 3D: pendiente

## Villanos

Inicialmente se trabajará con cuatro personajes enemigos.

Estado:
- diseño visual: pendiente de consolidación
- hojas maestras: pendientes
- modelos 3D: pendientes

Los personajes clásicos/adicionales se incorporarán al final como contenido nostálgico.

---

# 8. Producción correcta de cada personaje

Cada personaje debe tener una hoja maestra antes de generar su modelo 3D.

## Turnaround mínimo

- frontal
- espalda
- lateral izquierdo
- lateral derecho
- 3/4 frontal
- 3/4 posterior

## Información adicional

- cabeza
- expresiones
- manos
- botas
- ropa
- accesorios
- materiales
- paleta de colores
- detalles importantes

## Para generación 3D

La imagen debe priorizar:

- consistencia anatómica
- silueta
- proporciones
- geometría interpretable
- iluminación uniforme
- fondo neutro
- ausencia de perspectiva extrema
- personaje aislado
- pose neutra/A-pose/T-pose cuando corresponda

No usar una imagen cinematográfica como única referencia para reconstrucción 3D.

---

# 9. Motos

Cada moto se tratará como un activo 3D independiente.

## Hoja maestra de moto

- frontal
- posterior
- lateral izquierdo
- lateral derecho
- superior
- inferior
- 3/4 frontal
- 3/4 posterior
- cockpit
- tablero
- ruedas
- suspensión
- escape
- luces
- detalles mecánicos
- materiales
- paleta

## Estructura conceptual

```text
VINNIE
    └── Character

VINNIE_MOTO
    └── Motorcycle
```

No fusionar permanentemente personaje y moto durante la fase de producción.

Esto facilita:

- animación
- física
- cambios de moto
- mantenimiento
- optimización
- reutilización

---

# 10. Primer objetivo jugable — VERTICAL SLICE

Antes de crear siete personajes y muchas pistas:

## VERTICAL SLICE 01

Debe contener solamente:

- Vinnie
- moto de Vinnie
- una pista
- cámara
- aceleración
- frenado
- dirección
- turbo
- derrape
- salto
- colisiones
- HUD
- vueltas
- posición
- velocidad
- al menos algunos rivales/obstáculos

Objetivo:

> Poder arrancar el juego, elegir a Vinnie, conducir su moto por una pista y terminar una carrera.

Si esto funciona, el proyecto deja de ser solamente conceptual y pasa a ser un videojuego real en desarrollo.

---

# 11. Orden recomendado desde el estado actual

## FASE 1 — Activos

### Paso 1
Validar el modelo 3D de Vinnie.

Revisar:

- ¿Tiene textura?
- ¿Tiene materiales?
- ¿Qué formato entrega?
- ¿Cuántos polígonos tiene?
- ¿La malla está cerrada/coherente?
- ¿Se puede riggear?
- ¿Qué escala tiene?
- ¿Hay partes defectuosas?

### Paso 2
Preparar Vinnie para rigging.

### Paso 3
Crear la moto de Vinnie en una hoja maestra independiente.

### Paso 4
Generar la moto 3D.

### Paso 5
Preparar personaje + moto.

### Paso 6
Crear las primeras animaciones.

---

# 12. Animaciones iniciales de Vinnie

No necesitamos cientos de animaciones.

Primera tanda:

- idle
- montar moto
- desmontar
- acelerar
- frenar
- girar izquierda
- girar derecha
- derrape
- salto
- aterrizaje
- turbo
- recibir golpe
- caída
- victoria
- derrota

Las animaciones específicas de combate se añadirán después.

---

# 13. Sistema de personajes

No crear un sistema completamente diferente para cada personaje.

Conceptualmente:

```text
CharacterBase
├── Mesh
├── Skeleton
├── Animations
├── Stats
├── Motorcycle
├── Attacks
├── Effects
└── AI
```

Después:

```text
Vinnie  → CharacterBase
Throttle → CharacterBase
Modo     → CharacterBase
Villano1 → CharacterBase
Villano2 → CharacterBase
...
```

Cada personaje tendrá:

- modelo propio
- moto propia
- estadísticas propias
- animaciones propias
- ataques propios cuando corresponda

Pero compartirán la estructura principal.

---

# 14. Estadísticas iniciales

Sistema arcade sencillo.

Variables posibles:

- velocidad máxima
- aceleración
- manejo
- frenado
- peso
- turbo
- resistencia

Ejemplo inicial:

| Personaje | Velocidad | Aceleración | Manejo | Peso |
|---|---:|---:|---:|---:|
| Vinnie | ★★★★ | ★★★★★ | ★★★★★ | ★★ |
| Throttle | ★★★★★ | ★★★★ | ★★★★ | ★★★ |
| Modo | ★★★ | ★★★ | ★★★ | ★★★★★ |

Estos valores son provisionales y se balancearán jugando.

---

# 15. Primera pista

No empezar con un mundo abierto.

Primera pista:

- circuito cerrado
- duración corta
- varias curvas
- rectas
- rampas
- obstáculos
- zonas de turbo
- posibilidad de adelantamiento
- atajos opcionales

La primera pista sirve para probar el gameplay, no para demostrar todo el contenido artístico.

---

# 16. Menú principal

Dirección visual ya definida.

Conceptualmente:

```text
BIKER MICE FROM MARS
THE GAME
REMASTERED

JUGAR
UN JUGADOR
DOS JUGADORES
CONFIGURACIÓN
EXTRAS
SALIR
```

## Configuración

- teclado
- mando
- audio
- gráficos
- volumen música
- volumen efectos
- sensibilidad
- vibración cuando corresponda
- resolución
- calidad gráfica

## Controles

Primera implementación:

### Teclado

- acelerar
- frenar
- izquierda
- derecha
- turbo
- ataque
- pausa

Posteriormente:

- mando Xbox/PC
- configuración remapeable

---

# 17. Modos de juego previstos

## Un jugador

- carrera rápida
- campeonato
- contrarreloj
- posiblemente modo historia

## Dos jugadores

Inicialmente:

- pantalla dividida/local

Online NO es prioridad inicial.

---

# 18. Gameplay

Dirección principal:

> Carreras arcade + combate.

Elementos:

- velocidad
- curvas
- derrape
- turbo
- saltos
- ataques
- obstáculos
- rivales
- atajos
- pickups/power-ups si funcionan con el diseño

La conducción debe sentirse divertida antes que realista.

---

# 19. IA de rivales

Después de que Vinnie pueda conducir correctamente:

- waypoint system
- seguimiento de pista
- adelantamientos
- recuperación después de choque
- dificultad
- comportamiento diferente por personaje
- ataques

No construir IA compleja antes de tener conducción funcional.

---

# 20. Pistas futuras

Después del primer circuito:

- pistas futuristas
- Marte
- ciudad nocturna
- zonas industriales
- desiertos
- túneles
- autopistas
- escenarios inspirados en la estética original

Las pistas clásicas se recrearán/adaptarán posteriormente como contenido nostálgico.

---

# 21. Prioridades

## PRIORIDAD CRÍTICA

1. Vinnie 3D
2. Vinnie correctamente preparado
3. Moto de Vinnie
4. conducción
5. primera pista
6. cámara
7. carrera funcional

## PRIORIDAD ALTA

8. HUD
9. IA básica
10. menú
11. Throttle
12. Modo
13. combate

## PRIORIDAD MEDIA

14. villanos
15. nuevas pistas
16. garaje
17. campeonato
18. pantalla dividida

## PRIORIDAD BAJA / FINAL

19. contenido clásico
20. extras
21. secretos
22. personalización avanzada
23. online, si alguna vez se desea

---

# 22. Regla de alcance

No agregar una característica grande solamente porque "sería chévere".

Cada nueva característica debe responder:

1. ¿Mejora el gameplay?
2. ¿Es necesaria?
3. ¿Podemos implementarla sin romper lo existente?
4. ¿Vale el tiempo?

El objetivo es terminar un juego pequeño y divertido antes que diseñar un juego gigantesco imposible de terminar.

---

# 23. Estado actual resumido

```text
CONCEPTO VISUAL                 ██████████ 100%
INTERFAZ PRINCIPAL              ██████████ 100%
DIRECCIÓN ARTÍSTICA              ██████████ 100%

VINNIE CONCEPT                   ██████████ 100%
VINNIE 3D                        ████████░░  80%
VINNIE TEXTURAS/MATERIALES       ████░░░░░░  pendiente de revisión
VINNIE RIG                       ░░░░░░░░░░   0%
VINNIE ANIMACIONES               ░░░░░░░░░░   0%

MOTO VINNIE                      ░░░░░░░░░░   0%
PRIMERA PISTA                    ░░░░░░░░░░   0%
CONDUCCIÓN                       ░░░░░░░░░░   0%
IA                               ░░░░░░░░░░   0%
COMBATE                          ░░░░░░░░░░   0%

THROTTLE                         ░░░░░░░░░░   0%
MODO                             ░░░░░░░░░░   0%
VILLANOS                         ░░░░░░░░░░   0%
```

Los porcentajes son orientativos y no representan métricas técnicas exactas.

---

# 24. PRÓXIMO PASO INMEDIATO

**NO hacer todavía los otros seis personajes.**

Primero:

### Vinnie 3D → validación técnica

Necesitamos conocer:

- formato del archivo
- si contiene textura
- si contiene materiales
- cantidad de polígonos
- tamaño de las texturas
- orientación
- escala
- posibilidad de rigging

Después:

### Vinnie → rig → animaciones básicas

En paralelo:

### Vinnie Moto → hoja maestra → 3D

Después:

### Vinnie + Moto → Godot → primera pista

---

# 25. Regla para continuar el proyecto en un chat nuevo

Este archivo es la memoria operativa del proyecto.

Cuando se abra un nuevo chat:

1. cargar este MD
2. revisar la sección "Estado actual"
3. continuar desde "Próximo paso inmediato"
4. no repetir fases ya terminadas
5. actualizar este archivo cuando cambie una fase importante

Formato de actualización:

```text
FECHA:
FASE:
COMPLETADO:
PENDIENTE:
PROBLEMAS:
DECISIONES:
SIGUIENTE PASO:
```

---

# 26. Registro de decisiones

### Decisión 001
Proyecto destinado inicialmente a PC y uso personal.

### Decisión 002
Formato principal de modelos para juego: GLB/GLTF.

### Decisión 003
STL no será utilizado como formato principal.

### Decisión 004
Vinnie será el primer personaje completamente desarrollado.

### Decisión 005
Vinnie tendrá identidad cromática ROJA.

### Decisión 006
Personaje y moto se producirán como activos independientes.

### Decisión 007
Primero se construirá un vertical slice antes de producir todo el contenido.

### Decisión 008
El primer vertical slice tendrá Vinnie + moto + una pista.

### Decisión 009
El juego será inicialmente arcade de carreras + combate.

### Decisión 010
Los contenidos clásicos se añadirán después de que la versión moderna sea jugable.

---

# 27. Nota de propiedad intelectual

El proyecto se plantea como un proyecto personal/no comercial inspirado en la nostalgia de la franquicia.

Si en algún momento se quisiera distribuir, publicar, monetizar o comercializar públicamente el juego, habría que revisar los derechos correspondientes y cambiar el planteamiento si fuese necesario.

---

# OBJETIVO FINAL

```text
          CONCEPTO
             ↓
        PERSONAJES 3D
             ↓
           MOTOS
             ↓
          ANIMACIÓN
             ↓
        PRIMER CIRCUITO
             ↓
          GAMEPLAY
             ↓
        IA + COMBATE
             ↓
       7 PERSONAJES
             ↓
        VARIAS PISTAS
             ↓
      CAMPEONATO / 2P
             ↓
    CONTENIDO CLÁSICO
             ↓
       MOTORRATONES
        REMASTERED
```

**Principio rector:**

> Primero hacemos que una sola rata pueda correr y divertirse. Después hacemos que corran las siete.
