# Ofrenda de Día de Muertos en el cementerio

**Equipo "Los tilines"** · Grupo 04
Proyecto final de Computación Gráfica e Interacción Humano-Computadora · Semestre 2027-1 · UNAM, Facultad de Ingeniería
Profesor: José Ramón Pérez Athié

---

## Sobre el proyecto

Cada 1 y 2 de noviembre, las familias mexicanas visitan a sus difuntos en los panteones, limpian y decoran sus tumbas y les llevan flores, velas, comida y fotografías. Este proyecto recrea esa noche: un panteón con reja de entrada, un camino de cempasúchil que lleva a una capilla, tumbas arregladas por sus familias, catrinas, una banda de viento y un altar de muertos tradicional, bajo un cielo con luna llena, nubes y niebla.

La escena corre en tiempo real en OpenGL 3.3 con shaders en GLSL: iluminación de Phong con luna, velas y linterna, brillo de Fresnel, niebla, skybox y nueve animaciones que se activan con el teclado.

## Video

Recorrido por la escena y las animaciones: https://youtu.be/aELgFKHT_Xw

## Reportes

- [Reporte final en español](docs/reportes/Reporte_final_ES_Equipo_Tilines.pdf)
- [Final report in English](docs/reportes/Final_report_EN_Team_Tilines.pdf)

## Presentación

La presentación de la exposición está en [docs/presentacion/Presentacion_Equipo_Tilines.pdf](docs/presentacion/Presentacion_Equipo_Tilines.pdf).

## Descarga

El instalador para Windows y la versión portable están en [Releases](https://github.com/VvyasservV/ProyectoBlenderTeoria_OfrendadeDiadeMuertos/releases/latest). Con la versión instalada no hace falta Visual Studio.

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

## Modelos por integrante

| Integrante | Archivos | Modelos |
|---|---|---|
| Yasser | `Modelos/Yasser/` | Flor de cempasúchil, flor baja, pétalos del camino y de tumba, portarretratos, calaverita, guirnalda y guirnalda baja (`flores.blend`, `adornos.blend`, `cosas_familia.blend`), florero, tapetes de cruz y de corazón (`tapetes.blend`), escoba |
| Sebastian | `Modelos/Sebastian/` | Tumba y pan de muerto (`Modelos.blend`), papel picado (`Decoracion.blend`), tumba de tierra, tumba de azulejo y cruz de tumba (`tumbas.blend`), lápida rota, cruz vieja y hierba seca (`zona_vieja.blend`), tapetes de franjas y de vela (`tapetes.blend`), botella |
| Melissa | `Modelos/Melissa/` | Altar, vela, flama y copalero (`altar_con_flamas.blend`), coronas blanca, de corazón, de cruz y de flores (`coronas.blend`), veladora de vaso, silla plegable y cazuela (`cosas_familia.blend`) |

Animaciones hechas en Blender:

| Integrante | Archivos | Animación |
|---|---|---|
| Yasser | `anim_caminar.blend`, `reja_animada.blend` | Hombre que camina (huesos) y reja que se abre (objetos) |
| Sebastian | `anim_abrazar.blend`, `mariposas.blend` | Niño que abraza una tumba (huesos) y mariposas monarca (objetos) |
| Melissa | `anim_rezar.blend`, `humo_copal.blend` | Señora que reza (huesos) y humo de copal (objetos) |

`Modelos/Cargados/` tiene los modelos cargados o generados con IA y adaptados para la escena: escenario con barda y reja, capilla, ángel del dolor, árbol, catrina, platillos del altar (en `modelos_cargados/`), ofrenda tradicional, mausoleo, angelito, xoloitzcuintle, terrazas, cruz atrial, tumba de tierra vieja, cubeta, tapetes de sol, de calavera y de mariposa, coronas amarilla, con banda, de gladiolas y de lágrima, personas y la banda de siete músicos.

## La escena

`Escena/escena_layout.txt` tiene una línea por objeto (`modelo x y z rotY escala [r g b]`) y el programa la lee al arrancar: 1,291 objetos de 72 modelos distintos, con 274 velas, 16 veladoras de vaso y 48 personas. `Escena/escena_preview.blend` muestra la misma escena en Blender, como referencia, y `Escena/preview_*.png` son capturas del programa.

## Cómo colaborar

- Antes de trabajar y antes de subir algo, trae los cambios del equipo (*Fetch origin* y *Pull* en GitHub Desktop).
- Cada quien sube sus propios `.blend`: son binarios y Git no puede juntar cambios hechos al mismo archivo.
- No subas los respaldos de Blender (`*.blend1`, `*.blend2`); ya están en `.gitignore`.
