# DroneIntelligence

Landing pública premium y plataforma geoespacial para trabajar con imágenes de drones, ortomosaicos y datos raster.

## Publicación estática

La rama `main` contiene una carpeta `public/` preparada para Hostinger:
- `public/landing.html`: landing pública de DroneIntelligence.
- `public/.htaccess`: configura la landing como página principal y deriva `/app/` a la aplicación existente.
- `public/index.html`: aplicación/plataforma existente; se conserva sin reemplazar.
- `public/proyectos.html`: galería de proyectos.
- `public/project-1.webp` a `public/project-4.webp`: recursos visuales de la galería y landing.
- `public/inter.ttf`: tipografía Inter.
- `public/config.js`: configuración del endpoint API.

**Configuración recomendada en Hostinger:** repositorio `JoelMelgarejo2025/droneintelligence`, rama `main`, directorio de despliegue `public` (si el plan permite elegirlo). No desplegar todo el repositorio en `public_html`, porque también contiene backend y documentación.

Dominio previsto: https://droneintelligence.space

Consulta [HOSTINGER.md](HOSTINGER.md) para el procedimiento de publicación y verificación. Un commit en GitHub no demuestra que Hostinger haya desplegado los cambios: hay que comprobar el dominio después del despliegue.

## Capacidades implementadas en el backend

El código Python contempla:
- lectura y visualización de ortomosaicos GeoTIFF RGB con CRS;
- reproyección y generación de vistas/teselas raster;
- biblioteca de proyectos y vistas previas;
- inferencia YOLO cuando Ultralytics y un modelo local están instalados;
- envío de fotografías a NodeODM, seguimiento de tareas y descarga de ortomosaicos.

## Seguridad y límites de despliegue

El backend Flask actual está limitado a localhost y no incorpora autenticación multiusuario. No exponerlo directamente en Internet. Para habilitar funciones de procesamiento desde la web pública hace falta un backend de producción con autenticación, CORS limitado, permisos, almacenamiento persistente y servicios configurados.

La landing estática puede publicarse por separado. La publicación de HTML no significa que los endpoints Python, YOLO o NodeODM estén activos en el dominio. No colocar TIFF privados, pesos de modelos ni datos de clientes en el directorio público.

## Ejecución local

Revisa las rutas y dependencias de la versión local antes de ejecutar el backend. Los datos, modelos y proyectos privados deben mantenerse fuera del repositorio público.
