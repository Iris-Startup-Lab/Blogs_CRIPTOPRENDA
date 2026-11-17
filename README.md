# CriptoPrenda · 4 blogs en HTML para integración

## Qué contiene
Cuatro artículos convertidos desde los documentos entregados (DOCX para blogs 1–3; PDF para blog 4), sus 16 imágenes JPG y una hoja de estilos común. Cada blog se puede abrir localmente con `index.html` y su estructura se puede revisar en GitHub. **No se ha comprobado la compatibilidad con el CMS o framework de producción de CriptoPrenda.**

## Estructura
```
blogs/<slug>/index.html        Página HTML de cada artículo
blogs/<slug>/images/*.jpg      Imágenes locales de ese artículo
assets/css/blog.css           Estilos compartidos con prefijo cp-
README.md                     Instrucciones
REVISION_EDITORIAL.md          Pendientes antes de publicar
```

## Integración
1. Copiar el HTML semántico dentro de la plantilla de artículos del CMS (preferiblemente **solo** el contenido de `<article>`; no copiar `<html>`, `<head>` ni `<body>` si el CMS ya los genera).
2. Subir imágenes a la biblioteca de medios y sustituir rutas relativas `images/...` por sus URLs definitivas. Mantener los textos ALT descriptivos, adaptándolos a cada imagen.
3. Integrar los estilos de `assets/css/blog.css` en el sistema de estilos del sitio; ajustar a su diseño actual.
4. Configurar **en el CMS** el `title`, meta description, URL/canonical, Open Graph, Twitter Card, robots, autor verificado, fechas reales y datos estructurados BlogPosting/BreadcrumbList, evitando duplicados con plugins SEO.
5. **Retirar `noindex` solo cuando el artículo esté aprobado y publicado en la URL definitiva.** El `noindex` se dejó deliberadamente para evitar indexación accidental de versiones preliminares.
6. Revisar enlaces internos y llamadas a la acción; en el material original hay enlaces editoriales pendientes y URLs `www.ejemplo.com` no publicables.
7. Verificar responsive, accesibilidad, imágenes, performance, SEO y compatibilidad con el CMS en staging.

## Fuentes y fidelidad
El texto proviene de los cuatro documentos recibidos. Se separaron los anexos de SEO y ejemplos de Schema.org del cuerpo visible. No se han verificado de manera independiente afirmaciones financieras, fiscales, regulatorias, comparativas de competidores ni condiciones comerciales. Las imágenes se agruparon en una sección visual por artículo para evitar asignarles una posición editorial inventada. La conversión de Blog 4 se realizó desde PDF y requiere una revisión adicional de listas, tablas y saltos de párrafo.

## Estado
**Código entregable para revisión e integración técnica, no listo para publicar sin validación editorial/legal y configuración de metadatos.**
