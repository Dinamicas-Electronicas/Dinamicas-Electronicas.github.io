# Dinámicas Electrónicas — web

Sitio público de Dinámicas Electrónicas, servido directamente en:

https://dinamicas-electronicas.github.io/

El contenido es HTML estático con CSS propio, sin dependencias de ejecución. La
rama publicada es `main` y GitHub Pages sirve desde la raíz del repositorio.

## Estructura

| Ruta | Contenido |
| --- | --- |
| `index.html` | Portada. |
| `proyectos/` | Índice y fichas de Expanse, RSS2, ChatLand y Vuigram. |
| `en/` | Versión inglesa del sitio. |
| `blog/` | Blog y feeds RSS. Las entradas se generan automáticamente. |
| `assets/` | Estilos, logotipos e imágenes. |
| `blog/automation/` | Generador y configuración del blog automático. |
| `.github/workflows/blog.yml` | Publicación semanal del resumen de los repositorios. |

## Blog automático

Cada lunes a las 06:00 UTC, GitHub Actions lee los commits de los repositorios
del proyecto, agrupa los cambios relevantes y publica una entrada en español e
inglés. También se puede ejecutar a mano desde la pestaña *Actions*.

Los detalles de configuración están en `blog/automation/README.md`.

## Desarrollo local

Al ser HTML estático basta con servirlo desde la raíz del repositorio:

```bash
python3 -m http.server 8080
# http://localhost:8080/
```

## Repositorio antiguo

El sitio se servía antes en `https://dinamicas-electronicas.github.io/web/`.
Esa ruta se conserva mediante un repositorio de redirección para no romper
enlaces antiguos.
