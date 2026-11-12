# 🎮 SOY SERGIO VACCARO '26 — Mi Mundo 3D Interactivo & Portafolio Web (v2.1.0)

> **Experiencia 3D interactiva en tiempo real (Three.js / WebGL PBR)** narrada **100% en primera persona por Sergio Vaccaro**, inspirada en [`https://samsy.ninja/`](https://samsy.ninja/) y construida directamente a partir de mi archivo original de Blender (`YDRAY-city2.blend`).

---

## 🚀 Cómo Ejecutar el Proyecto

### Opción 1: Ejecución Instantánea (Sin Servidor / Doble Clic)
Abre directamente [`index.html`](file:///c:/Users/Daniel/Desktop/cv%20Sergio/index.html) en cualquier navegador moderno (Chrome, Edge, Brave, Firefox).  
Gracias a [`assets/media_bundle.js`](file:///c:/Users/Daniel/Desktop/cv%20Sergio/assets/media_bundle.js) y [`assets/ydray_city_meshes.js`](file:///c:/Users/Daniel/Desktop/cv%20Sergio/assets/ydray_city_meshes.js), **todas las mallas 3D reales de Blender, los 437 colisionadores físicos, las texturas PBR, el GIF Pixel Art y el loop de mis 4 videos reales están empaquetados sin restricciones CORS (`file://`)**.

### Opción 2: Servidor Local o GitHub Pages
Si deseas subirlo a **GitHub Pages**, simplemente sube el contenido de esta carpeta (`index.html`, `assets/` y `docs/`) a la rama principal de tu repositorio.

---

## ✨ Novedades Principales de la Versión 2.1.0

1. **Comunicación 100% en Primera Persona («Soy Sergio Vaccaro»):**
   - Toda la narrativa del juego, HUD, barra superior (`SOBRE MÍ (SERGIO)`), botón izquierdo (`+ Conóceme (Soy Sergio)`), controles (`MI ESPADA BLENDER`), notificaciones y modales están redactados en **primera persona**, presentando a Sergio Vaccaro como el creador directo de este mundo 3D y de los proyectos proyectados.
2. **Cámara Anti-Oclusión Sin Pared Negra + Mundo `YDRAY-city2.blend` Ampliado (`1,130` Objetos):**
   - Eliminada la caja de niebla volumétrica (`OBCube.052`) que bloqueaba la cámara con una pared negra al retroceder en `Z = 35.1`, y añadido el sistema `clampCameraOutOfWalls()` para que la cámara **jamás pierda visibilidad**.
   - Ampliado el ancho del bulevar (`+14.4m` extra entre fachadas) y la longitud de las manzanas (`1,130` objetos compilados y `145,840` triángulos por lotes).
3. **Colisiones Físicas Reales contra Columnas, Postes y Paredes (`437` Colisionadores AABB):**
   - El personaje ahora se detiene físicamente frente a cada columna, pilar, caja, escalera y pared (`resolveWorldCollisions`), y los bordillos bajos de acera fueron nivelados a ras de suelo para que los pies nunca se hundan.
4. **Corrección de la Gorra `HEADSPACE` y Cabeza Funko Pop (`taperSkullForCap`):**
   - Eliminada la rotación errónea de `-90°` en `headMesh` y aplicado un ahusamiento superior al cráneo bajo la corona de la gorra para que ninguna parte del cráneo sobresalga ni tape la palabra `"HEADSPACE"`.
5. **Pantalla Gigante 3D 100% Despejada con Videos en Loop Continuo (`updateGiantScreenCanvas`):**
   - Eliminada la estructura de puente elevado (`OBCube.029`, `OBCube.375`, `OBCube.399`) que tapaba parte de la pantalla.
   - Decodificación binaria limpia del Base64 de video + renderizado continuo en `<canvas>` 2D (`1280x720`) hacia `THREE.CanvasTexture` para garantizar reproducción fluida en loop en cualquier navegador.
6. **Fantasmas Azules Realmente en Movimiento y Latas White Monster Más Brillantes y Menos Frecuentes:**
   - Los 4 fantasmas azules recorren activamente toda la avenida con velocidad persistente (`4.2 m/s` a `5.8 m/s`) y rebotan físicamente contra columnas y límites.
   - Las latas de **White Monster Energy Ultra** ahora tienen auto-iluminación cian/blanca intensa (`emissiveIntensity: 0.92`, cápsula de brillo y `PointLight` de `3.2`) y aparecen con menor frecuencia (solo 2 latas en el mapa y `38s` de enfriamiento).

---

## 📚 Documentación Técnica Completa (Para Desarrolladores y Otras IAs)

Toda la documentación del proyecto se encuentra en la carpeta [`docs/`](file:///c:/Users/Daniel/Desktop/cv%20Sergio/docs):

1. [**`01_INFORME_TECNICO_Y_ARQUITECTURA.md`**](file:///c:/Users/Daniel/Desktop/cv%20Sergio/docs/01_INFORME_TECNICO_Y_ARQUITECTURA.md) — Arquitectura del sistema, extracción binaria `DNA1` de Blender 5.0 y módulos de `index.html`.
2. [**`02_DISENO_DE_JUEGO_Y_NARRATIVA.md`**](file:///c:/Users/Daniel/Desktop/cv%20Sergio/docs/02_DISENO_DE_JUEGO_Y_NARRATIVA.md) — Controles, diseño Funko Pop de Sergio, fantasmas rojos/azules, latas Monster Ultra y sistema de pausa.
3. [**`03_HISTORIAL_DE_CAMBIOS_CHANGELOG.md`**](file:///c:/Users/Daniel/Desktop/cv%20Sergio/docs/03_HISTORIAL_DE_CAMBIOS_CHANGELOG.md) — Historial detallado de versiones (`v1.0.0` -> `v2.0.0`).
4. [**`04_REGISTRO_DE_PROMPTS_Y_RESULTADOS.md`**](file:///c:/Users/Daniel/Desktop/cv%20Sergio/docs/04_REGISTRO_DE_PROMPTS_Y_RESULTADOS.md) — Registro completo de requerimientos del usuario y soluciones implementadas.
