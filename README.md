# danicarrusel

**danicarrusel** es una librería sencilla en JavaScript y CSS para crear un carrusel de imágenes sin dependencias externas. Solo necesitas una estructura HTML básica con imágenes y la librería se encarga del resto automáticamente.

Está pensada para ser **fácil de usar**, ideal para proyectos pequeños o educativos.

---

## Características

* Sin dependencias (vanilla JavaScript)
* Uso muy simple
* Transiciones suaves con CSS
* Botones de navegación automáticos
* Compatible con cualquier imagen

---

## Instalación

Incluye los archivos CSS y JavaScript desde GitHub Pages o descárgalos para tu proyecto.

```html
<link rel="stylesheet" href="https://danicp22.github.io/danicarrusel/danicarrusel.css">
<script src="https://danicp22.github.io/danicarrusel/danicarrusel.js"></script>
```

> Importante: el script debe cargarse **después** del HTML del carrusel.

---

## Uso básico

### 1. Estructura HTML

Solo necesitas un contenedor con la clase `danicarrusel` y las imágenes dentro.

```html
<div class="danicarrusel">
  <img src="imagen1.png" alt="Imagen 1">
  <img src="imagen2.png" alt="Imagen 2">
  <img src="imagen3.png" alt="Imagen 3">
  <img src="imagen4.png" alt="Imagen 4">
</div>
```

No hace falta añadir botones ni contenedores extra:
la librería los crea automáticamente al cargarse.

---

### 2. Resultado

Al cargarse la página, el script:

1. Detecta el contenedor `.danicarrusel`
2. Extrae las imágenes
3. Crea un `<section>` interno para el desplazamiento
4. Inserta los botones de navegación (◀ ▶)
5. Aplica el movimiento horizontal con transiciones CSS

---

## Funcionamiento interno (resumen)

* Cada imagen ocupa **1280x720 px**
* El carrusel se mueve horizontalmente usando `left`
* El desplazamiento se controla con un contador interno
* La animación se realiza con `transition: all 1s`

---

## Estilos por defecto

El carrusel viene con estos estilos base:

* Tamaño fijo: `1280x720`
* Bordes redondeados
* Sombra suave
* Botones centrados verticalmente
* Animación suave al cambiar de imagen

Si quieres modificar el tamaño, deberás ajustar:

* `width` y `height` en `.danicarrusel`
* `width` y `height` en `.danicarrusel section img`
* La variable `anchura` en el JavaScript

---

## Ejemplo completo

```html
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <title>Ejemplo danicarrusel</title>
</head>
<body>

  <div class="danicarrusel">
    <img src="imagen1.png" alt="Imagen 1">
    <img src="imagen2.png" alt="Imagen 2">
    <img src="imagen3.png" alt="Imagen 3">
    <img src="imagen4.png" alt="Imagen 4">
    <img src="imagen5.png" alt="Imagen 5">
    <img src="imagen6.png" alt="Imagen 6">
    <img src="imagen7.png" alt="Imagen 7">
    <img src="imagen8.png" alt="Imagen 8">
  </div>

  <link rel="stylesheet" href="https://danicp22.github.io/danicarrusel/danicarrusel.css">
  <script src="https://danicp22.github.io/danicarrusel/danicarrusel.js"></script>

</body>
</html>
```

---

## Limitaciones actuales

* El número de imágenes está pensado para 8 por defecto
* El tamaño es fijo (no responsive)
* No admite múltiples carruseles en la misma página

Estas limitaciones pueden mejorarse en futuras versiones.

---

## Autor

Creado por **Daniel CP**
Proyecto educativo y experimental.

---
