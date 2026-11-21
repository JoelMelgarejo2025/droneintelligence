# Publicación de DroneIntelligence en Hostinger

## Estado y estructura verificada (21-11-2026)

Repositorio: https://github.com/JoelMelgarejo2025/droneintelligence  
Rama: `main`  
Dominio: https://droneintelligence.space  
Carpeta estática preparada: `public/`

La carpeta `public/` contiene los recursos estáticos de la plataforma existente y ahora incorpora:
- `landing.html`: nueva landing pública.
- `.htaccess`: muestra la landing en la raíz y conserva la entrada anterior de la aplicación en `/app/`.
- `index.html`: aplicación/plataforma existente; no se reemplaza.
- `proyectos.html`, `project-1.webp` a `project-4.webp`, `inter.ttf`, `config.js`.

## Publicación en Hostinger

En hPanel, abrir **Websites → Manage → Advanced → Git** (la ruta puede variar por plan) y configurar el repositorio:
- Repository: `https://github.com/JoelMelgarejo2025/droneintelligence.git`
- Branch: `main`
- Deployment directory: `public` (si el asistente permite elegir directorio de despliegue).

Si Hostinger no permite seleccionar `public/` como directorio, no desplegar la raíz completa del repositorio sobre `public_html`: primero preparar un artefacto que contenga solo los archivos de `public/` y subir ese contenido a `public_html`. Hacer una copia de seguridad del contenido actual antes de reemplazarlo.

Después de desplegar:
1. Abrir `https://droneintelligence.space/` y confirmar que aparece la landing DroneIntelligence.
2. Verificar imágenes, fuente, menú móvil, secciones, FAQ y enlaces.
3. Abrir `https://droneintelligence.space/proyectos.html`.
4. Abrir `https://droneintelligence.space/app/`; la regla de redirección lleva a la entrada anterior `/index.html`.
5. Confirmar HTTPS y que no se haya publicado el backend ni archivos privados.

## Límites importantes

La landing y la galería son estáticas. El backend Python/Flask del repositorio conserva una restricción de acceso local y no implementa autenticación multiusuario. No exponerlo directamente en Internet. YOLO y NodeODM solo funcionarán públicamente después de desplegar un backend de producción con autenticación, CORS limitado, permisos, almacenamiento persistente y servicios configurados.

La publicación del HTML en Hostinger no implica que los endpoints Python estén operativos. No subir TIFF privados, pesos de modelos ni datos de clientes al directorio público.

## Comprobación de entrega

La actualización de GitHub no confirma por sí sola que Hostinger haya ejecutado un despliegue. La verificación final debe hacerse contra el dominio después de que hPanel complete la publicación.
