# Portafolio Interactivo

Portafolio web creado para mostrar efectos visuales con CSS. Incluye una presentación, tarjetas de proyectos con transformaciones 2D, una tarjeta interactiva 3D y un formulario de contacto. La interfaz está construida con HTML y CSS, y utiliza Bootstrap para la navegación y el diseño adaptable.

## Transformaciones, transiciones y animaciones

Los efectos se implementan en `style.css` y se activan al pasar el cursor sobre las tarjetas:

| Elemento | Efecto |
| --- | --- |
| Primera tarjeta de proyecto | Rotación 2D de `7deg` mediante `rotate(7deg)`. |
| Segunda tarjeta de proyecto | Escalado a `1.16` veces su tamaño con `scale(1.16)`. |
| Tercera tarjeta de proyecto | Desplazamiento hacia arriba de `16px` con `translateY(-16px)`. |
| Tarjeta de experiencia 3D | Un contenedor con `perspective: 1000px` da profundidad; al pasar el cursor, la tarjeta gira `30deg` en los ejes X e Y. |
| Título de presentación | La animación `deslizarDerecha` mueve el título horizontalmente entre `-60px` y `60px`, mientras cambia su opacidad. Dura 4 segundos, se repite indefinidamente y alterna la dirección. |
| Indicador de carga | La animación `girarLoader` rota el indicador circular continuamente en 360 grados. Dura 1 segundo por vuelta y usa velocidad lineal. |

Las transformaciones de las tarjetas y sus sombras cambian con transiciones suaves: `0.45s` en las tarjetas de proyecto y `0.6s` en la tarjeta 3D. La página también utiliza desplazamiento suave al navegar entre secciones. En pantallas pequeñas se ajustan el espaciado y los tamaños para mantener el contenido legible.

> Los efectos de las tarjetas dependen de `:hover`, por lo que su interacción puede variar en dispositivos táctiles. La configuración `prefers-reduced-motion` desactiva el desplazamiento suave y las transiciones de las tarjetas; las animaciones continuas del título y del indicador siguen activas.

## Tecnologías

- **HTML5:** estructura y contenido de la página.
- **CSS3:** diseño visual, degradados, sombras, transformaciones, transiciones, animaciones y media queries.
- **Bootstrap 5.3.3:** cuadrícula adaptable, navegación, botones y estilos del formulario; su bundle JavaScript habilita el menú desplegable.
- **JavaScript propio:** `script.js` está reservado para futuras funcionalidades y actualmente no contiene lógica.

## Estructura del proyecto

```text
Portafolio-Interactivo-VF/
├── index.html
├── style.css
├── script.js
├── img/
│   ├── logo.png
│   └── tecnologia-3d.png
└── README.md
```

## Cómo ejecutarlo

No es necesario instalar dependencias ni compilar el proyecto:

1. Descarga o clona el repositorio.
2. Abre `index.html` en un navegador moderno.

También puedes abrir la carpeta en Visual Studio Code y utilizar Live Server. Se requiere conexión a Internet para cargar Bootstrap desde el CDN de jsDelivr.

## Cómo probar los efectos

1. Usa la barra de navegación o el botón **Ver proyectos** para recorrer las secciones.
2. Pasa el cursor por cada tarjeta de proyecto para ver su rotación, escalado o desplazamiento.
3. Pasa el cursor por la tarjeta **Experiencia 3D** para observar su inclinación.
4. Observa el movimiento del título y la rotación continua del indicador circular.
5. Cambia el ancho de la ventana para comprobar la adaptación de la cuadrícula y del menú.

## Formulario de contacto

El formulario verifica los campos obligatorios y el formato del correo mediante la validación nativa del navegador. Los botones permiten intentar el envío o limpiar los campos, pero no hay una integración con un servidor: los mensajes no se entregan.

## Personalización

- Edita `index.html` para cambiar los textos, las tarjetas o los campos del formulario.
- Modifica `style.css` para ajustar los colores, las distancias, los tiempos y los efectos.
- Sustituye las imágenes dentro de `img/` o actualiza sus rutas en el HTML.
- Añade funcionalidades en `script.js` si necesitas lógica propia, como procesar el formulario u ocultar el indicador al terminar la carga.
