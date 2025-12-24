# Portfolio Martín Peña Escobedo - Astro + Swiper.js

Portfolio profesional construido con Astro y Swiper.js para el carrusel de testimonios.

## 🚀 Características

- **Astro** - Framework moderno y rápido
- **Swiper.js** - Carrusel de testimonios con autoplay
- **SVG Icons** - Logos vectoriales personalizados
- **Responsive** - Diseño adaptable a todos los dispositivos
- **Animaciones** - Transiciones suaves y efectos interactivos

## 📦 Instalación

```bash
# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev

# Construir para producción
npm run build

# Previsualizar build de producción
npm run preview
```

## 🏗️ Estructura del Proyecto

```
/
├── public/
├── src/
│   ├── components/
│   │   ├── Profile.astro
│   │   ├── Experience.astro
│   │   ├── Tools.astro
│   │   └── Testimonials.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css
├── astro.config.mjs
└── package.json
```

## 🎨 Componentes

### Profile
Información personal, estadísticas y enlaces sociales.

### Experience
Experiencia laboral con empresas como Zaple Tech, El Litoral, Hi Fry, y LT9 Radio.

### Tools
Herramientas digitales con logos SVG animados:
- CapCut (rosa/rojo)
- Canva (degradado cyan-purple)
- OBS Studio (verde con indicador LIVE)
- Adobe Audition (púrpura)
- Adobe Premiere (azul)

### Testimonials
Carrusel de 5 testimonios usando Swiper.js con:
- **Autoplay automático**: 8 segundos entre slides
- **Navegación manual**: Click en bullets para cambiar
- **Pausa en hover**: Se detiene al pasar el mouse
- **Loop infinito**: Ciclo continuo de testimonios
- **Animaciones suaves**: 
  - Nombre aparece desde arriba (fadeInName)
  - Texto aparece desde abajo (fadeInQuote)
  - Transición de slide suave (1000ms)
- **Paginación personalizada**: 
  - Bullets horizontales con barra de progreso
  - Color verde lima (#C5FF00)
  - Animación de progreso durante 8 segundos
- **Diseño centrado**: Una sola línea de texto por slide
- **Responsive**: Se adapta perfectamente a mobile

## 🔧 Configuración de Swiper

El carrusel está configurado con:
- **Efecto**: fade con crossFade
- **Velocidad**: 800ms
- **Autoplay**: 8000ms con pausa en hover
- **Paginación**: Custom con animación de progreso

## 📱 Responsive

- **Desktop**: Grid de 3 columnas
- **Tablet**: Cards apiladas
- **Mobile**: Layout vertical optimizado

## 🎯 Deployment

El sitio puede ser desplegado en:
- Vercel
- Netlify
- GitHub Pages
- Cualquier hosting estático

## 📄 Licencia

Código del portfolio de Martín Peña Escobedo.
