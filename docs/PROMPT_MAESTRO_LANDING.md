# Prompt maestro — Landing premium de DroneIntelligence

Este documento reúne el brief funcional y visual para recrear o evolucionar la landing de DroneIntelligence con Codex, Cursor, Lovable, Bolt u otro generador de aplicaciones web con IA.

> **Regla de continuidad:** antes de modificar la web, inspecciona la rama `main`, identifica el punto de entrada que realmente se publica y conserva la identidad, los recursos y las funcionalidades que ya existen. No reemplaces el visor ni la aplicación GIS por una maqueta genérica.

## 1. Objetivo

Crear y mantener una landing page premium para **DroneIntelligence**, una plataforma que transforma imágenes capturadas con drones y ortomosaicos en información territorial útil para análisis, monitoreo y toma de decisiones.

Repositorio de referencia: https://github.com/JoelMelgarejo2025/droneintelligence

La landing debe explicar el valor de la plataforma, demostrar capacidades mediante material auténtico y conducir al usuario hacia la aplicación geoespacial.

## 2. Prompt maestro de desarrollo web

Copia el bloque completo y úsalo como instrucción de desarrollo:

---

### PROMPT — DRONEINTELLIGENCE

**OBJETIVO**

Diseña e implementa una landing page premium para **DroneIntelligence**, una plataforma geoespacial que convierte imágenes de drones y ortomosaicos en información territorial. Toma como referencia el repositorio https://github.com/JoelMelgarejo2025/droneintelligence y revisa su implementación actual antes de proponer cambios.

**PRINCIPIOS DE IMPLEMENTACIÓN**

- Mantén la identidad visual y los recursos existentes cuando sean compatibles con la nueva experiencia.
- Separa la landing en componentes reutilizables y mantenibles; evita mezclar toda la interfaz en un único bloque monolítico.
- No rompas ni simules las funciones del visor geoespacial o del backend.
- No inventes clientes, ubicaciones, métricas, resultados de análisis ni nombres de proyectos.
- Reutiliza los cuatro recursos visuales de proyectos disponibles en el repositorio y verifica su contenido antes de asignarles títulos o descripciones.
- Si una función todavía no está conectada a un servicio real, identifícala claramente como demostración o función futura.
- Mantén separadas la landing pública y la aplicación GIS.

**DISEÑO**

- Tema oscuro: negro, grafito y grises, con acentos discretos y alto contraste.
- Tipografía Inter, respetando los archivos de fuente y licencias existentes.
- Estética tecnológica, geoespacial y corporativa; composición limpia, premium y sin efectos visuales excesivos.
- Hero principal con un visor geoespacial o una visualización territorial convincente.
- Navegación sticky, transiciones sutiles y microinteracciones funcionales.
- Diseño responsive para escritorio, tablet y móvil.
- Accesibilidad: navegación por teclado, foco visible, etiquetas semánticas, contraste suficiente y textos alternativos.

**ESTRUCTURA DE SECCIONES**

1. **Hero:** propuesta de valor clara, mensaje orientado a resultados, visual geoespacial y CTA principal para explorar la plataforma.
2. **Plataforma:** explicación de cómo DroneIntelligence transforma ortomosaicos en información territorial consultable.
3. **Seis capacidades:** presenta seis capacidades verificables de la plataforma. Inspecciona el código y documenta las funciones existentes; no atribuyas capacidades que no estén implementadas.
4. **Flujo de trabajo en cuatro pasos:** captura con dron, procesamiento del ortomosaico, análisis/publicación y consulta de resultados. Ajusta los pasos al flujo real del software.
5. **Proyectos:** galería de cuatro proyectos con imágenes auténticas del repositorio. Implementa un selector de proyectos y muestra únicamente datos confirmados. Si faltan metadatos, utiliza etiquetas neutrales como “Proyecto 01” hasta verificarlos.
6. **Tecnología e integraciones:** explica los formatos y herramientas realmente compatibles, incluyendo GeoTIFF, YOLO y NodeODM únicamente en el alcance que confirme el código.
7. **Preguntas frecuentes:** FAQ interactiva, accesible y con respuestas concretas.
8. **CTA final:** invitación a explorar la plataforma mediante la ruta válida de la aplicación (por ejemplo, `/app/` solo si está disponible en el despliegue).

**FUNCIONALIDAD**

- Navegación fluida entre secciones y enlaces internos correctos.
- Pestañas o selector para explorar herramientas/capacidades.
- Selector de proyectos que actualice imagen, título y descripción.
- FAQ interactiva con estados accesibles.
- Botón **“Copiar prompt completo”** que copie el contenido íntegro de este prompt, sin truncarlo ni copiar únicamente el texto visible de un resumen.
- CTA hacia la aplicación geoespacial, comprobando que la ruta exista en el entorno de publicación.
- SEO técnico: título y descripción únicos, jerarquía correcta de encabezados, Open Graph, metadatos, URLs canónicas cuando corresponda, imágenes optimizadas y datos estructurados solo si son veraces.
- Buen rendimiento: imágenes responsivas, carga diferida debajo del primer pantallazo, dimensiones declaradas y JavaScript optimizado.
- Preparar la arquitectura para una futura conexión con la plataforma GIS mediante API, sin exponer secretos ni endpoints privados.

**PROYECTOS Y CONTENIDO**

Antes de redactar las fichas de los cuatro proyectos:

1. Inspecciona las cuatro imágenes de proyecto disponibles.
2. Comprueba si existen metadatos, miniaturas, manifiestos o información asociada en el repositorio.
3. Relaciona cada imagen con su proyecto solo cuando exista evidencia.
4. No publiques coordenadas, nombres de clientes, ubicaciones sensibles ni resultados no autorizados.
5. Si la información no está disponible, conserva identificadores neutrales y deja indicado qué metadato falta.

**INSTRUCCIONES DE ENTREGA**

- Primero analiza la estructura, los estilos, los recursos y las rutas actuales.
- Presenta una lista breve de archivos que se modificarán y por qué.
- Implementa la landing en componentes reutilizables y conserva intacta la aplicación GIS.
- Verifica enlaces, rutas, selector de proyectos, pestañas, FAQ y botón de copiado.
- Comprueba responsive, accesibilidad, consola y rendimiento.
- Entrega una previsualización funcional y un resumen de cambios.
- No publiques ni despliegues automáticamente sin verificar el resultado y confirmar el destino de publicación.

### FIN DEL PROMPT

---

## 3. Archivos de referencia del repositorio

Las rutas compartidas inicialmente (`web/index.html`, `web/app/index.html`, `backend/server.py`) describen una estructura de trabajo anterior o alternativa. **En la rama `main` de este repositorio conectado, la estructura visible está aplanada en la raíz**, por lo que se deben comprobar las rutas reales antes de ejecutar instrucciones.

| Recurso confirmado en la raíz de `main` | Función / observación |
| --- | --- |
| [index.html](../index.html) | Entrada HTML publicada en esta copia. Inspeccionar antes de editar. |
| [project-1.webp](../project-1.webp) | Imagen de proyecto 1. Verificar contenido y metadatos. |
| [project-2.webp](../project-2.webp) | Imagen de proyecto 2. Verificar contenido y metadatos. |
| [project-3.webp](../project-3.webp) | Imagen de proyecto 3. Verificar contenido y metadatos. |
| [project-4.webp](../project-4.webp) | Imagen de proyecto 4. Verificar contenido y metadatos. |
| [inter.ttf](../inter.ttf) y [OFL-Inter.txt](../OFL-Inter.txt) | Fuente Inter y archivo de licencia incluido. |
| [server.py](../server.py) | Código de servidor Python presente en la raíz de esta copia. Revisar rutas y configuración antes de desplegar. |
| [config.js](../config.js) | Configuración JavaScript presente en la raíz. |
| [README.md](../README.md) | Descripción y notas de ejecución del repositorio. |
| [HOSTINGER.md](../HOSTINGER.md) | Notas sobre publicación y separación entre landing y backend. |
| [REPLICAR.md](../REPLICAR.md) | Notas sobre réplica entre repositorios/cuentas. |

La estructura descrita en algunos documentos (`web/`, `web/app/`, `web/landing-assets/`, `backend/`) no coincide con el listado actual de la raíz conectada. No se deben asumir esas rutas ni crear enlaces hacia ellas sin verificar primero la rama y el contenido correspondiente.

## 4. Criterio para los cuatro proyectos reales

La galería debe usar los cuatro archivos de imagen que ya están en el repositorio, no fotografías de stock ni imágenes generadas que se presenten como trabajos reales. Sin metadatos comprobables no se debe inventar el nombre, la ubicación, el cliente, el área ni los resultados de cada proyecto.

## 5. Recomendación de arquitectura

Mantén la landing como una capa de presentación independiente del software geoespacial. Organiza secciones, tarjetas, pestañas, FAQ y galería en componentes reutilizables; centraliza textos y metadatos de proyectos en una fuente de datos fácil de actualizar; y encapsula la futura conexión GIS en un servicio/API.

La landing debe poder evolucionar sin reescribir el visor ni alterar el procesamiento de GeoTIFF, los modelos o los datos privados. Antes de conectar servicios, revisa autenticación, permisos, CORS, almacenamiento y despliegue seguro del backend.
