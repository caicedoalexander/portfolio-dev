# Portfolio de Alexander Caicedo

Portfolio personal profesional construido con **Astro 5** y **Tailwind CSS 4**, con un diseño minimalista suizo moderno que destaca por su atención a los detalles y micro-interacciones.

## ✨ Características Destacadas

- 🎨 **Diseño Minimalista Suizo Moderno** - Geometría precisa con personalidad
- 🎭 **Sistema de Diseño Cohesivo** - Variables CSS para temas consistentes
- ⚡ **Performance Optimizada** - SSG con Astro 5
- 🌗 **Dark Mode Automático** - Basado en preferencias del sistema
- 🎬 **Micro-interacciones** - Animaciones sutiles en hover, scroll reveals, staggered animations
- ♿ **Accesible** - Focus states, semántica HTML correcta
- 📱 **Responsive** - Diseño fluido desde móvil a desktop

## 🎨 Sistema de Diseño

### Tipografía
- **Display**: Syne Variable - Bold, geométrica, para títulos
- **Body**: Manrope Variable - Limpia, legible, para contenido
- **Mono**: JetBrains Mono Variable - Para código

### Paleta de Colores
```css
--color-primary: #3b82f6        /* Azul */
--color-accent-energy: #f59e0b  /* Naranja - CTAs principales */
--color-accent-success: #10b981 /* Verde - Skills/logros */
--color-accent-creative: #ec4899 /* Rosa - Proyectos */
```

Todos los colores se adaptan automáticamente a dark/light mode.

## 🏗️ Estructura del Proyecto

```text
/
├── public/
│   ├── alexandercaicedo.jpeg   # Foto de perfil
│   └── projects/               # Imágenes de proyectos
├── src/
│   ├── components/
│   │   ├── icons/             # Iconos SVG como componentes
│   │   ├── Hero.astro         # Sección hero con CTAs
│   │   ├── Skills.astro       # Grid de habilidades con iconos
│   │   ├── Projects.astro     # Showcase de proyectos
│   │   ├── Experience.astro   # Timeline de experiencia
│   │   └── Header.astro       # Navegación fija con scroll effects
│   ├── layouts/
│   │   └── Layout.astro       # Layout base con sistema de diseño
│   ├── pages/
│   │   └── index.astro        # Página principal (SPA)
│   └── styles/
│       └── global.css         # Imports de Tailwind
├── astro.config.mjs           # Config con Tailwind Vite plugin
└── CLAUDE.md                  # Guía para desarrollo con Claude Code
```

## 🚀 Comandos

Todos los comandos se ejecutan desde la raíz del proyecto:

| Comando           | Acción                                              |
| :---------------- | :-------------------------------------------------- |
| `bun install`     | Instala las dependencias                            |
| `bun dev`         | Inicia servidor de desarrollo en `localhost:4321`  |
| `bun build`       | Construye el sitio para producción en `./dist/`    |
| `bun preview`     | Previsualiza el build de producción localmente     |

## 🛠️ Stack Tecnológico

### Core
- [Astro 5](https://astro.build) - Framework web moderno
- [Tailwind CSS 4](https://tailwindcss.com) - Framework CSS utility-first
- [Bun](https://bun.sh) - JavaScript runtime y package manager

### Tipografía
- [@fontsource-variable/syne](https://fontsource.org/fonts/syne) - Display font
- [@fontsource-variable/manrope](https://fontsource.org/fonts/manrope) - Body font
- [@fontsource-variable/jetbrains-mono](https://fontsource.org/fonts/jetbrains-mono) - Monospace font

## 🎯 Secciones del Portfolio

1. **Hero** - Presentación con foto, CTAs prominentes y enlaces sociales
2. **Stack Tecnológico** - Grid de habilidades con iconos coloridos
3. **Experiencia Laboral** - Timeline de experiencia profesional
4. **Proyectos** - Showcase de proyectos destacados con imágenes
5. **Sobre Mí** - Información personal y biografía

## 🎨 Características de Diseño

### Micro-interacciones
- **Hover effects**: Scale, colores, sombras
- **Scroll reveals**: Animaciones de entrada con stagger
- **Active states**: Feedback táctil con scale
- **Gradient text**: Nombre con gradiente multicolor

### Navegación
- **Header fijo** con scroll-based blur/shadow animation
- **IntersectionObserver** para highlighting de sección activa
- **Smooth scroll** a secciones con anclas

### Componentes Reutilizables
- `Badge` - Badge animado con gradiente rotatorio
- `LinkButton` - Botón con estilos consistentes
- `SocialPill` - Pill para enlaces sociales
- `TitleSection` - Títulos de sección con iconos

## 📝 Personalización

### Actualizar Contenido

**Skills** (`src/components/Skills.astro`):
```javascript
const SKILLS = [
  {
    category: "Frontend",
    color: "primary",
    items: [
      { name: "Astro", icon: AstroIcon },
      // ...
    ]
  }
]
```

**Proyectos** (`src/components/Projects.astro`):
```javascript
const PROJECTS = [
  {
    title: "Título del Proyecto",
    description: "Descripción...",
    link: "https://...",
    github: "https://github.com/...",
    image: "/projects/imagen.png",
    tags: [TAGS.REACT, TAGS.NODEJS]
  }
]
```

**Experiencia** (`src/components/Experience.astro`):
```javascript
const EXPERIENCE = [
  {
    role: "Puesto",
    company: "Empresa",
    period: "Fecha - Fecha",
    description: "Descripción..."
  }
]
```

## 🔍 SEO y Meta Tags

El componente `Layout.astro` acepta props para SEO:
```astro
<Layout
  title="Tu título - SEO optimizado"
  description="Tu descripción para motores de búsqueda"
>
```

## 📚 Documentación Adicional

- [CLAUDE.md](./CLAUDE.md) - Guía completa de arquitectura para Claude Code
- [Astro Docs](https://docs.astro.build)
- [Tailwind CSS v4 Docs](https://tailwindcss.com)

## 👤 Autor

**Alexander Caicedo**
- Full Stack Developer
- Especializado en IA Generativa y Agentes Autónomos
- Buenaventura, Colombia

## 📧 Contacto

- Email: a.caicedo.dev@gmail.com
- LinkedIn: [caicedoalexander](https://www.linkedin.com/in/caicedoalexander/)
- GitHub: [caicedoficial](https://github.com/caicedoficial)

---

Desarrollado con ❤️ usando Astro 5 y Tailwind CSS 4
