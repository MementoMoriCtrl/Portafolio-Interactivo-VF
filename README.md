# Portafolio Interactivo

Proyecto web de presentación que demuestra transformaciones 2D y 3D, transiciones y animaciones con CSS. Incluye una sección de proyectos y un formulario de contacto, con un diseño adaptable a distintos tamaños de pantalla.

## Características

- Barra de navegación con enlaces a Inicio, Proyectos y Contacto, y menú desplegable en pantallas pequeñas.
- Presentación con título animado y botón para explorar los proyectos.
- Tres tarjetas con efectos al pasar el cursor: rotación, escalado y desplazamiento vertical.
- Tarjeta con perspectiva y rotación en los ejes X e Y para mostrar un efecto 3D.
- Indicador circular con animación continua.
- Formulario con campos de nombre, correo electrónico y mensaje, además de botones para enviar y limpiar.
- Desplazamiento suave entre secciones y ajustes de diseño mediante media queries.

## Tecnologías

| Tecnología | Uso |
| --- | --- |
| HTML5 | Estructura y contenido de la página. |
| CSS3 | Estilos, degradados, sombras, transformaciones y animaciones. |
| Bootstrap 5.3.3 | Cuadrícula adaptable, navegación, botones y formularios. |
| JavaScript | Bootstrap utiliza su bundle para el menú desplegable. El archivo local `script.js` está vacío y disponible para futuras funcionalidades. |

## Estructura del proyecto

```text
Portafolio-Interactivo-1/
├── index.html           # Página principal
├── style.css            # Estilos y animaciones personalizadas
├── script.js            # Archivo reservado para JavaScript propio
├── img/
│   ├── logo.png         # Logo de la barra de navegación
│   └── tecnologia-3d.png # Imagen de la tarjeta 3D
└── README.md
```

## Cómo ejecutarlo

1. Descarga el proyecto o clona el repositorio:

   ```bash
   git clone https://github.com/MementoMoriCtrl/Portafolio-Interactivo.git
   cd Portafolio-Interactivo
   ```

2. Abre `index.html` en un navegador moderno.

También puedes abrir la carpeta en Visual Studio Code y servir `index.html` con la extensión Live Server, si la tienes instalada.

No requiere instalar dependencias ni ejecutar un proceso de compilación. Se necesita conexión a Internet para cargar los estilos y el JavaScript de Bootstrap desde el CDN de jsDelivr.

## Cómo explorar las interacciones

1. Utiliza el menú o el botón **Ver proyectos** para recorrer las secciones.
2. Pasa el cursor sobre cada tarjeta para observar las transformaciones 2D.
3. Pasa el cursor sobre la tarjeta de **Experiencia 3D** para ver su inclinación.
4. Cambia el ancho de la ventana para comprobar la distribución adaptable y el menú móvil.
5. Completa los campos del formulario o utiliza **Limpiar** para restablecerlos.

## Estado actual

El formulario utiliza la validación nativa de HTML para los campos obligatorios y el formato del correo. No tiene un servicio de envío ni una integración con un servidor, por lo que no entrega mensajes.

El indicador circular permanece visible y animado: todavía no existe lógica para ocultarlo cuando termina la carga. Los efectos de las tarjetas se activan mediante `:hover`; su comportamiento puede variar en dispositivos táctiles.

La preferencia de movimiento reducido desactiva el desplazamiento suave y las transiciones de las tarjetas. Las animaciones continuas del título y del indicador permanecen activas.

## Personalización

- Modifica `index.html` para actualizar textos, proyectos y campos del formulario.
- Edita `style.css` para cambiar colores, tamaños, animaciones y puntos de adaptación.
- Sustituye las imágenes de `img/` manteniendo sus nombres o actualizando sus rutas en el HTML.
- Añade funcionalidades propias en `script.js`, como gestionar el formulario u ocultar el indicador de carga.
