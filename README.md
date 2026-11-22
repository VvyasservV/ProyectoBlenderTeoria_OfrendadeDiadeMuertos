# Ofrenda de Día de Muertos en el cementerio

**Equipo "Los tilines"** · Grupo 04
Proyecto final de Computación Gráfica e Interacción Humano-Computadora · Semestre 2027-1 · UNAM, Facultad de Ingeniería
Profesor: José Ramón Pérez Athié

---

## Sobre el proyecto

Cada 1 y 2 de noviembre, las familias mexicanas visitan a sus difuntos en los panteones, limpian y decoran sus tumbas y les llevan flores, velas, comida y fotografías. Este proyecto recrea esa noche: un panteón con reja de entrada, un camino de cempasúchil que lleva a una capilla, tumbas arregladas por sus familias, catrinas, una banda de viento y un altar de muertos tradicional, bajo un cielo con luna llena, nubes y niebla.

La escena corre en tiempo real en OpenGL 3.3 con shaders en GLSL: iluminación de Phong con luna, velas y linterna, brillo de Fresnel, niebla, skybox y nueve animaciones que se activan con el teclado.

## Integrantes

| Nombre | No. de cuenta |
|---|---|
| Yasser Vladimir Cruz Miranda | 424039512 |
| Sebastian Andre Fuentes Poma | 620271005 |
| Alejandra Melissa Saucedo Serralde | 320284858 |

## Cómo correr el proyecto

1. Clona el repositorio.
2. Abre `OpenGL/ProyectoFinal.slnx` en Visual Studio 2026 (con el desarrollo de escritorio en C++).
3. Elige **Release** y **x86**.
4. Ejecuta con Ctrl+F5. La escena tarda unos segundos en cargar.

El directorio de trabajo tiene que ser la carpeta `OpenGL/`, porque ahí están `assets/` y `shaders/`. Los detalles del código están en [`OpenGL/README.md`](OpenGL/README.md).

## Controles

| Tecla | Acción |
|---|---|
| W A S D / flechas | Mover la cámara |
| Ratón | Mirar alrededor |
| F | Linterna |
| V | Prender o apagar las velas |
| R | Brillo de Fresnel |
| N | Niebla |
| + / - | Subir o bajar la luz de la luna |
| 1 | Hombre que camina (huesos) |
| 2 | Señora que reza (huesos) |
| 3 | Niño que abraza una tumba (huesos) |
| 4 | Reja que se abre |
| 5 | Mariposas monarca |
| 6 | Humo de copal |
| 7 | Banda de viento |
| 8 | Niño que saluda |
| 9 | Viento en el papel picado |
| Esc | Salir |

## Estructura del repositorio

```
├── Modelos/     # Archivos .blend: una carpeta por integrante y Cargados/
├── Texturas/    # Imágenes de los materiales de los .blend
├── Shaders/     # Shaders de referencia (skybox, niebla, modelo base)
├── Escena/      # Acomodo de la escena y vista previa en Blender
├── OpenGL/      # Proyecto de Visual Studio con la escena completa
└── README.md
```

Los `.blend` usan rutas relativas a `Texturas/`, así que hay que conservar la estructura de carpetas. Los modelos chicos del mismo tipo están juntos en un archivo, cada uno en su colección con el nombre que usa OpenGL.

## Cómo colaborar

- Antes de trabajar y antes de subir algo, trae los cambios del equipo (*Fetch origin* y *Pull* en GitHub Desktop).
- Cada quien sube sus propios `.blend`: son binarios y Git no puede juntar cambios hechos al mismo archivo.
- No subas los respaldos de Blender (`*.blend1`, `*.blend2`); ya están en `.gitignore`.
