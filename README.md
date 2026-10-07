# Restaurant Home Page

Página de inicio (landing page) para un restaurante, maquetada con HTML, CSS y un poco de jQuery. Es un sitio estático: no necesita servidor, build ni dependencias instaladas.

## Secciones

La página está dividida en las siguientes secciones dentro de `index.html`:

| Sección | Selector | Contenido |
|---|---|---|
| Header | `header` | Logo, menú de navegación (Home, Pricing, About, Contact) e ícono de menú para móvil. |
| Intro | `#intro` | Imagen de fondo a pantalla, título principal "Only Quality Food" y botones *View Menu* y *Reservation*. |
| Our Story | `#our-story` | Texto de presentación del restaurante a la izquierda y una foto a la derecha. |
| Menu | `#menu` | Cuadrícula de platos en dos filas (`first-row`, `second-row`) que alterna fotos y tarjetas con precio, nombre y descripción. |
| Testimonials | `#testimonials` | Cuatro opiniones de clientes con calificación en estrellas. |
| Contact | `#contact` | Horario de atención con botón de reserva, enlace de contacto y formulario de suscripción al newsletter. |

## Estructura del proyecto

```
.
├── index.html     # Estructura y contenido de la página
├── estilos.css    # Estilos y diseño responsive
├── script.js      # Abre/cierra el menú de navegación en móvil
└── imagenes/      # Fondos, fotos de platos, ícono de menú y estrellas
```

## Tecnologías

- **HTML5**
- **CSS3**: Flexbox para la maquetación y una media query para móvil.
- **jQuery 3.4.1** (por CDN): solo para el menú desplegable en móvil.
- **Google Fonts**: tipografía Poppins.

## Diseño responsive

En pantallas de **800px o menos**:

- El menú de navegación se oculta y aparece un ícono de menú (`.menu-icon`). Al hacer clic, `script.js` muestra u oculta la navegación con `slideToggle()`.
- Las columnas de *Our Story*, *Menu*, *Testimonials* y *Contact* se apilan en una sola columna.
- Se reducen los tamaños de los títulos y textos.

## Cómo verlo

1. Clona o descarga el proyecto.
2. Abre `index.html` en el navegador.

Si quieres que la página se recargue sola al guardar cambios, puedes usar una extensión como **Live Server** de VS Code.

## Convención de nombres

Las clases e IDs están en inglés y describen el rol de cada elemento, no su apariencia. Por ejemplo: `container`, `left-column`, `button-group`, `price`, `description`, `testimonials-container`.

## Mejoras pendientes

- Los títulos usan la fuente `Playfair Display`, pero no se carga desde Google Fonts, así que el navegador muestra una fuente de respaldo.
- La clase `.menu` se usa tanto para la barra de navegación como para el botón *View Menu*. Convendría separarla en dos clases distintas.
- Hay estilos en línea (`style="width: ..."`) en la sección *Menu* que deberían pasar a `estilos.css`.
- Los enlaces de navegación y botones todavía no apuntan a ninguna página (`href=""`).
- Las imágenes no tienen texto alternativo (`alt`), que es importante para la accesibilidad.
