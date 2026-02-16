# Baya Diseño Web - Contexto del Proyecto

## Resumen
Proyecto web profesional para **Baya Diseño**, empresa de diseño web ubicada en Claromeco, Tres Arroyos, Buenos Aires. El sitio incluye múltiples páginas con diseño responsive, animaciones y componentes modernos.

---

## Estructura del Proyecto

```
BayaDiseñoWeb/
├── html/
│   ├── servicios.html      # Página de servicios (Landing Page)
│   └── index.html          # Página principal
├── css/
│   ├── styles.css          # Estilos globales y componentes comunes
│   └── servicios.css       # Estilos específicos de servicios
├── js/
│   └── main.js             # Scripts JavaScript
├── src/
│   ├── Logo/               # Logos de la empresa
│   ├── iconos/             # Iconos de redes sociales
│   ├── servicio/           # Imágenes específicas de servicios
│   └── main/               # Imágenes generales
├── fonts/                  # Fuentes personalizadas (Brisa Sans, Corbel)
└── imagenes/               # Imágenes del sitio
```

---

## Páginas Principales

### 1. Servicios (`html/servicios.html`)
Página de venta de Landing Pages unificada con contenido del index:

- **Hero Section**: Título principal + imagen del indio con gradiente celeste-blanco
- **Sección de presentación** (traída de index): Layout de 3 columnas con redes sociales, texto de presentación de Baya Diseño y 6 tarjetas de servicios (adaptada con estilos de servicios.css)
- **Guarda decorativa**: Imagen separadora
- **Cards de valores** (traídas de index): 3 cards con título, imagen y descripción (Lo Importante, El Diseño, Análisis)
- **Tarjetas de servicios**: 3 tarjetas con imagen, título, texto y botón
- **¿Por qué una landing?**: Lista de beneficios con imagen del niño flotante
- **Formulario de contacto**: Input tipo alert con diseño moderno
- **Footer completo**: Logo, redes sociales, navegación, contacto

**Características especiales de Servicios:**
- Layout de tarjetas cambia a horizontal (< 950px)
- Imagen del niño con animación de flotación continua
- Imágenes decorativas (.img-izq, .img-der) con animación vertical alternada
- Título con efecto hover de escala
- Div1 del index integrado con estilos adaptados a la paleta de servicios

### 2. Index (`html/index.html`)
Página principal (estructura similar, contenido variable)

---

## Componentes Clave

### Layout General
- **Container central**: `.central` con ancho controlado
- **Header moderno fusionado** (`.header-modern`): 
  - Logo grande a la izquierda (115-130px) - marca principal visible
  - Dos botones de navegación a la derecha: Home y Contacto
  - Color turquesa (#19C1CE) que combina con toda la página
  - Diseño redondeado con efecto glassmorphism
  - Sticky en la parte superior
- **Footer fijo**: Copyright + logo pequeño

### Tarjetas de Servicios (`.tarjeta1Serv`)
**Desktop (> 950px):**
- 3 tarjetas en fila horizontal
- Formato vertical: imagen arriba, contenido abajo

**Tablet (700px - 950px):**
- Tarjetas apiladas verticalmente
- Formato horizontal: imagen izquierda (35%), contenido derecha (65%)
- Botón centrado abajo

**Móvil (< 700px):**
- Formato vertical centrado

### Formulario de Contacto (`.inputSer`)
Estética tipo alert/CTA:
- Fondo degradado crema
- Borde izquierdo naranja (#FF6600) de 5px
- Icono de email flotante arriba
- Input con focus naranja
- Botón con gradiente y efectos hover

### Footer (`.div5`)
Estructura en dos niveles:

**Nivel superior (`.arriba`):**
- Logo de la empresa (80px)
- Botones de redes sociales (redondos, glassmorphism)
  - Facebook
  - Contacto (email)
  - Producto
  - Nosotros (aboutUs)

**Nivel inferior (`.abajo`):**
- Columna izquierda (54%): Categorías principales + 6 enlaces en 2 columnas
- Columna derecha (46%): Información de contacto (dirección, teléfono, email)

**Diseño:**
- Fondo degradado turquesa (#19C1CE → #17a8b3)
- Barra decorativa naranja arriba
- Tipografía Roboto, colores blancos semi-transparentes

---

## Estilos y Convenciones

### Fuentes Utilizadas
- **Lato**: Títulos principales (bold)
- **Roboto / Roboto Mono**: Textos corporativos
- **Nova Square**: Especificaciones técnicas
- **Oregano**: Títulos elegantes/decorativos
- **Montserrat**: Botones

### Paleta de Colores
- **Primario**: #19C1CE (turquesa)
- **Acento**: #FF6600 (naranja)
- **Secundario**: #AB682F (marrón/cobre)
- **Fondos**: #F8F5EC (crema), #ffffff (blanco)
- **Texto**: #333333 (oscuro), rgba(255,255,255,0.9) (claro)

### Breakpoints Responsive
- **Desktop**: > 1200px
- **Tablet**: 700px - 1200px
- **Móvil**: < 700px
- **Móvil pequeño**: < 450px

### Animaciones Comunes
1. **Flotar**: Movimiento vertical continuo (usado en imagen del niño)
2. **MoverVertical**: Subida/bajada de 15px (imágenes decorativas)
3. **Hover scale**: Escala 1.08 al pasar mouse (títulos)
4. **Transiciones**: 0.3s-0.4s ease-out para interactividad

---

## Mejores Prácticas del Proyecto

### CSS
- Uso extensivo de **CSS Grid** para layouts complejos (tarjetas)
- **Flexbox** para alineaciones simples
- **clamp()** para tipografía fluida y proporcional
- **Variables implícitas** mediante comentarios
- Media queries anidados por componente

### HTML
- Estructura semántica (header, nav, main, footer)
- Clases BEM-like (`.tarjeta1Serv`, `.tituloTarj1Serv`)
- Comentarios de sección claros

### Imágenes
- Rutas relativas: `../src/...`
- Formatos: PNG preferido para transparencias
- Convención de nombres: camelCase o kebab-case

---

## Notas Importantes para el Desarrollo

1. **Footer fijo**: El footer final (`<footer>`) tiene `position: fixed` en la parte inferior. Verificar que no tape contenido importante.

2. **Animaciones**: Las imágenes decorativas (`.img-izq`, `.img-der`) tienen posición absoluta y animaciones. Asegurar `overflow: hidden` en contenedores padre.

3. **Tarjetas responsive**: El cambio de layout vertical a horizontal ocurre a los 950px mediante CSS Grid.

4. **Formulario**: El componente `.inputSer` tiene diseño tipo "alerta" con icono emoji (📧) posicionado absolutamente.

5. **Gradientes**: Usados frecuentemente para fondos y botones (linear-gradient 135deg).

---

## Contacto del Cliente
- **Ubicación**: Claromeco, Tres Arroyos, Buenos Aires
- **Teléfono**: +549 2983 60-9425
- **Email**: bayadiseño@gmail.com
- **Año**: 2025

---

## Regla de Commits por Tarea
- Cada tarea realizada debe terminar en un commit independiente que describa el propósito y el resultado (el "por qué" de la tarea).
- El mensaje de commit debe ser claro y breve (máximo 60-72 caracteres en el subject) y reflejar el objetivo de la tarea.
- Recomendación de formato de mensaje (uno de estos):
-   - `feat: ...` para nueva funcionalidad o mejora significativa
-   - `fix: ...` para corrección de errores
-   - `docs: ...` para documentación
-   - `chore: ...` para cambios de mantenimiento sin impacto de funcionalidad
- El cuerpo del commit debe incluir contexto básico, motivos y forma de verificación (parámetros de prueba o pasos de verificación).
- Evitar commits que contengan secretos o información sensible.
- Mantener un historial legible y atómico: los commits deben ser poder desambiguar cambios lógicamente independientes.
- Se recomienda agrupar todos los cambios de una tarea en su propio commit y no mezclar cambios de tareas distintas.
- Si se trabajan en varias correcciones pequeñas, considerar commits de tipo `fix` secuenciales por cada corrección.
- En caso de requerir revertir, preferir `revert:` con referencia al commit anterior y el motivo.
 
## Historial de Modificaciones Recientes
- ✅ Layout horizontal de tarjetas a partir de 950px
- ✅ Animación continua de imagen del niño
- ✅ Rediseño de footer con estética moderna
- ✅ Formulario tipo alert con icono flotante
- ✅ Corrección de transparencias en logos e iconos
- ✅ Integración de div1 (presentación empresa) desde index a servicios
- ✅ Adaptación de estilos del div1 para combinar con paleta de servicios
- ✅ Integración de div2 (cards de valores) desde index a servicios
- ✅ Rediseño de header: Menu reducido a 2 botones (Home y Contacto) + Logo grande a la izquierda
- ✅ Header moderno con glassmorphism y color turquesa (#19C1CE)
