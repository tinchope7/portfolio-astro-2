# Notas sobre Swiper.js en Testimonials

## ✨ Características Implementadas

### Autoplay Automático
- Los testimonios cambian automáticamente cada **8 segundos**
- El autoplay se **pausa** cuando pasás el mouse sobre el carrusel
- Se **reanuda** automáticamente cuando sacás el mouse
- El autoplay **no se detiene** al hacer click en los bullets

### Navegación Manual
- **5 bullets** horizontales en la parte inferior
- Click en cualquier bullet para saltar a ese testimonio
- Los bullets tienen un **hover effect** que los agranda verticalmente

### Animaciones
1. **Nombre del autor**:
   - Aparece desde arriba con `fadeInName`
   - Duración: 0.6s
   - Color verde lima (#C5FF00)
   - Centrado y en mayúsculas

2. **Texto del testimonio**:
   - Aparece desde abajo con `fadeInQuote`
   - Duración: 0.8s con delay de 0.2s
   - Color blanco con 95% opacidad
   - Centrado y en una sola línea (word-wrap automático)

3. **Transición entre slides**:
   - Efecto slide horizontal
   - Duración: 1000ms (1 segundo)
   - Suave con easing por defecto

### Barra de Progreso
- Cada bullet muestra una **barra de progreso** verde lima
- La barra se llena durante los 8 segundos del autoplay
- Animación: `bulletProgress 8s linear`
- Solo el bullet activo muestra la animación

### Loop Infinito
- El carrusel vuelve al inicio automáticamente después del último slide
- No hay fin, ciclo continuo

## 🎨 Estilos Personalizados

### Bullets
- **Ancho**: 40px (32px en mobile)
- **Alto**: 4px (3px en mobile)
- **Color inactivo**: rgba(255, 255, 255, 0.2)
- **Color activo**: rgba(197, 255, 0, 0.3)
- **Color hover**: rgba(255, 255, 255, 0.4)

### Contenedor
- **Max-width**: 900px
- **Padding**: 80px (responsive)
- **Background**: #0a0a0a (negro)

## 📱 Responsive

### Desktop (>968px)
- Padding: 80px 24px
- Bullets: 40px x 4px
- Gap entre bullets: 12px

### Tablet (640px - 968px)
- Padding: 60px 24px
- Mantiene tamaño de bullets

### Mobile (<640px)
- Padding: 40px 20px
- Bullets: 32px x 3px
- Gap entre bullets: 8px
- Nombre más pequeño: 20px

## 🔧 Configuración de Swiper

```javascript
{
    modules: [Autoplay, Pagination],
    slidesPerView: 1,
    spaceBetween: 30,
    speed: 1000,
    autoplay: {
        delay: 8000,
        disableOnInteraction: false,
        pauseOnMouseEnter: true,
    },
    pagination: {
        el: '.swiper-pagination',
        clickable: true,
        dynamicBullets: false,
    },
    loop: true,
    effect: 'slide',
}
```

## 🐛 Solución de Problemas

### Si el autoplay no funciona:
1. Verificar que `swiper` y los módulos estén importados
2. Verificar que el evento `astro:page-load` se dispare
3. Revisar consola del navegador por errores

### Si los bullets no son clickeables:
1. Verificar que `clickable: true` esté en la config
2. Revisar que `.swiper-pagination` exista en el DOM

### Si las animaciones no se ven:
1. Verificar que los `@keyframes` estén definidos en el `<style>`
2. Revisar que las clases CSS se apliquen correctamente

## ✅ Testing

Para probar que todo funciona:
1. Abrí el portfolio en el navegador
2. Esperá 8 segundos → debe cambiar automáticamente
3. Pasá el mouse sobre el carrusel → debe pausarse
4. Sacá el mouse → debe reanudarse
5. Hacé click en un bullet → debe saltar a ese slide
6. Observá las animaciones del nombre y texto
7. Observá la barra de progreso en el bullet activo
