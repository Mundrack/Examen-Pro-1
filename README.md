# Paddlix - Proyecto de Página Web Responsive

## 📋 Descripción del Proyecto

Este proyecto replica el diseño de Paddlix usando HTML5, CSS3 y Sass, implementando las mejores prácticas de desarrollo web moderno.

## 🎯 Características Implementadas

### ✅ Primera Parte - Requisitos Cumplidos:

1. **Flexbox y CSS Grid**
   - Grid para productos (4 columnas, responsive)
   - Grid para accesorios (2 columnas)
   - Grid para stories (3 columnas)
   - Flexbox en header, footer, cards y navegación

2. **Sass Features**
   - ✅ **Variables**: Colores, tipografía, espaciado, breakpoints
   - ✅ **Nesting**: Todos los componentes usan anidación
   - ✅ **Componentes**: 9 componentes modulares separados
   - ✅ **Mixins**: Para responsive, flexbox, grid, overlays

3. **Media Queries**
   - Breakpoints: 480px (móvil), 768px (tablet), 1024px (desktop)
   - Diseño completamente responsive
   - Mobile-first approach

4. **Nomenclatura BEM**
   - Block: `.header`, `.hero`, `.product-card`
   - Element: `.header__logo`, `.hero__title`, `.product-card__image`
   - Modifier: `.button--primary`, `.button--outline`

## 📁 Estructura del Proyecto

```
/
├── index.html                 # Estructura HTML con BEM
├── scss/
│   ├── _variables.scss       # Variables globales
│   ├── _mixins.scss          # Mixins reutilizables
│   ├── _base.scss            # Estilos base y reset
│   ├── styles.scss           # Archivo principal
│   └── components/
│       ├── _button.scss      # Componente de botones
│       ├── _header.scss      # Header y navegación
│       ├── _hero.scss        # Sección hero
│       ├── _product-card.scss # Tarjetas de productos
│       ├── _banner.scss      # Banners promocionales
│       ├── _coaches.scss     # Sección de coaches
│       ├── _collections.scss # Colecciones
│       ├── _stories.scss     # Historias/blog
│       └── _footer.scss      # Footer
├── css/
│   └── styles.css            # CSS compilado
├── images/                    # Imágenes del proyecto
└── README.md                 # Este archivo
```

## 🚀 Instalación y Uso

### Prerrequisitos
```bash
# Node.js y npm instalados
node --version
npm --version
```

### Compilar Sass

```bash
# Instalar Sass globalmente
npm install -g sass

# Compilar una vez
sass scss/styles.scss css/styles.css

# Modo watch (auto-compilar al guardar)
sass --watch scss/styles.scss css/styles.css
```

### Abrir el Proyecto

Simplemente abre `index.html` en tu navegador o usa un servidor local:

```bash
# Con Python
python -m http.server 8000

# Con Node.js (http-server)
npx http-server
```

## 📱 Breakpoints Responsive

- **Mobile**: < 480px
- **Tablet**: 481px - 768px
- **Desktop**: 769px - 1024px
- **Large Desktop**: > 1024px

## 🎨 Variables Sass Principales

```scss
// Colores
$color-primary: #1a1a1a;
$color-accent: #b4ff00;
$color-white: #ffffff;

// Espaciado
$spacing-xs: 8px;
$spacing-sm: 16px;
$spacing-md: 24px;
$spacing-lg: 32px;
$spacing-xl: 48px;

// Tipografía
$font-size-h1: 48px;
$font-size-h2: 36px;
$font-size-base: 16px;
```

## 🧩 Componentes BEM

### Ejemplo de Button Component
```html
<button class="button button--primary">Click me</button>
<button class="button button--outline">Outline</button>
```

### Ejemplo de Product Card
```html
<article class="product-card">
  <div class="product-card__image">
    <img src="..." alt="...">
  </div>
  <h3 class="product-card__name">Product Name</h3>
  <p class="product-card__price">USD 249.00</p>
</article>
```

## 📐 Grid Layout Ejemplos

### Products Grid (4 columnas)
```scss
.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
}
```

### Stories Grid (3 columnas)
```scss
.stories__grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
```

## 🎯 Mixins Útiles

```scss
// Flexbox center
@include flex-center;

// Container responsive
@include container;

// Grid automático
@include grid-auto(250px, 24px);

// Media queries
@include mobile { ... }
@include tablet { ... }
@include desktop { ... }
```

## 📝 Notas para la Evaluación

### Técnicas Aplicadas:

1. **Flexbox**
   - Header navigation
   - Product cards layout
   - Button alignment
   - Footer structure

2. **CSS Grid**
   - Products grid (4 cols → 2 cols → 1 col)
   - Coaches grid (2 cols → 1 col)
   - Stories grid (3 cols → 1 col)
   - Footer grid (4 cols → 2 cols → 1 col)

3. **Sass Features**
   - Variables para colores, tipografía, espaciado
   - Nesting en todos los componentes
   - 9 componentes modulares separados
   - Mixins para DRY (Don't Repeat Yourself)

4. **BEM Naming**
   - Consistente en todo el proyecto
   - Fácil de mantener y escalar
   - Mejora la legibilidad del código

5. **Responsive Design**
   - Mobile-first approach
   - 3 breakpoints principales
   - Images responsive
   - Grid adaptable

## 🖼️ Imágenes Necesarias

Para que el proyecto funcione completamente, necesitas agregar las siguientes imágenes en la carpeta `/images`:

- `hero.jpg` - Imagen hero principal
- `paddle1.jpg` a `paddle8.jpg` - Imágenes de productos
- `choose.jpg` - Banner "How to choose"
- `tech.jpg` - Banner tecnología
- `fun.jpg` - Banner comunidad
- `coach1.jpg`, `coach2.jpg` - Imágenes de coaches
- `balls.jpg`, `cover.jpg` - Accesorios
- `beginner.jpg`, `pro.jpg` - Colecciones
- `guarantee.jpg` - Banner garantía
- `story1.jpg` a `story3.jpg` - Historias

Puedes usar imágenes de:
- [Unsplash](https://unsplash.com) - Fotos gratis
- [Pexels](https://pexels.com) - Fotos gratis
- Crear placeholders con [Placeholder.com](https://placeholder.com)

## ✨ Mejoras Implementadas

- ✅ Smooth scroll behavior
- ✅ Hover effects en cards y botones
- ✅ Transitions suaves
- ✅ Overlays en banners
- ✅ Sticky header
- ✅ Box shadows en cards
- ✅ Image hover effects (scale)
- ✅ Link underline animations

## 📚 Recursos de Aprendizaje

- [Sass Documentation](https://sass-lang.com/documentation)
- [BEM Methodology](http://getbem.com/)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## 👨‍💻 Autor

Proyecto desarrollado como parte del curso de Desarrollo Web.

---

**Nota**: Este proyecto demuestra conocimiento de HTML semántico, CSS moderno, Sass, metodología BEM, diseño responsive y buenas prácticas de desarrollo web.
