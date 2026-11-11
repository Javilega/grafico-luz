# grafico-luz

Este repositorio contiene únicamente la **imagen pública** con los precios de la luz (PVPC) y los umbrales de decisión para el control del enchufe inteligente.

## ¿Dónde está el gráfico?

El gráfico **no se guarda en esta rama (`main`)**. Se publica automáticamente en la rama **`gh-pages`** mediante un workflow de GitHub Actions que se ejecuta desde el repositorio privado de control.

Puedes ver la imagen directamente en:

👉 **https://javilega.github.io/grafico-luz/grafico_umbrales.png**

> **Nota:** GitHub Pages puede tardar hasta 10 minutos en reflejar los cambios. Si no ves la imagen actualizada, fuerza la recarga de tu navegador (`Ctrl + F5` o `Cmd + Shift + R`).

## ¿Qué muestra el gráfico?

- **Barras**: PVPC con el descuento de familia numerosa aplicado.
  - **Verde**: Precio por debajo del umbral de inyección (el enchufe se enciende solo).
  - **Azul**: Precio entre el umbral de inyección y el de eficiencia (decisión manual).
  - **Naranja**: Precio por encima del umbral de eficiencia (el enchufe se apaga solo).
- **Línea morada**: PVPC puro, sin descuento.
- **Líneas discontinuas**:
  - **Verde**: Umbral de inyección de calor (precio de eficiencia × factor mensual).
  - **Azul**: Umbral de eficiencia (coste de referencia de la aerotermia).

Los valores bajo cada hora indican el PVPC puro (en morado) y el PVPC con descuento (en negro).

## ¿Cómo se actualiza?

El workflow **"Grafico diario"** del repositorio privado de control genera el gráfico, lo guarda en la carpeta `publicar/` y lo despliega en la rama `gh-pages` de este repositorio usando la acción `JamesIves/github-pages-deploy-action`.

- **Repositorio de origen (privado)**: `Javilega/Enchufe-pvpc`
- **Rama de publicación**: `gh-pages`
- **Archivo publicado**: `grafico_umbrales.png`
- **GitHub Pages**: Activado en la rama `gh-pages` de este repositorio.

## Licencia

Este repositorio solo contiene una imagen generada automáticamente. No hay código ejecutable aquí.
